## EC2 Instances Purchasing Options
• On-Demand Instances – short workload, predictable pricing, pay by second
• Reserved (1 & 3 years)
• Reserved Instances – long workloads
• Convertible Reserved Instances – long workloads with flexible instances
• Savings Plans (1 & 3 years) –commitment to an amount of usage, long workload
• Spot Instances – short workloads, cheap, can lose instances (less reliable)
• Dedicated Hosts – book an entire physical server, control instance placement
• Dedicated Instances – no other customers will share your hardware
• Capacity Reservations – reserve capacity in a specific AZ for any duration


### EC2 On Demand
• Pay for what you use:
• Linux or Windows - billing per second, after the first minute
• All other operating systems - billing per hour
• Has the highest cost but no upfront payment
• No long-term commitment
• Recommended for short-term and un-interrupted workloads, where
you can't predict how the application will behave
EC2 Reserved Instances
• Up to 72% discount compared to On-demand
• You reserve a specific instance attributes (Instance Type, Region, Tenancy, OS)
• Reservation Period – 1 year (+discount) or 3 years (+++discount)
• Payment Options – No Upfront (+), Partial Upfront (++), All Upfront (+++)
• Reserved Instance’s Scope – Regional or Zonal (reserve capacity in an AZ)
• Recommended for steady-state usage applications (think database)
• You can buy and sell in the Reserved Instance Marketplace
• Convertible Reserved Instance
• Can change the EC2 instance type, instance family, OS, scope and tenancy
• Up to 66% discount

### EC2 Savings Plans
• Get a discount based on long-term usage (up to 72% - same as RIs)
• Commit to a certain type of usage ($10/hour for 1 or 3 years)
• Usage beyond EC2 Savings Plans is billed at the On-Demand price
• Locked to a specific instance family & AWS region (e.g., M5 in us-east-1)
• Flexible across:
• Instance Size (e.g., m5.xlarge, m5.2xlarge)
• OS (e.g., Linux, Windows)
• Tenancy (Host, Dedicated, Default)


### EC2 Spot Instances
• Can get a discount of up to 90% compared to On-demand
• Instances that you can “lose” at any point of time if your max price is less than the
current spot price
• The MOST cost-efficient instances in AWS
• Useful for workloads that are resilient to failure
• Batch jobs
• Data analysis
• Image processing
• Any distributed workloads
• Workloads with a flexible start and end time
• Not suitable for critical jobs or databases


### EC2 Dedicated Hosts
• A physical server with EC2 instance capacity fully dedicated to your use
• Allows you address compliance requirements and use your existing server- bound software licenses (per-socket, per-core, pe—VM software licenses)
• Purchasing Options:
• On-demand – pay per second for active Dedicated Host
• Reserved - 1 or 3 years (No Upfront, Partial Upfront, All Upfront)
• The most expensive option
• Useful for software that have complicated licensing model (BYOL – Bring Your Own License)
• Or for companies that have strong regulatory or compliance needs


### EC2 Dedicated Instances • Instances run on hardware that’s dedicated to you
• May share hardware with other
instances in same account
• No control over instance placement
(can move hardware after Stop / Start)


### EC2 Capacity Reservations
• Reserve On-Demand instances capacity in a specific AZ for any duration
• You always have access to EC2 capacity when you need it
• No time commitment (create/cancel anytime), no billing discounts
• Combine with Regional Reserved Instances and Savings Plans to benefit
from billing discounts
• You’re charged at On-Demand rate whether you run instances or not
• Suitable for short-term, uninterrupted workloads that needs to be in a
specific AZ


### EC2 Spot Instance Requests
• Can get a discount of up to 90% compared to On-demand
• Define max spot price and get the instance while current spot price < max
• The hourly spot price varies based on offer and capacity
• If the current spot price > your max price you can choose to stop or terminate your instance with a 2 minutes grace period.
• Other strategy: Spot Block
• “block” spot instance during a specified time frame (1 to 6 hours) without interruptions
• In rare situations, the instance may be reclaimed
• Used for batch jobs, data analysis, or workloads that are resilient to failures.
• Not great for critical jobs or databases

### How to terminate Spot Instances?
You can only cancel Spot Instance requests that are open, active, or disabled.
Cancelling a Spot Request does not terminate instances
You must first cancel a Spot Request, and then terminate the associated Spot Instances


### Spot Fleets
• Spot Fleets = set of Spot Instances + (optional) On-Demand Instances
• The Spot Fleet will try to meet the target capacity with price constraints
• Define possible launch pools: instance type (m5.large), OS, Availability Zone
• Can have multiple launch pools, so that the fleet can choose
• Spot Fleet stops launching instances when reaching capacity or max cost
• Strategies to allocate Spot Instances:
• lowestPrice: from the pool with the lowest price (cost optimization, short workload)
• diversified: distributed across all pools (great for availability, long workloads)
• capacityOptimized: pool with the optimal capacity for the number of instances
• Spot Fleets allow us to automatically request Spot Instances with the lowest price

### EC2 Section – Summary
• EC2 Instance: AMI (OS) + Instance Size (CPU + RAM) + Storage +
security groups + EC2 User Data
• Security Groups: Firewall attached to the EC2 instance
• EC2 User Data: Script launched at the first start of an instance
• SSH: start a terminal into our EC2 Instances (port 22)
• EC2 Instance Role: link to IAM roles
• Purchasing Options: On-Demand, Spot, Reserved (Standard +
Convertible + Scheduled), Dedicated Host, Dedicated Instance

