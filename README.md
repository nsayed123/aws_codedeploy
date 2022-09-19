# aws_codePipeline

## Steps:
1. You’ve created an AWS Identity and Access Management (IAM) user account with administrative policy permissions, and generated an access key ID and secret key
2. As part of this setup, we need to install K8s, AWS CLI, Kubectl, aws-iam-authenticator, EKSCTL otherwise the setup will not work as expected.
3. Create the ECR repo.
4. Set the below environment variale.

```AWS_DEFAULT_REGION
AWS_CLUSTER_NAME
AWS_ACCOUNT_ID
IMAGE_REPO_NAME
IMAGE_TAG```

5. NOTE: Also add, ecr, eks, s3 access to the build service role.
6. Create an IAM role with some name like CodeBuildKubectlRole. Use the script `create_iam_role.sh`
