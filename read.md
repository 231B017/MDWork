## Week 1
### 1. Which of the following best represents the meaning of resource pooling in cloud computing?

- A. Every customer receives a permanently dedicated physical server.
- B. Computing resources are dynamically assigned to multiple customers using a shared infrastructure.
- C. Resources can only be accessed from a local network.
- D. Users must manually allocate hardware before using cloud services.

**Correct Answer:** B

**Solution:** Resource pooling is one of the NIST essential characteristics of cloud computing. Providers serve multiple customers using shared computing resources that are dynamically assigned and reassigned according to demand.

### 2. A startup rents virtual servers on Amazon EC2. The team installs and patches its own operating system, configures the web server, and manages the runtime and applications itself. The provider supplies only the virtualized compute, storage, and networking. This is best classified as:

- A. SaaS
- B. PaaS
- C. IaaS
- D. FaaS

**Correct Answer:** C

**Solution:** The consumer manages the operating system, runtime, and applications while the provider supplies virtualized compute, storage, and networking. This division of responsibility is the defining feature of Infrastructure as a Service (IaaS).

### 3. Which deployment model allows an organization to maintain cloud infrastructure exclusively for its own use, either on-premises or hosted by a third party?

- A. Public Cloud
- B. Hybrid Cloud
- C. Community Cloud
- D. Private Cloud

**Correct Answer:** D

**Solution:** A private cloud is dedicated to a single organization, providing greater control over security, compliance, and resource management.

### 4. Virtualization technology allows multiple virtual machines (VMs) to run on a single physical system or on a cluster of physical systems. Which of the following statements is the MOST accurate?

- A. Each VM always shares the same operating system kernel with the host OS.
- B. Multiple VMs can run different operating systems on the same physical machine simultaneously.
- C. Virtualization is only possible in cloud computing environments.
- D. Virtualization prevents resource overcommitment on the host system.

**Correct Answer:** B

**Solution:** Modern hypervisors (e.g., VMware, KVM) allow multiple VMs with different OSs to share the same physical hardware. Option A describes containers more than full VMs. Virtualization pre-dates cloud (so C is false), and resource overcommitment (CPU/memory overcommit) is actually a feature often used, not prevented (D is false).

### 5. Consider the following statements about distributed systems (DS):
(i) DS can improve scalability by adding more nodes to the system.
(ii) DS can increase fault tolerance through data and service replication.
(iii) DS guarantees lower latency for every single operation compared to a centralized system.
Choose the MOST APPROPRIATE option:

- A. (i) and (ii)
- B. Only (iii)
- C. (i) and (iii)
- D. (i), (ii), and (iii)

**Correct Answer:** A

**Solution:** Distributed systems improve scalability by adding nodes and increase fault tolerance through replication. However, distribution introduces network communication and coordination overhead, so lower latency for every operation is not guaranteed and some operations may be slower (iii is false).

### 6. The combination of Service-Oriented Architecture (SOA) and Cloud Computing led to a paradigm where almost any IT capability can be delivered as a network-accessible service. This is often referred to as:

- A. FTP
- B. SNTP
- C. XaaS
- D. FaaS

**Correct Answer:** C

**Solution:** XaaS = “Anything/Everything as a Service”, an umbrella term for delivering diverse IT services via the cloud. FaaS (Functions as a Service) is only one specific service model, not the broad paradigm.

### 7. Which of the following correctly describes a Type-2 (hosted) hypervisor?

- A. It runs directly on the physical hardware without any underlying operating system.
- B. It runs as an application on top of a host operating system.
- C. It always provides lower virtualization overhead than a Type-1 hypervisor.
- D. It cannot run more than one virtual machine at a time.

**Correct Answer:** B

**Solution:** A Type-2 (hosted) hypervisor runs as an application on top of a host operating system (e.g., VirtualBox, VMware Workstation). A Type-1 (bare-metal) hypervisor runs directly on hardware and typically gives lower overhead, so A and C describe Type-1; D is false since hosted hypervisors can run multiple VMs.

### 8. Which of the following are advantages of Platform-as-a-Service (PaaS)?
(i) Developers can focus primarily on application development.
(ii) Automatic software updates for the underlying platform.
(iii) Complete control over physical server hardware.
(iv) Faster application deployment.

- A. (i), (ii), and (iv)
- B. (ii) and (iii)
- C. (i) and (iii)
- D. (i), (ii), (iii), and (iv)

**Correct Answer:** A

**Solution:** PaaS simplifies software development by abstracting infrastructure management and providing managed runtime environments. Developers typically do not control physical hardware.

### 9. Which of the following services is most likely to be classified as Infrastructure as a Service (IaaS)?

- A. Microsoft Word Online
- B. Amazon EC2 Virtual Machines
- C. Google Docs
- D. Salesforce CRM

**Correct Answer:** B

**Solution:** Amazon EC2 provides virtual machines where users manage the operating system, software, and applications, making it an IaaS offering.

### 10. A __________ is a form of distributed computing in which a large number of geographically dispersed and often heterogeneous resources across multiple administrative domains are loosely coupled and coordinated to work together on a common, large-scale task.

- A. Cluster
- B. Grid
- C. Node
- D. Hypervisor

**Correct Answer:** B

**Solution:** Grid computing coordinates geographically dispersed, heterogeneous, and loosely coupled resources spanning multiple administrative domains to solve large-scale tasks. Clusters are tightly coupled and co-located, a node is a single machine, and a hypervisor is virtualization software.
## Week 2
### 1. A virtualization solution requires the guest operating system to invoke hypercalls instead of executing certain privileged instructions directly. This approach is known as:

- A. Full Virtualization
- B. Hardware-assisted Virtualization
- C. Para-virtualization
- D. Containerization

**Correct Answer:** C

**Solution:** Para-virtualization modifies the guest operating system so that privileged operations are performed through hypercalls to the hypervisor. This reduces virtualization overhead but requires OS modification.

### 2. Which of the following is a key characteristic of full (hardware-assisted) virtualization, as opposed to para-virtualization?

- A. Guest OS must be modified to issue hypercalls to the hypervisor.
- B. Guest OS runs unmodified, with the hypervisor and CPU extensions handling privileged instructions.
- C. Guest and host must share the same operating system kernel.
- D. No hypervisor is involved at all.

**Correct Answer:** B

**Solution:** In full (hardware-assisted) virtualization, an unmodified guest OS runs while CPU extensions (e.g., Intel VT-x, AMD-V) and the hypervisor transparently handle privileged instructions. Option A describes para-virtualization (guest OS modified via hypercalls), C describes containers, and D is false since a hypervisor is always present.

### 3. Which statement about a public cloud is MOST accurate?

- A. It is dedicated to, and controlled by, a single organization behind its own firewall.
- B. Its infrastructure is provisioned for open use by the general public and is owned and operated by a cloud service provider.
- C. It is shared only among organizations that have common regulatory concerns.
- D. It always guarantees stronger data isolation than a private cloud.

**Correct Answer:** B

**Solution:** A public cloud is provisioned for open use by the general public and is owned, managed, and operated by a cloud service provider on its own premises. Option A describes a private cloud, C describes a community cloud, and D is false since private clouds typically provide stronger isolation.

### 4. An application must repeatedly navigate, randomly access, and modify elements of a moderately sized XML document held in memory. Which XML parser API is MOST appropriate?

- A. SAX (push-based, event-driven, forward-only)
- B. StAX (pull-based, event-driven, forward-only)
- C. DOM (builds an in-memory tree allowing random access and modification)
- D. None; an XML document cannot be modified once parsed

**Correct Answer:** C

**Solution:** DOM builds a complete in-memory tree representation of the document, enabling random access, navigation, and in-place modification of elements. This suits documents that fit in memory and require manipulation. SAX and StAX are forward-only streaming parsers not designed for random access or modification, so they are unsuitable here.

