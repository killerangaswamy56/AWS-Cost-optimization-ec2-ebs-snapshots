# AWS-Cost-optimization-ec2-ebs-snapshots
AWS Cloud Cost Optimization - Identifying Stale Resources
Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
<img width="960" alt="2025-05-12_22h34_52" src="https://github.com/user-attachments/assets/743c1ccb-176b-4d81-bb17-124a22a3de27" />
