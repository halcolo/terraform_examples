# CHECK before run this script

- Validate your GKE API is enabled 
- Your Account service have following permissions with a custom role or search for a role how have these permitions
    - compute.instanceGroupManagers.get
    - compute.networks.create
    - compute.networks.delete
    - compute.networks.get
    - compute.networks.updatePolicy
    - compute.subnetworks.create
    - compute.subnetworks.delete
    - compute.subnetworks.get
    - container.clusters.create
    - container.clusters.delete
    - container.clusters.get
    - container.operations.get

- And the role of iam.seviceAccountUser with the following permissions would be applyed
    - iam.serviceAccounts.actAs
    - iam.serviceAccounts.get
    - iam.serviceAccounts.list
    - resourcemanager.projects.get
    - resourcemanager.projects.list

## INPUTS
| Input         | example     | description |
|--------------|-----------|------------|
| project | optical-metric-450220      | GCP project ID       |
| credentials     | ../auth/credentials.json  | json account service path       |
## OUTPUTS

| Output         | Description     |
|--------------|-----------|
| project | gcp project_id     |
| instructions     | instructions to check k8s context and set context if doesn't setted |