### 5. Which statement correctly distinguishes a 'host OS', a 'guest OS', and a 'hypervisor'?

- A. The host OS runs inside a VM, the guest OS runs on bare metal, and the hypervisor is a user application.
- B. The hypervisor creates and manages VMs; each guest OS runs inside a VM; and for a Type-2 hypervisor, the host OS is the OS on which the hypervisor runs.
- C. The guest OS and host OS are always identical copies of the same operating system.
- D. The hypervisor is simply the hardware layer located beneath the host OS.

**Correct Answer:** B

**Solution:** The hypervisor creates and manages virtual machines; each guest OS runs inside its own VM; and for a Type-2 (hosted) hypervisor, the host OS is the operating system on which the hypervisor runs as an application. Option A reverses the host/guest roles, C is false, and D incorrectly describes the hypervisor as hardware.

### 6. An enterprise migrates its private cloud to a third-party managed data center. Which of the following concerns should be evaluated?
(i) Service availability guarantees (SLAs)
(ii) Compliance with data protection regulations
(iii) Network latency between users and cloud resources

- A. Only (i)
- B. (i) and (ii)
- C. (ii) and (iii)
- D. (i), (ii), and (iii)

**Correct Answer:** D

**Solution:** Hosted private clouds require organizations to evaluate SLA commitments, legal compliance regarding data location, and network performance because applications now depend on external connectivity.

### 7. In the traditional web services stack, which technology is used to describe a web service's interface — its operations, input/output messages, and how to invoke it?

- A. UDDI
- B. WSDL
- C. SMTP
- D. HTML

**Correct Answer:** B

**Solution:** WSDL is an XML-based language that describes a web service's interface: its operations, message formats, and binding/invocation details. UDDI is the registry used for discovery, SMTP is an email transport protocol, and HTML is a markup language for web pages.

### 8. Traditional SOAP-based web services provide which of the following capabilities?
(i) Platform-independent communication
(ii) XML-based message exchange
(iii) Automatic service discovery through UDDI
(iv) Guaranteed microsecond-level response latency

- A. (i), (ii), and (iii)
- B. (ii) and (iv)
- C. Only (i)
- D. All of the above

**Correct Answer:** A

**Solution:** SOAP web services promote interoperability using XML and WSDL and support service discovery through UDDI. They do not guarantee extremely low-latency communication because XML processing introduces overhead.

### 9. Which of the following problems are effectively addressed by traditional web services, and which are NOT?
(i) Passing through firewalls using standard HTTP/HTTPS
(ii) Enabling interoperability across different programming languages and operating systems
(iii) Ultra-low-latency, real-time inter-service communication
(iv) Service discovery through registries like UDDI

- A. Only (i) and (ii) are addressed
- B. (i), (ii), and (iv) are addressed; (iii) is NOT addressed
- C. Only (ii) is addressed
- D. All are addressed

**Correct Answer:** B

**Solution:** Traditional web services address firewall transparency by using HTTP/HTTPS, ensure platform and language interoperability via XML, SOAP, and WSDL, and support service discovery through registries like UDDI. However, they do not provide ultra-low-latency, real-time communication, as XML parsing and SOAP overhead introduce delays, making modern alternatives like gRPC better suited for real-time scenarios.

### 10. In the Service-Oriented Architecture (SOA) model, which set of operations correctly maps the interactions among the service provider, service registry, and service requestor?

- A. Publish (provider → registry), Find (requestor → registry), Bind (requestor → provider)
- B. Publish (requestor → provider), Find (provider → registry), Bind (registry → requestor)
- C. Bind (provider → registry), Publish (requestor → registry), Find (provider → requestor)
- D. Find (provider → registry), Publish (requestor → registry), Bind (provider → provider)

**Correct Answer:** A

**Solution:** In SOA, the provider publishes its service description to the registry, the requestor finds a suitable service by querying the registry, and the requestor then binds to and invokes the provider directly. This publish–find–bind triangle defines the interactions among the three roles.
## Week 3
### 1. Which of the following is least likely to be specified in an operational cloud Service Level Agreement(SLA)?

- A. Recovery Time Objective (RTO)
- B. Exact encryption algorithm and key storage procedures
- C. Mean Time To Repair (MTTR) for incidents
- D. Penalty / credit calculation for downtime

**Correct Answer:** B

**Solution:** SLAs describe service-level commitments (RTO, MTTR, penalties); low-level implementation/security procedures (exact algorithms/key storage) belong in security/operational documents, not the SLA.

### 2. A multilevel SLA generally consists of which of the following levels?
(i) Corporate Level
(ii) Customer Level
(iii) Service Level

- A. Only (i)
- B. (i) and (ii)
- C. (ii) and (iii)
- D. (i), (ii), and (iii)

**Correct Answer:** D

**Solution:** A multilevel SLA typically consists of corporate-level commitments applicable to all customers, customer-level agreements tailored to specific clients, and service-level agreements defining guarantees for individual services.

### 3. An enterprise signs a three-tier multilevel SLA with a cloud provider. However, the corporate-level SLA guarantees 95% uptime, the customer-level SLA specifies 98% uptime, and the service-level SLA guarantees 99.9% uptime. In case of a service disruption, which level of SLA is the provider LEGALLY BOUND to honor?

- A. Corporate-level SLA, as it's the broadest agreement
- B. Customer-level SLA, as it's the middle ground
- C. Service-level SLA, as it's the most specific agreement
- D. The provider can choose the lowest applicable SLA

**Correct Answer:** C

**Solution:** Multilevel SLAs are structured hierarchically. The service-level SLA is the most granular and specific to the actual service delivery and is legally binding. If there's a conflict, the highest level of commitment (service-level SLA at 99.9%) applies. Corporate and customer-level SLAs provide broader guarantees, but disputes are typically resolved at the service-level SLA because that's where accountability directly lies with the provider's infrastructure.

### 4. Which pair of metrics is most directly used to quantify the reliability and recoverability commitments in a cloud SLA?

- A. Availability (uptime %) and Mean Time To Recovery (MTTR)
- B. Lines of code and number of microservices
- C. Number of employees and office locations
- D. CPU clock speed and RAM size of the servers

**Correct Answer:** A

**Solution:** Availability (uptime percentage) captures reliability, and Mean Time To Recovery (MTTR) captures how quickly the service is restored after an incident. The other options are organizational or low-level implementation details, not SLA commitments.

### 5. A cloud service guarantees 99.9% availability per 30-day month. What is the maximum allowable downtime in that month under the SLA? (Assume 30 days = 720 hours.)

- A. About 0.72 hours
- B. About 7.2 hours
- C. About 3.6 hours
- D. About 72 minutes

**Correct Answer:** A

**Solution:** Allowed downtime = (1 − 0.999) × 720 hours = 0.001 × 720 = 0.72 hours ≈ 43 minutes per month.

### 6. Which feature primarily enables a parallel database to process large analytical queries faster than a traditional database?

- A. Exclusive use of SQL
- B. Distributed query execution across multiple computing nodes
- C. Elimination of indexing
- D. Storing all data in a single server

**Correct Answer:** B

**Solution:** Parallel databases partition data and execute query operations across multiple nodes simultaneously, significantly improving analytical performance.

### 7. You are building a fraud-detection pipeline that must flag suspicious transactions within a few hundred milliseconds as they arrive. The system must:

Ingest about 500,000 transactions per second

Detect and alert within sub-second latency

Apply per-transaction rules and short sliding-window aggregations
Which architectural choice is LEAST suitable?

- A. Apache Kafka feeding Apache Flink for continuous stream processing
- B. Amazon Kinesis with a real-time stream-processing application
- C. A nightly batch job on a data warehouse that scans the day's transactions
- D. Apache Pulsar with a stream processor for windowed aggregation

