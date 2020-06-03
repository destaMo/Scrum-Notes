# AWS Batch

AWS Batch enables developers, scientists, and engineers to easily and efficiently run hundreds of thousands of batch computing jobs on AWS. AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory optimized instances) based on the volume and specific resource requirements of the batch jobs submitted. With AWS Batch, there is no need to install and manage batch computing software or server clusters that you use to run your jobs, allowing you to focus on analyzing results and solving problems. AWS Batch plans, schedules, and executes your batch computing workloads across the full range of AWS compute services and features, such as Amazon EC2 and Spot Instances.

There is no additional charge for AWS Batch. You only pay for the AWS resources (e.g. EC2 instances) you create to store and run your batch jobs.

- **fully managed**
  - AWS Batch eliminates the need to operate third-party commercial or open source batch processing solutions. There is no batch software or servers to install or manage. AWS Batch manages all the infrastructure for you, avoiding the complexities of provisioning, managing, monitoring, and scaling your batch computing jobs
- **integrates with AWS**
  - AWS Batch is natively integrated with the AWS platform, allowing you to leverage the scaling, networking, and access management capabilities of AWS. This makes it easy to run jobs that safely and securely retrieve and write data to and from AWS data stores such as Amazon S3 or Amazon DynamoDB.

## Use scenarios

### Financial services

Financial Services organizations, from fintech startups to longstanding enterprises, have been utilizing batch processing in areas such as high performance computing for risk management, end-of-day trade processing, and fraud surveillance. You can use AWS Batch to minimize human error, increase speed and accuracy, and reduce costs with automation, so that you can refocus on evolving the business.

#### High performance computing

The Financial Services industry has advanced the use of high performance computing in areas such as pricing, market positions, and risk management. By taking these compute-intensive workloads onto AWS, organizations have increased speed, scalability, and cost-savings. With AWS Batch, organizations can automate the resourcing and scheduling these jobs to save costs and accelerate decision-making and go-to-market speeds.

![high performance computing](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium_flowchart%20diagrams_v3_kw-01.4ea7fa029996903a29f867d42d308f66568c2d5e.png)

#### Post-trade analytics

Trading desks are constantly looking for opportunities to improve their positions by analyzing the day’s transaction costs, execution reporting, and market performance, among other areas. All of this requires require batch processing of large data sets from multiple sources after the trading day closes. AWS Batch enables the automation of these workloads so that you can understand the pertinent risk going into the next day’s trading cycle and make better decisions based on data.

![post trade analytics](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium_flowchart%20diagrams_v3_kw-02.322877d73eda8ed71a44db216a1d195550befac0.png)

#### Fraud surveillance

Fraud is an ongoing concern impacting all industries, especially Financial Services. Amazon Machine Learning enables more intelligent ways to analyze data using algorithms and models to combat this challenge. When used in conjunction with AWS Batch, organizations can automate the data processing or analysis required to detect irregular patterns in your data that could be an indicator of fraudulent activity such as money laundering and payments fraud.

![fraud surveillance](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium_flowchart%20diagrams_v3_kw-03.071d7c6d71777e7b7b109fdd9221ddd41922b4bf.png)

### Life sciences

The scientific insight that allows Biopharmaceutical and Genomics companies to bring products to market demand high performance computing environments. AWS Batch can be applied throughout your organization in applications such as computational chemistry, clinical modelling, molecular dynamics, and genomic sequencing testing and analysis.

#### Drug screening

AWS Batch allows research scientists involved in drug discovery to more efficiently and rapidly search libraries of small molecules in order to identify those structures which are most likely to bind to a drug target, typically a protein receptor or enzyme. By doing this, scientists can capture better data to begin drug design and have a deeper understanding for the role of a particular biochemical process, which could potentially lead to the development of more efficacious drugs and therapies.

![drug screening](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium---flowchart-diagrams_UseCase1-ScreeningforPharma.b24e75093f2868a866995df6bbeca059b8acd1d5.png)

#### DNA sequencing

After bioinformaticians complete their primary analysis of a genomic sequence to produce the raw files, they can use AWS Batch to complete their secondary analysis. With AWS Batch, customers can simplify and automate the assembly of the raw DNA reads into a complete genomic sequence by comparing the multiple overlapping reads and the reference sequence, as well as potentially reduce data errors caused by incorrect alignment between the reference and the sample.

![DNA](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium---flowchart-diagrams_UseCase2-ScreeningforPharma.feace97dd6b9ca68f948851ebff63c8acafe2a01.png)

### Digital media

Media and Entertainment companies require highly scalable batch computing resources to enable accelerated and automated processing of data as well as the compilation and processing of files, graphics, and visual effects for high-resolution video content. Use AWS Batch to accelerate content creation, dynamically scale media packaging, and automate asynchronous media supply chain workflows.

#### Rendering
AWS Batch provides content producers and post-production houses with tools to automate content rendering workloads and reduces the need for human intervention due to execution dependencies or resource scheduling. This includes the scaling of compute cores in a render farm, triggering spot market compute instances, and coordinating the execution of disparate steps in the process.

![rendering](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium-Diagrams_Visual-Effects-Rendering.ad9c0479c3772c67953e96ef8ae76a5095373d81.png)

AWS Batch accelerates batch and file based transcoding workloads by automating workflows, overcoming resource bottlenecks, and reducing the number of manual processes by scheduling and monitoring the executing of asynchronous processes, then triggering conditional responses to scale resources for a given workload when necessary.

![transcoding](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium-Diagrams_Content-Library-Processing-Supply-Chains.0807151efb37a7170a68850114dc489650f48d0e.png)

#### Media supply chain

AWS Batch simplifies complex media supply chain workflows by coordinating the execution of disparate and dependent jobs at different stages of processing, and supports a common framework for managing content preparation for different contributors to the media supply chain.

![media supply chain](https://d1.awsstatic.com/Test%20Images/Kate%20Test%20Images/Dilithium-Diagrams_Media-Processing-Supply-Chains.7fc28d097dc9326ef5733e5df5a4fc59f7c58c26.png)

> [Batch overview](https://aws.amazon.com/batch/)
