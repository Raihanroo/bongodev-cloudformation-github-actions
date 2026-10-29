# bongoDev Homework - Submission Checklist

- [x] GitHub repository URL containing `cloudformation.yaml` and `.github/workflows/deploy.yml`.
- [x] Screenshot: successful GitHub Actions workflow (the green check and steps).
- [x] Screenshot: CloudFormation stack `bongodev-github-iac-dev` in `CREATE_COMPLETE` or `UPDATE_COMPLETE`.
- [x] Screenshot: Ubuntu EC2 instance and tags (sensitive IDs are cropped from the public evidence).
- [x] Screenshot: Nginx website reading `Hello from bongoDev!` and `Environment: dev`.
- [x] GitHub commit URL where the EC2 `Course` tag is modified and automatically deployed.
- [x] Screenshot: CloudFormation update and the new EC2 tag after second push.
- [x] Screenshot: deleted stack / cleanup confirmation.
- [x] Two sentences explaining what GitHub Actions does and what CloudFormation does.

## Submission evidence

Evidence screenshots are in [`evidence/`](./evidence/):

- [Successful GitHub Actions run](./evidence/github-actions-success.png)
- [Course tag update commit](./evidence/course-tag-commit.png)
- [CloudFormation update complete](./evidence/cloudformation-update-complete.png)
- [Updated EC2 Course tag](./evidence/ec2-updated-course-tag.png)
- [Nginx website](./evidence/nginx-website.png)
- [CloudFormation stack deletion complete](./evidence/cloudformation-delete-complete.png)
- [IAM policy deletion confirmation](./evidence/iam-policy-deleted.png)

Second-push commit: [Update EC2 Course tag through IaC](https://github.com/Raihanroo/bongodev-cloudformation-github-actions/commit/07d2938dd67a284a54367c575bd8684f8c60a9c4).

GitHub Actions runs the deployment workflow on a push and uses OIDC to obtain temporary AWS credentials. CloudFormation reads the YAML template and creates or updates the AWS infrastructure described by it.

Do not submit AWS access keys, session tokens, `.aws/credentials`, private SSH keys, or a trust policy with unnecessary wildcard principals. Never commit such material.