**Correct Answer:** C

**Solution:** A nightly batch job introduces hours of latency and cannot meet a sub-second, real-time detection requirement. Kafka + Flink, Kinesis real-time applications, and Pulsar + stream processors are all designed for low-latency continuous stream processing and are suitable here.

### 8. A company stores petabytes of satellite imagery that must be processed in parallel by Spark clusters. Which storage system is most suitable?

- A. Local SSD attached to a single virtual machine
- B. Object storage such as Amazon S3 or Google Cloud Storage
- C. Relational database server
- D. Client-side browser cache

**Correct Answer:** B

**Solution:** Cloud object storage provides virtually unlimited scalability, durability, and seamless integration with distributed processing frameworks like Spark and Hadoop.

### 9. A MapReduce job is designed to count word frequencies in 2 TB of text files. The mapper output is 1.5 TB (including overhead), and after the shuffle and sort phase, the data is 1.3 TB. During the reduce phase, a node runs out of disk space during the merge operation. Which of the following is the most likely cause and solution?

- A. The mapper logic is inefficient; rewrite the mapper function
- B. The combiner phase didn't run; ensure combiner is explicitly configured to compress intermediate data locally
- C. The shuffle and sort didn't deduplicate keys; increase the number of reducers
- D. The network bandwidth is saturated; add more nodes to the cluster

**Correct Answer:** B

**Solution:** The combiner is a key MapReduce optimization that runs locally on each mapper node after the map phase, pre-aggregating intermediate key-value pairs to reduce their volume before shuffling. In a word count job, for example, it can sum occurrences of each word on the mapper node, potentially shrinking 1.5 TB of mapper output to 400–500 GB. Without a combiner, all intermediate data is sent to the reducers, which can overwhelm disk space during the merge phase. By explicitly configuring a combiner, the amount of data transferred across the network and merged by reducers is greatly reduced, preventing disk exhaustion and improving overall job efficiency.

### 10. An OpenStack compute node contains 640 physical vCPUs. If the CPU allocation ratio is 5:1, what is the maximum number of virtual CPUs that may be allocated?

- A. 3000
- B. 3200
- C. 3400
- D. 3500

**Correct Answer:** B

**Solution:** Total allocatable vCPUs = Physical vCPUs × Allocation Ratio = 640 × 5 = 3200 vCPUs
## Week 4
### 1. Which Azure SQL Database service tier separates compute and storage so that storage can automatically grow up to 100 TB without requiring application downtime?

- A. Basic
- B. Business Critical
- C. Hyperscale
- D. Standard

**Correct Answer:** C

**Solution:** The Hyperscale tier decouples compute and storage, allowing storage to automatically scale up to 100 TB. It is intended for very large databases and supports rapid scaling and fast backup/restore operations.

### 2. One company deploys two Azure Virtual Machines in different Availability Zones within the same Azure region. One data center experiences a complete power outage. Which statement is correct?

- A. Both VMs will become unavailable because they are in the same region.
- B. The second VM can continue running because Availability Zones are isolated from each other.
- C. Azure automatically moves the failed VM to another region.
- D. Both VMs share the same cooling and networking infrastructure.

**Correct Answer:** B

**Solution:** Availability Zones are physically separate data centers within the same Azure region, each with independent power, cooling, and networking. If one zone fails, resources in another zone continue to operate.

### 3. Which App Service pricing tier supports the highest number of deployment slots?

- A. Basic
- B. Standard
- C. Premium (P1v3 and higher)
- D. Free

**Correct Answer:** C

**Solution:** The Premium (P1v3 and higher) App Service plan supports up to 20 deployment slots, making it suitable for advanced DevOps and CI/CD scenarios.

### 4. An administrator notices that users can still access an Azure App Service website using http://. Which App Service configuration should be enabled to prevent unencrypted access?

- A. Managed Identity
- B. Always On
- C. HTTPS Only
- D. Deployment Slots

**Correct Answer:** C

**Solution:** Enabling HTTPS Only forces all incoming HTTP requests to be redirected to HTTPS, preventing unencrypted communication.

### 5. Which Google Cloud database service is designed specifically for structured relational data with global consistency and horizontal scalability?

- A. Firestore
- B. Cloud SQL
- C. Cloud Spanner
- D. Memorystore

**Correct Answer:** C

**Solution:** Cloud Spanner is a globally distributed relational database that combines SQL support, horizontal scalability, and strong consistency. Firestore is NoSQL, Cloud SQL scales primarily vertically, and Memorystore is an in-memory cache.

### 6. A virtual machine requires an additional 100 GB persistent disk that should remain intact even after the VM is terminated. Which OpenStack service manages this storage?

- A. Nova
- B. Swift
- C. Cinder
- D. Keystone

**Correct Answer:** C

**Solution:** Cinder provides persistent block storage volumes independent of the VM lifecycle. If the VM is deleted, the Cinder volume remains unless explicitly removed.

### 7. Which statement correctly distinguishes GKE from Cloud Run?

- A. GKE only supports virtual machines.
- B. Cloud Run requires users to manage Kubernetes clusters.
- C. GKE manages Kubernetes clusters, while Cloud Run executes containers without requiring cluster management.
- D. Both services require manual Kubernetes control plane management.

**Correct Answer:** C

**Solution:** GKE is a managed Kubernetes service, whereas Cloud Run is a serverless container platform where Google manages the underlying infrastructure and scaling.

### 8. A company collects millions of IoT sensor events every minute. The data must be ingested in real time, stored in a scalable analytical warehouse, and visualized through interactive dashboards. Which GCP architecture best satisfies these requirements?

- A. Cloud SQL + Cloud Functions + Looker
- B. Pub/Sub + BigQuery + Looker Studio
- C. Firestore + Compute Engine + Bigtable
- D. Cloud Storage + Memorystore + App Engine

**Correct Answer:** B

**Solution:** Pub/Sub provides scalable real-time event ingestion. BigQuery stores petabyte-scale analytical data and supports SQL queries. Looker Studio connects directly to BigQuery for dashboards and reports. Firestore is operational NoSQL storage, while Cloud SQL is not suitable for high-volume analytics.

### 9. A DevOps engineer wants to route all production traffic to version v3 of an App Engine service. Which command is correct?

- A. gcloud app services set-traffic default --splits=v3=1
- B. gcloud app deploy --traffic=v3
- C. gcloud app versions promote v3
- D. gcloud app services update v3

**Correct Answer:** A

**Solution:** Setting the split to v3=1 directs 100% of traffic to version v3.

### 10. Which OpenStack service is primarily responsible for routing tenant traffic between internal and external networks?

- A. Nova
- B. Neutron
- C. Keystone
- D. Swift

**Correct Answer:** B

**Solution:** Neutron provides networking services, including virtual networks, routers, DHCP, security groups, and floating IPs.
## Week 5
### 1. A cloud provider guarantees 99% availability. A customer's application operates 12 hours per day. What is the maximum allowable downtime during a 30-day month without violating the SLA?

- A. 3.6 hours
- B. 6 hours
- C. 7.2 hours
- D. 9 hours

**Correct Answer:** A

**Solution:** Scheduled time 12×30=360 hours. Allowed downtime : 1%=0.01×360=3.6 hours.

### 2. A cloud server dynamically activates additional CPU cores to handle a sudden spike in user requests. What is the most likely impact on the server's power consumption?

- A. Power consumption decreases because the workload is distributed.
- B. Power consumption remains unchanged since CPU frequency is fixed.
- C. Power consumption increases as additional CPU cores become active.
- D. Power consumption depends only on the amount of RAM used.

**Correct Answer:** C

**Solution:** Activating more CPU cores increases overall power consumption because each active core consumes power. Although techniques such as Dynamic Voltage and Frequency Scaling (DVFS) can improve energy efficiency, the total power generally increases as more cores are utilized.

