# CloudFront

Amazon CloudFront speeds up distribution of your static and dynamic web content, such as .html, .css, .php, image, and media files. When users request your content, CloudFront delivers it through a worldwide network of edge locations that provide low latency and high performance.

- provides low latency and high data transfer speeds for distribution of static, dynamic web or streaming content to web users
- delivers the content through a worldwide network of data centers called **Edge Locations**
- keeps persistent connections with the origin servers so that the files can be fetched from the origin servers as quickly as possible.
- dramatically **reduces the number of network hops** that users’ requests must pass through
- supports **multiple origin server options**, like AWS hosted service *for e.g. S3, EC2, ELB* or an on premise server, which stores the original, definitive version of the objects
- **single distribution can have multiple origins** and Path pattern in a cache behavior determines which requests are routed to the origin
- supports **Web Download** distribution and **RTMP Streaming** distribution
  - Web distribution supports static, dynamic web content, on demand using progressive download & HLS and live streaming video content
  - RTMP supports streaming of media files using Adobe Media Server and the Adobe Real-Time Messaging Protocol (RTMP) **ONLY**
- supports HTTPS using either
  - **dedicated IP address**, which is expensive as dedicated IP address is assigned to each CloudFront edge location
  - **Server Name Indication (SNI)**, which is free but supported by modern browsers only with the domain name available in the request header
- For E2E HTTPS connection,
  - **Viewers -> CloudFront** needs either **self signed certificate, or certificate issued by CA or ACM**
  - **CloudFront -> Origin** needs **certificate issued by ACM for ELB and by CA for other origins**
- Security
  - **Origin Access Identity** (OAI) can be used to restrict the content from S3 origin to be accessible from CloudFront only
  - supports **Geo restriction (Geo-Blocking) to whitelist or blacklist** countries that can access the content
  - **Signed URLs **
    - for RTMP distribution as signed cookies aren’t supported
    - to restrict access to individual files, *for e.g., an installation download for your application.*
    - users using a client, *for e.g. a custom HTTP client,* that doesn’t support cookies
  - **Signed Cookies**
    - provide access to multiple restricted files, *for e.g., video part files in HLS format or all of the files in the subscribers’ area of a website.*
    - don’t want to change the current URLs
  - integrates with AWS **WAF**, a web application firewall that helps protect web applications from attacks by allowing rules configured based on IP addresses, HTTP headers, and custom URI strings
- supports **GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE** to get object & object headers, add, update, and delete objects
  - **only caches** responses to **GET and HEAD** requests and, optionally, OPTIONS requests
  - **does not cache** responses to **PUT, POST, PATCH, DELETE** request methods and these requests are proxied back to the origin
- object **removal** from cache
  - would be removed upon **expiry (TTL)** from the cache, by default 24 hrs
  - can be **invalidated explicitly**, but has a cost associated, however might continue to see the old version until it expires from those caches
  - objects can be **invalidated only for Web distribution**
  - change object name, **versioning**, to serve different version
- supports adding or modifying custom headers before the request is sent to origin which can be used to
  - **validate** if user is accessing the content from CDN
  - **identifying CDN** from which the request was forwarded from, in case of multiple CloudFront distribution
  - for **viewers not supporting CORS** to return the Access-Control-Allow-Origin header for every request
- supports **Partial GET requests** using range header to download object in smaller units improving the efficiency of partial downloads and recovery from partially failed transfers
- supports **compression** to compress and serve compressed files when viewer requests include Accept-Encoding: gzip in the request header
- supports different **price class** to include all regions, to include only least expensive regions and other regions to exclude most expensive regions
- supports **access logs** which contain detailed information about every user request for both web and RTMP distribution

## Use scenarios

- Distribute content with low latency and high data transfer rates by serving requests using a network of edge locations around the world
- Use standard cache control headers you set on your files to identify static and dynamic content

> [Service overview](https://aws.amazon.com/cloudfront/)
