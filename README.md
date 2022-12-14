# Setup CICD pipeline using code pipeline, code commit and code deploy. Deploy any docker image.

## Steps:
1. You’ve created an AWS Identity and Access Management (IAM) user account with administrative policy permissions, and generated an access key ID and secret key.
2. As part of this setup, we need to install K8s aka EKS, AWS CLI, Kubectl, aws-iam-authenticator, EKSCTL otherwise the setup will not work as expected.
3. Create the ECR repo.
4. Create a code commit repository.
5. Set the below environment variale during pipeline setup
```
    AWS_DEFAULT_REGION
    AWS_CLUSTER_NAME
    AWS_ACCOUNT_ID
    IMAGE_REPO_NAME
    IMAGE_TAG
```
`NOTE: Code deploy doesn't support deployment for K8s. So we are including deploymenet files in the repo` <br />
6. Also add, ecr, eks, s3 access to the build service role.<br />
7. Create an IAM role with some name like CodeBuildKubectlRole. Use the script `create_iam_role.sh`<br />
8. Attach the  cluster with CodeBuildKubectlRole role.<br />
9. Provide the codepipeline service role with ECR access.<br />
10. Run the pipeline and test.