### 3. Which cloud characteristic most directly helps organizations avoid large upfront hardware investments?

- A. Elastic scalability
- B. Pay-as-you-go pricing
- C. Fault tolerance
- D. Multi-tenancy

**Correct Answer:** B

**Solution:** Pay-as-you-go pricing allows customers to pay only for consumed resources, eliminating the need for significant upfront hardware purchases.

### 4. An HDFS cluster has a block size of 128 MB. A 700 MB input file is processed using MapReduce. Assuming one map task per HDFS block, how many map tasks are created?

- A. 5
- B. 6
- C. 7
- D. 8

**Correct Answer:** B

**Solution:** Blocks 700 MB = 128 + 128 + 128 + 128 + 128 + 60 = 6 blocks. One mapper per block so 6 map tasks.

### 5. Which virtualization component is primarily responsible for creating and managing virtual machines?

- A. Operating System Kernel
- B. Hypervisor
- C. BIOS
- D. Device Driver

**Correct Answer:** B

**Solution:** A hypervisor (Virtual Machine Monitor) creates, runs, and manages virtual machines by abstracting the underlying physical hardware.

### 6. Which MapReduce component determines which Reducer receives a particular key?

- A. Combiner
- B. Partitioner
- C. RecordWriter
- D. InputSplit

**Correct Answer:** B

**Solution:** The Partitioner determines the destination Reducer for each intermediate key. By default, Hadoop uses a hash-based partitioner to distribute keys among Reducers.

### 7. Which MapReduce component is optional and may execute zero, one, or multiple times?

- A. Mapper
- B. Reducer
- C. Combiner
- D. RecordReader

**Correct Answer:** C

**Solution:** The Combiner is an optional optimization. Hadoop does not guarantee that it will execute, so algorithms must remain correct even if the Combiner is skipped.

### 8. A cloud provider observes that many physical servers are running at only 15% CPU utilization. To reduce electricity costs, it migrates virtual machines onto fewer servers and powers off the idle hosts while ensuring that application performance remains within SLA limits. Which scheduling strategy is being applied?

- A. Round-Robin Scheduling
- B. Energy-Aware Scheduling
- C. First-Come-First-Serve Scheduling
- D. Fair Scheduling

**Correct Answer:** B

**Solution:** Energy-aware scheduling consolidates workloads onto fewer physical machines, allowing unused servers to be switched to low-power or off states. This reduces energy consumption while maintaining the required Quality of Service (QoS).

### 9. Statement 1: Elasticity enables cloud users to increase or decrease resources according to workload demand.
Statement 2: Elasticity helps organizations avoid paying for unused computing resources.

- A. Both statements are true.
- B. Both statements are false.
- C. Statement 1 is true and Statement 2 is false.
- D. Statement 1 is false and Statement 2 is true.

**Correct Answer:** A

**Solution:** Elasticity allows resources to scale dynamically. Since resources can be released when demand decreases, organizations avoid paying for idle infrastructure.

### 10. Average demand = 75 units, Peak demand = 225 units, The cloud provider offers a utility premium of 2.8. Which statement is true?

- A. Cloud cost < Owning cost
- B. Cloud cost > Owning cost
- C. Both costs are equal
- D. None of the above

**Correct Answer:** A

**Solution:** Maximum premium 225/75=3. Since 2.8<3. Cloud remains cheaper.
## Week 6
### 1. A database stores customer records in encrypted form. However, an administrator accidentally changes several account balances due to a software bug. Which security objective has failed?

- A. Confidentiality only
- B. Integrity only
- C. Availability only
- D. Confidentiality and Availability

**Correct Answer:** B

**Solution:** Encryption protects confidentiality but does not prevent authorized users or software from incorrectly modifying data. The erroneous modification violates integrity.

### 2. An employee logs into a fake VPN portal that perfectly imitates the company's official login page. Before any credentials are entered, which security property has already been compromised?

- A. Confidentiality
- B. Integrity
- C. Availability
- D. Authenticity

**Correct Answer:** D

**Solution:** The fake portal falsely claims to be the legitimate VPN service. The attack exploits authenticity before any confidential information is disclosed.

### 3. Which of the following attacks is NOT considered a passive attack?

- A. Packet sniffing
- B. Traffic analysis
- C. Session hijacking
- D. Network monitoring

**Correct Answer:** C

**Solution:** Session hijacking allows an attacker to take over an active communication session by injecting or modifying packets. Since it alters the communication, it is an active attack. Packet sniffing, traffic analysis, and network monitoring only observe communications without altering them and are therefore passive attacks.

### 4. Which of the following attacks cannot directly modify the contents of transmitted data?

- A. Replay attack
- B. Man-in-the-Middle attack
- C. Eavesdropping
- D. Masquerading

**Correct Answer:** C

**Solution:** Eavesdropping only captures data being transmitted and does not modify or inject messages. Hence, it is a passive attack.

### 5. Which of the following best describes a Denial-of-Service (DoS) attack?

- A. An attacker secretly monitors network traffic without modifying it.
- B. An attacker floods a server with excessive requests, making the service unavailable to legitimate users.
- C. An attacker impersonates a legitimate user to gain unauthorized access.
- D. An attacker modifies data during transmission between two communicating parties.

**Correct Answer:** B

**Solution:** A Denial-of-Service (DoS) attack attempts to make a service or resource unavailable by overwhelming it with excessive traffic or resource requests. This is an active attack because it interferes with the normal operation of the system.

### 6. Which of the following activities is least likely to be considered part of the reconnaissance phase?

- A. Performing DNS enumeration to identify subdomains
- B. Scanning the target to discover open ports and running services
- C. Exploiting a buffer overflow vulnerability to gain administrator privileges
- D. Searching public websites and social media for organizational information

**Correct Answer:** C

**Solution:** Reconnaissance involves gathering information about the target using passive or active techniques. DNS enumeration, port scanning, and Open-Source Intelligence (OSINT) are common reconnaissance activities. Exploiting a buffer overflow is part of the exploitation (attack) phase, not reconnaissance.

### 7. Statement I: Authentication determines whether a user is allowed to access a resource.
Statement II: Authorization determines what actions an authenticated user is permitted to perform.

- A. Statement I is TRUE and Statement II is FALSE.
- B. Statement I is FALSE and Statement II is TRUE.
- C. Both statements are TRUE.
- D. Both statements are FALSE.

**Correct Answer:** B

**Solution:** Authentication verifies who the user is, whereas authorization determines what that authenticated user is allowed to do.

### 8. A financial institution must install a custom Linux kernel module, configure firewall rules at the operating system level, and deploy proprietary database software. However, it does not want to purchase or maintain physical servers. Which cloud service model is most appropriate?

- A. SaaS
- B. PaaS
- C. IaaS
- D. FaaS

**Correct Answer:** C

**Solution:** The organization requires control over the operating system and installed software, which is available in IaaS. The cloud provider manages the underlying physical infrastructure, while the customer manages the OS, middleware, and applications.

### 9. An organization discovers that backups of its confidential data are automatically replicated to another country without its knowledge. Which cloud security concern has been violated?

- A. Data Location
- B. Recovery
- C. Virtualization
- D. Resource Pooling

**Correct Answer:** A

**Solution:** Automatic replication across geographic regions may violate legal or organizational requirements governing where sensitive data is stored.

### 10. Which of the following cloud design practices is most effective in reducing vendor lock-in?

- A. Using provider-specific APIs whenever possible
- B. Developing applications using open standards and portable technologies
- C. Storing data only in proprietary database formats
- D. Relying exclusively on managed proprietary services

**Correct Answer:** B

**Solution:** Open standards, containerization, and portable technologies reduce dependence on any single provider and simplify migration.
## Week 7
### 1. Which of the following applications is least suitable for computation offloading to a remote cloud in Mobile Cloud Computing (MCC)?

