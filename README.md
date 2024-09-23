# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

I have created a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function is designed to retrieve all EBS snapshots owned by the account and cross-reference them with a list of active EC2 instances (both running and stopped). For each snapshot, it checks if the associated volume is still attached to an active instance. If it identifies a snapshot linked to a volume that is no longer in use, the snapshot is automatically deleted, contributing to AWS cost optimization by eliminating unused resources.