- A. Image rendering requiring intensive GPU computation
- B. Large-scale machine learning inference
- C. Emergency collision avoidance requiring millisecond response
- D. Video transcoding

**Correct Answer:** C

**Solution:** Safety-critical real-time applications require extremely low latency. Network delays and connectivity uncertainty make cloud execution unsuitable. Such tasks are better handled locally or at nearby edge/fog nodes.

### 2. A cloud-based mobile application automatically allocates additional computing resources during a sudden surge in users and releases them when demand decreases. Which cloud characteristic is demonstrated?

- A. Resource pooling
- B. Rapid elasticity
- C. Location independence
- D. Broad network access

**Correct Answer:** B

**Solution:** Rapid elasticity enables cloud resources to scale up or down automatically according to workload, ensuring efficient resource utilization and performance.

### 3. Dynamic computation offloading primarily aims to optimize which combination of objectives?

- A. Screen brightness and storage capacity
- B. Execution time, energy consumption, and resource utilization
- C. Camera quality and display refresh rate
- D. Cloud subscription cost only

**Correct Answer:** B

**Solution:** Dynamic offloading balances performance and energy by considering execution delay, battery consumption, CPU utilization, and network conditions.

### 4. A mobile augmented reality application requires object recognition with an end-to-end response time below 20 ms. Which infrastructure is most appropriate?

- A. A geographically distant public cloud data center
- B. A nearby cloudlet connected through a high-speed local network
- C. Local storage only
- D. An offline mobile application

**Correct Answer:** B

**Solution:** Augmented reality applications are highly latency-sensitive. A nearby cloudlet minimizes communication delay and provides computational resources close to the user, unlike a remote cloud.

### 5. A healthcare application stores patient records in the cloud. Which security requirement is most critical to ensure that unauthorized users cannot access sensitive medical information?

- A. Elasticity
- B. Data confidentiality
- C. Resource pooling
- D. Load balancing

**Correct Answer:** B

**Solution:** Medical records contain sensitive information. Confidentiality ensures that only authorized individuals can access the data.

### 6. Which limitation of traditional cloud computing is primarily addressed by fog computing?

- A. Limited virtualization support
- B. High network latency caused by distant cloud data centers
- C. Lack of cloud storage
- D. Insufficient computing power in cloud servers

**Correct Answer:** B

**Solution:** Fog computing places computational resources closer to end devices, minimizing the delay associated with transmitting data to distant cloud data centers.

### 7. Which statement about fog nodes is FALSE?

- A. They may perform filtering and aggregation of sensor data.
- B. They are usually located close to IoT devices.
- C. They permanently store all enterprise data.
- D. They reduce communication with distant cloud servers.

**Correct Answer:** C

**Solution:** Fog nodes mainly perform temporary processing and short-term storage. Long-term storage is generally handled by cloud data centers.

### 8. Statement 1: Geospatial Cloud Computing enables parallel processing of massive satellite imagery by distributing computation across multiple cloud nodes.
Statement 2: Distributed storage and parallel processing frameworks reduce execution time for large geospatial datasets compared with a single desktop workstation.

- A. Both Statement 1 and Statement 2 are true, and Statement 2 is the correct explanation of Statement 1
- B. Both Statement 1 and Statement 2 are true, but Statement 2 is not the correct explanation of Statement 1
- C. Statement 1 is true, but Statement 2 is false
- D. Statement 1 is false, but Statement 2 is true

**Correct Answer:** A

**Solution:** Distributed storage and parallel computation are the fundamental reasons cloud platforms efficiently process massive geospatial datasets.

### 9. A cloud platform divides a large raster image into tiles for parallel processing. Which challenge must be carefully addressed to ensure accurate results?

- A. Screen resolution of client devices
- B. Boundary effects between adjacent image tiles
- C. Keyboard input latency
- D. Number of GIS users

**Correct Answer:** B

**Solution:** Many raster operations (e.g., filtering, convolution, terrain analysis) require neighboring pixels. Partitioning into tiles can introduce boundary effects unless overlap or edge handling is implemented.

### 10. A wearable ECG sensor continuously streams a patient's heart signals. Which architecture is most appropriate to detect cardiac abnormalities within a few milliseconds?

- A. IoT sensors → Remote Cloud → Physician
- B. IoT sensors → Fog/Edge Node → Cloud
- C. IoT sensors → Local Storage → Weekly Upload
- D. IoT sensors → FTP Server → Desktop GIS

**Correct Answer:** B

**Solution:** Delay-sensitive healthcare applications require immediate processing at nearby fog/edge nodes. The cloud is mainly used for long-term storage, historical analysis, and model training.
## Week 8

### 1. Which command is used to remove a Docker image that is no longer required?

- A. docker rm
- B. docker rmi
- C. docker delete
- D. docker remove

**Correct Answer:** B

**Solution:** docker rmi removes one or more Docker images from the local system. docker rm is used to remove containers, not images.

### 2. Which Docker command is primarily used to list all available Docker networks?

- A. docker network ls
- B. docker network show
- C. docker net ps
- D. docker networks

**Correct Answer:** A

**Solution:** docker network ls displays all Docker networks available on the host. It shows information such as network ID, name, driver, and scope.

### 3. Which of the following is the most accurate comparison between VMs and containers?

- A. VMs share the host kernel, while containers have separate kernels
- B. Containers generally share the host kernel, while VMs virtualize hardware and run separate guest OS kernels
- C. Both always require separate guest operating systems
- D. Containers require more resources than VMs because they include a complete OS

**Correct Answer:** B

**Solution:** A VM typically includes a complete guest OS and its own kernel, operating on virtualized hardware. Containers share the host kernel and isolate applications at the operating- system level, making them generally lighter than VMs.

### 4. What is the primary role of etcd in a Kubernetes cluster?

- A. Running application containers
- B. Storing Kubernetes cluster state and configuration data
- C. Scheduling Pods onto Nodes
- D. Providing container images

**Correct Answer:** B

**Solution:** etcd is a distributed key-value store used by Kubernetes to persist important cluster state, configuration, and metadata. The Kubernetes control plane relies on it as its backing data store.

### 5. Which of the following is an example of a Type 2 (hosted) hypervisor?

- A. VMware ESXi
- B. Xen
- C. Oracle VirtualBox
- D. Microsoft Hyper-V Server

**Correct Answer:** C

**Solution:** Oracle VirtualBox is a Type 2 hypervisor because it runs as an application on top of an existing host operating system. VMware ESXi and Xen are examples of Type 1 hypervisors.

### 6. A cloud data center has 100 physical servers, but only 40 are heavily utilized while the remaining servers operate at very low utilization. Which strategy would MOST effectively reduce energy consumption?

- A. Distribute VMs equally across all 100 servers
- B. Consolidate VMs onto fewer servers and switch idle servers to a low-power state
- C. Increase CPU frequency on all servers
- D. Duplicate every VM across multiple servers

**Correct Answer:** B

**Solution:** VM consolidation migrates workloads from lightly loaded servers onto fewer physical machines. Underutilized servers can then be switched to sleep or power-off states, reducing unnecessary energy consumption.

### 7. In a Sensor Cloud environment, why is a middleware layer often required between Wireless Sensor Networks (WSNs) and cloud services?

- A. To increase the physical size of sensor nodes
- B. To abstract heterogeneous sensors and provide cloud-accessible sensor resources
- C. To eliminate all communication between sensors
- D. To replace the sensing function of WSN nodes

**Correct Answer:** B

**Solution:** A middleware layer provides an abstraction between resource-constrained, heterogeneous sensor networks and cloud platforms. It can handle resource discovery, data collection, protocol translation, virtualization/abstraction, and service management, allowing cloud applications to access sensor resources more conveniently.

### 8. Which architecture is generally BEST suited for applications requiring both low latency and large- scale cloud analytics?

- A. IoT Device → Cloud only
- B. IoT Device → Edge/Fog → Cloud
- C. IoT Device → Database only
- D. IoT Device → Hypervisor → Cloud

**Correct Answer:** B

**Solution:** An Edge/Fog–Cloud architecture combines local processing for latency- sensitive tasks with cloud resources for large-scale storage, historical analysis, and computationally intensive workloads.

### 9. An IoT application sends sensitive sensor data through public networks to a cloud platform. Which mechanism is MOST important for protecting the data during transmission?

- A. Data encryption
- B. Increasing CPU frequency
- C. Increasing sensor sampling rate
- D. VM consolidation

**Correct Answer:** A

**Solution:** Encryption protects data while it travels between IoT devices, gateways, and cloud services. Secure communication protocols such as TLS can help prevent unauthorized parties from reading or modifying data in transit.

### 10. Statement 1: Processing latency-sensitive IoT workloads at an edge node can reduce the communication delay associated with a distant cloud.

Statement 2: Edge processing eliminates all network latency because no communication is required.

- A. Statement 1 is True and Statement 2 is False
- B. Statement 2 is True and Statement 1 is False
- C. Both statements are True
- D. Both statements are False

**Correct Answer:** A

**Solution:** Edge computing reduces latency by moving processing closer to the data source, but some communication latency still exists. Therefore, it does not eliminate network latency completely.

## Week 9
### 1. A factory requires machine-level anomaly detection within milliseconds, but it also needs to aggregate data from multiple machines for plant-wide analysis before sending summaries to the cloud. Which placement BEST matches the requirements?

- A. All processing in the centralized cloud
- B. Machine-level processing at the edge and plant-level processing at fog nodes
- C. All processing directly on individual sensors
- D. Plant-wide processing exclusively at the cloud

**Correct Answer:** B

**Solution:** Edge computing is appropriate for extremely latency-sensitive processing close to individual machines. Fog computing provides an intermediate layer capable of aggregating and analyzing information across multiple edge devices before forwarding relevant data to the cloud.

### 2. A smart-city traffic system receives video streams from hundreds of cameras. Immediate object detection is performed near each camera, regional congestion patterns are analyzed at roadside micro-data centers, and long-term traffic trends are analyzed in the cloud. Which architecture BEST represents this system?

- A. Cloud-only architecture
- B. Fog-only architecture
- C. Edge–Fog–Cloud architecture
- D. Edge-only architecture

**Correct Answer:** C

**Solution:** The architecture uses Edge Computing for immediate processing near individual cameras, Fog Computing for regional aggregation and coordination, and Cloud Computing for large-scale historical analytics and storage. Therefore, the complete architecture is Edge–Fog–Cloud.

### 3. An IoT system performs local filtering before forwarding data to the cloud. Which ordering BEST represents the typical amount of raw data transmitted toward centralized cloud infrastructure, from lowest to highest?

- A. Edge processing → Fog processing → Cloud-only processing
- B. Cloud-only processing → Fog processing → Edge processing
- C. Fog processing → Cloud-only processing → Edge processing
- D. Edge processing → Cloud-only processing → Fog processing

**Correct Answer:** A

**Solution:** When processing occurs at the edge, unnecessary data can be filtered before transmission. Fog processing can also aggregate data regionally. In a cloud-only approach, much more raw data may need to travel to centralized infrastructure.

### 4. A fog node is running out of memory, but the infrastructure allows additional RAM and CPU resources to be assigned to that same node. Which scalability approach is being used?

- A. Horizontal scalability
- B. Temporal scalability
- C. Geographic scalability
- D. Vertical scalability

**Correct Answer:** D

**Solution:** Vertical scalability (scale-up) increases the resources of an existing node, such as CPU, RAM, or storage. Horizontal scalability, in contrast, adds additional nodes.

### 5. Which statement BEST describes the division of responsibilities in a hierarchical Edge–Fog–Cloud architecture?

- A. Edge handles global optimization, while Cloud handles sensor-level decisions
- B. Edge handles immediate local actions, Fog coordinates regional resources, and Cloud performs global orchestration
- C. All three layers perform exactly the same tasks
- D. Only the Cloud is allowed to make decisions

**Correct Answer:** B

**Solution:** A hierarchical architecture distributes decision-making according to proximity and scope: Edge → immediate local decisions, Fog → regional coordination and resource management, Cloud → global policies, optimization, and long-term analytics.

### 6. A video analytics application requires its first-stage processing to occur within 10 ms of the camera, while its model-training component requires substantial computational resources. Which placement is MOST appropriate?

- A. Both components on a distant cloud server
- B. Both components on the smallest IoT device
- C. First-stage processing at the edge and model training in the cloud
- D. First-stage processing only in the cloud and training at the edge

**Correct Answer:** C

**Solution:** The latency-sensitive component should be placed close to the camera at the edge, while computationally intensive model training can be performed in the cloud, where greater computational resources are available.

### 7. A mobile device is moving rapidly between coverage areas of different edge servers while executing an offloaded task. Which issue becomes MOST critical?

- A. Static CPU allocation
- B. Service migration and task continuity during handover
- C. Cloud storage capacity
- D. VM image size only

**Correct Answer:** B

**Solution:** High mobility can cause a device to move from one edge server's coverage area to another. Maintaining service continuity may require task migration, service migration, or intelligent reassignment, while minimizing interruption and migration overhead.

### 8. A cloud application requires additional resources because its primary CSP has insufficient capacity. A broker identifies a suitable secondary CSP and negotiates the required service conditions. Which cloud-federation function is being performed?

- A. Resource federation and inter-provider service provisioning
- B. VM deletion within a single CSP
- C. Local container orchestration
- D. Hardware virtualization

**Correct Answer:** A

**Solution:** In a cloud federation, a broker can discover resources from multiple CSPs and coordinate resource provisioning across providers. This enables an application to obtain additional capacity without depending entirely on a single provider.

### 9. Why is trust management particularly important in a cloud federation?

- A. Resources and services may be obtained from independent providers with different security and reliability policies
- B. All CSPs are automatically controlled by the same organization
- C. Federation eliminates authentication requirements
- D. Trust is required only for physical servers

**Correct Answer:** A

**Solution:** Federated clouds involve independent CSPs, so providers may have different security practices, compliance requirements, reliability levels, and policies. Establishing trust and verifying provider behaviour is therefore critical.

### 10. Which is the PRIMARY advantage of a Hybrid Cloud Federation for an organization handling sensitive workloads?

- A. It eliminates the need for security controls
- B. It forces all workloads into the public cloud
- C. It combines private-cloud control for sensitive workloads with public-cloud scalability
- D. It prevents workload migration between environments

**Correct Answer:** C

**Solution:** Hybrid federation provides a balance between security, control, compliance, and scalability. Sensitive applications can remain in private infrastructure, while less-sensitive or burst workloads can utilize public-cloud resources.

## Week 10
### 1. During live migration of a VM, which condition is most likely to increase the total migration time?
- A. Low rate of memory-page modification by the VM
- B. High rate of memory-page modification during migration
- C. Increasing the number of CPU cores on the destination host
- D. Reducing the VM memory size

**Correct Answer:** B
**Solution:** In live migration, memory pages are copied while the VM continues running. If the VM modifies pages rapidly, many already-transferred pages become dirty and must be copied again. This increases the amount of data transferred and therefore increases migration time.

---

### 2. Which live VM migration technique starts the VM on the destination first and then fetches memory pages from the source on demand as they are accessed?
- A. Cold migration
- B. Pre-copy migration
- C. Post-copy migration
- D. Offline image transfer

**Correct Answer:** C
**Solution:** Post-copy migration resumes the VM on the destination immediately and then pulls memory pages from the source on demand (via page faults) or by background pushing. Pre-copy transfers memory before switching over, while cold and offline transfers require the VM to be stopped first.

---

### 3. Which technique is most likely to reduce the total data transferred (and hence the energy used) during pre-copy live migration?
- A. Increasing the memory-dirtying rate of the workload
- B. Compressing and deduplicating memory pages before transfer
- C. Adding more iterative pre-copy rounds indefinitely
- D. Disabling dirty-page tracking

**Correct Answer:** B
**Solution:** Memory compression and deduplication cut the volume of data sent over the network, reducing migration time and energy. A higher dirtying rate increases retransmissions, unlimited extra rounds waste bandwidth, and disabling dirty-page tracking breaks pre-copy correctness.

---

### 4. Which resource management strategy is most important to prevent overload when many edge devices send data to nearby fog nodes?
- A. Increasing storage capacity at a single fog node
- B. Static task allocation
- C. Load balancing across fog nodes
- D. Sending all data directly to the cloud

**Correct Answer:** C
**Solution:** When many edge devices send data, one fog node can become overloaded. Static allocation or just adding storage doesn’t handle changing workloads well. Load balancing spreads tasks across multiple fog nodes, avoiding congestion and keeping latency low. Sending all data to the cloud increases delay and bandwidth use, defeating the purpose of fog computing.

---

### 5. A Kubernetes cluster has several worker nodes. A newly created Pod must be assigned to an appropriate node based on available resources and scheduling constraints. Which Kubernetes component is primarily responsible for this decision?
- A. kubelet
- B. kube-scheduler
- C. kube-proxy
- D. Container registry

**Correct Answer:** B
**Solution:** The kube-scheduler selects an appropriate worker node for newly created Pods. It considers factors such as resource requirements, node availability, affinity rules, and scheduling constraints. The kubelet subsequently manages the Pod on the selected node.

---

### 6. Consider the following Docker workflow:
Dockerfile → docker build → ______ → docker run
Which entity is produced by the docker build operation?
- A. Docker volume
- B. Docker image
- C. Running container
- D. Kubernetes Pod

**Correct Answer:** B
**Solution:** The docker build command processes instructions in a Dockerfile and creates a Docker image. A container is subsequently created from an image when docker run is executed.

---

### 7. Which of the following correctly describes the roles of Linux namespaces and cgroups in containers?
- A. Namespaces provide resource quotas, while cgroups provide process isolation.
- B. Namespaces provide isolation of processes and system resources, while cgroups control resource usage.
- C. Both namespaces and cgroups are used only to create Docker images.
- D. Neither is required for container isolation.

**Correct Answer:** B
**Solution:** Linux namespaces isolate processes and provide separate views of resources such as process IDs, networking, and mount points. cgroups restrict and monitor resource usage such as CPU and memory. Together, they provide important mechanisms for container isolation and resource control.

---

### 8. A VM has 32 GB of memory and the migration link provides 16 MB/sec of usable throughput. For a non-live (cold) migration where the entire memory is transferred once, what is the approximate transfer time? (Use 1 GB = 2³⁰ bytes, 1 MB = 2²⁰ bytes.)
- A. About 15 minutes
- B. About 34 minutes
- C. About 1 hour
- D. About 2 hours

**Correct Answer:** B
**Solution:** Time = (32 × 2³⁰) / (16 × 2²⁰) = (32 × 1024) / 16 = 32768 / 16 = 2048 seconds ≈ 34 minutes.

---

### 9. A database container is deleted accidentally. The database files were stored using a Docker named volume rather than only inside the container's writable layer. What happens to the data?
- A. The data is automatically deleted with the container.
- B. The data remains available in the named volume.
- C. The data is converted into a Docker image.
- D. The data can only be recovered by restarting the deleted container.

**Correct Answer:** B
**Solution:** Docker volumes have a lifecycle independent of individual containers. Deleting a container does not normally delete the data stored in its named volume. This makes volumes appropriate for persistent application data.

---

### 10. Which of the following statements about containers and virtual machines is CORRECT?
- A. Containers normally require a separate complete guest operating system for every application.
- B. Virtual machines and containers always provide identical levels of isolation.
- C. Containers generally share the host operating system kernel, whereas VMs virtualize a complete machine environment.
- D. Containers cannot be deployed on virtual machines.

**Correct Answer:** C
**Solution:** Containers share the host OS kernel and therefore generally require fewer resources and start faster. A virtual machine provides a virtualized hardware environment in which a separate guest operating system runs. Containers can also run inside virtual machines, so option D is incorrect.

## Week 11
### 1. Which capability is the defining feature of Dew computing compared to conventional cloud computing?
- A. It requires a permanent high-bandwidth connection to the cloud
- B. It provides local independence, letting a device store and process data offline and sync with the cloud when connectivity returns
- C. It eliminates the need for any cloud component
- D. It performs only data storage and never computation

**Correct Answer:** B
**Solution:** Dew computing's defining feature is local independence with later synchronization — devices keep working offline and reconcile with the cloud once reconnected. It complements rather than replaces the cloud, and supports both storage and computation.

---

### 2. A weather-monitoring device installed in a remote mountain region must continue recording and processing measurements for several hours even when the Internet connection is unavailable. Once connectivity is restored, the accumulated data is synchronized with a cloud server. Which computing paradigm best matches this requirement?
- A. Edge computing
- B. Fog computing
- C. Dew computing
- D. Centralized cloud computing

**Correct Answer:** C
**Solution:** Dew computing emphasizes autonomous operation at or near end devices. A dew-enabled device can continue functioning during network outages and synchronize its locally generated data with the cloud when connectivity becomes available.

---

### 3. Two users modify the same record independently while their devices are offline. When both devices reconnect, the cloud detects that the two versions conflict. Which mechanism is most directly required to handle this situation?
- A. CPU scheduling
- B. Conflict detection and resolution during synchronization
- C. Container image creation
- D. Load balancing

**Correct Answer:** B
**Solution:** Independent offline updates can create conflicting versions of the same data. During synchronization, the system must detect these conflicts and apply an appropriate resolution policy to restore a consistent state.

---

### 4. Allowing Dew devices to operate offline and modify data independently most directly introduces which challenge?
- A. Increased CPU virtualization overhead
- B. The need to detect and resolve data conflicts when devices reconnect and synchronize
- C. Permanent loss of all local data
- D. Inability to ever reach the cloud

**Correct Answer:** B
**Solution:** Independent offline modification lets copies of the data diverge, so the main challenge is detecting and resolving conflicts during synchronization to restore consistency — the autonomy-vs-consistency trade-off.

---

### 5. A serverless function has not been invoked for a long period. When the next request arrives, the platform requires additional time to initialize the execution environment. This delay is known as:
- A. Warm start
- B. Cold start
- C. Cache miss
- D. Bootstrapping failure

**Correct Answer:** B
**Solution:** A cold start occurs when the serverless platform needs to create or initialize a new execution environment before processing a request. This initialization introduces additional latency.

---

### 6. Why are serverless functions typically designed to be stateless?
- A. To reduce electricity consumption
- B. Because local storage is unlimited
- C. To allow automatic scaling and parallel execution without dependency conflicts
- D. To avoid using APIs

**Correct Answer:** C
**Solution:** Statelessness ensures each function invocation is independent, allowing the platform to scale horizontally and run multiple instances in parallel without coordination issues.

---

### 7. A team wants to run a batch job that takes about 45 minutes to complete in a single AWS Lambda invocation. Why is this NOT feasible?
- A. Lambda has no internet access
- B. Lambda enforces a maximum execution timeout of 15 minutes per invocation
- C. Lambda cannot process batch data
- D. Lambda functions must always be stateful

**Correct Answer:** B
**Solution:** A single AWS Lambda invocation is capped at 15 minutes (900 seconds), so a 45-minute job cannot finish in one invocation. Such workloads must be split into smaller units or run on a service without this limit (e.g., containers, AWS Batch, or EC2).

---

### 8. A serverless application receives 1,000 independent requests simultaneously. The provider can create multiple function instances to process these requests concurrently. Which property of serverless computing makes this possible?
- A. Stateful execution
- B. Horizontal scalability of independent function invocations
- C. Fixed allocation of one VM per user
- D. Permanent local storage

**Correct Answer:** B
**Solution:** Serverless platforms can automatically create multiple function instances as demand increases. Stateless or independently executable functions are especially suitable for such parallel execution and horizontal scaling.

---

### 9. A research group wants to execute a scientific computation that requires 40 minutes of uninterrupted execution for each task. The chosen FaaS platform imposes a maximum execution time of 15 minutes per invocation. What is the primary problem with using this platform directly?
- A. Functions cannot communicate with databases.
- B. The execution time exceeds the platform's maximum invocation duration.
- C. FaaS cannot process numerical calculations.
- D. Serverless functions cannot execute in parallel.

**Correct Answer:** B
**Solution:** A FaaS platform imposes a maximum execution duration for each invocation. A computation requiring 40 minutes cannot be completed in a single invocation when the platform limit is 15 minutes.

---

### 10. A company needs a managed cloud platform specifically designed for large-scale analytical queries over structured datasets, using distributed processing rather than relying on a single database server. Which service is most appropriate?
- A. Amazon Redshift
- B. Amazon EC2
- C. AWS Lambda
- D. Amazon Route 53

**Correct Answer:** A
**Solution:** Amazon Redshift is a managed cloud data warehouse designed for large-scale analytical workloads. It uses distributed query processing and column-oriented techniques to efficiently analyze large datasets.

## Week 12
### 1. Mobile Cloud Computing (MCC) benefits mobile devices by:

1. Offloading compute-intensive tasks to the cloud
2. Extending effective battery life by reducing on-device processing
3. Guaranteeing zero network latency
4. Providing access to large-scale storage
- A. 1, 2, and 4 only
- B. 1 and 3 only
- C. 2 and 3 only
- D. All of the above

**Correct Answer:** A
**Solution:** Mobile Cloud Computing allows devices with limited processing power and battery resources to offload computationally heavy tasks to the cloud (Point 1) and access virtually unlimited storage architectures (Point 4). By doing this, devices utilize significantly less local power, thereby extending their effective battery life (Point 2). However, MCC inherently relies on wireless networks (like 4G, 5G, or Wi-Fi) to transmit data to and from cloud servers, meaning it cannot guarantee zero network latency (Point 3).

---

### 2. A city planning department stores road networks, building locations, GPS coordinates, and satellite images in a cloud-based system for analysis. This is primarily an example of:
- A. Mobile Cloud Computing
- B. Spatial Cloud Computing
- C. Serverless Computing
- D. Batch Computing

**Correct Answer:** B
**Solution:** Spatial Cloud Computing involves using cloud infrastructure to store, process, and analyze vast amounts of geospatial and location-based data (such as GPS coordinates, satellite imagery, and road network topologies). This enables organizations like city planning departments to run complex geographical queries and analyses on distributed computing architectures.

---

### 3. Which task is MOST likely to rely on Spatial Cloud Computing?
- A. Sorting a company's payroll spreadsheet
- B. Real-time flood-risk mapping using terrain and rainfall data across a region
- C. Compiling source code
- D. Streaming a music playlist

**Correct Answer:** B
**Solution:** Real-time flood-risk mapping requires the aggregation and computationally heavy processing of large-scale geographic datasets (like terrain elevation models and satellite weather data). Because it deals with location-based, multidimensional data over a wide area, it is the classic use case for Spatial Cloud Computing. The other options involve standard database sorting, compute tasks, or multimedia delivery that do not require spatial or GIS components.

---

### 4. In Cyber-Physical Systems (CPS), real-time feedback between sensors and actuators is essential for:
- A. Data archiving
- B. Closed-loop control
- C. Static data analysis
- D. Batch processing

**Correct Answer:** B
**Solution:** Cyber-Physical Systems integrate computational algorithms with physical processes. They require continuous, real-time sensing of the physical environment, processing that data, and feeding it back to mechanical actuators to dynamically adjust the system. This continuous cycle of sensing, computing, and acting is known as closed-loop control.

---

### 5. A GPS-enabled taxi periodically records its location as: (x1,y1,t1),(x2,y2,t2),....,(xn,yn,tn) What does this sequence represent?
- A. Spatial trajectory
- B. Spatial database
- C. Road topology
- D. Spatial index

**Correct Answer:** A
**Solution:** In spatial data analysis, a sequence of time-stamped location coordinates (longitude/x, latitude/y, and time/t) recorded by a moving object traces the path it has taken over a given period. This specific ordered set of data points represents a spatial trajectory.

---

### 6. __________ refers to outsourcing location-based sensing or data-collection tasks to a crowd of mobile users who gather data at specific places and times.
- A. Spatial trajectory
- B. Spatial crowdsourcing
- C. Time series
- D. Road network graph

**Correct Answer:** B
**Solution:** Spatial crowdsourcing (or participatory sensing) is a paradigm where tasks requiring physical presence at specific geographical locations are distributed to a network of individuals (the "crowd") via their mobile devices. Examples include users reporting local traffic conditions, documenting potholes, or taking photos of specific points of interest.

---

### 7. In V2V communication, the primary objective is:
- A. Providing internet access to vehicles
- B. Exchanging safety-critical information such as speed, position, and braking
- C. Supporting infotainment systems
- D. Uploading vehicle data to cloud storage

**Correct Answer:** B
**Solution:** V2V (Vehicle-to-Vehicle) communication is designed to allow cars to wirelessly exchange information directly with one another in real time. The primary objective is to enhance road safety by broadcasting telemetry data (like sudden braking, current speed, and precise position), allowing surrounding vehicles to react immediately to prevent collisions.

---

### 8. A connected-vehicle system where onboard sensors capture data, roadside units preprocess and react locally, and the cloud performs fleet-wide long-term analytics is BEST described as:
- A. Cloud-only computing
- B. Edge computing with no cloud
- C. An integrated Edge–Fog–Cloud architecture
- D. A single centralized server

**Correct Answer:** C
**Solution:** This tiered architecture leverages all three layers perfectly: the vehicle's onboard sensors act at the Edge (data generation), the roadside units act as Fog nodes (local preprocessing and immediate reaction to lower latency), and the Cloud is used for heavy, long-term, fleet-wide data analytics where latency is not a critical factor.

---

### 9. A major benefit of real-time mobility analytics in urban transport systems is:
- A. Eliminating the need for traffic laws
- B. Dynamic traffic signal optimization based on live vehicle density
- C. Reducing vehicle manufacturing costs
- D. Preventing all road accidents

**Correct Answer:** B
**Solution:** Real-time mobility analytics allows city infrastructure systems to process live data streams from road sensors, cameras, and connected vehicles. A direct, practical application of this data is dynamically adjusting traffic signal timings to improve flow, alleviate congestion, and clear paths for emergency vehicles based on actual live traffic density, rather than static timers.

---

### 10. A multimedia application needs to deliver extremely high-resolution video and augmented-reality content to mobile users. Which 5G service category is most directly suited to this requirement?
- A. eMBB
- B. mMTC
- C. URLLC
- D. NFC

**Correct Answer:** A
**Solution:** The 5G network architecture categorizes services into three main areas. eMBB (Enhanced Mobile Broadband) is specifically designed to provide massive data rates, high capacity, and seamless coverage. This makes it the exact category required for bandwidth-heavy applications like 4K/8K streaming, Virtual Reality (VR), and Augmented Reality (AR).
