# AWS-VPN

Private VPN on AWS using WireGuard and EC2.

## Deployment

This project includes a GitHub Action to automatically deploy the CloudFormation template to AWS.

### Prerequisites

1.  **AWS Key Pair**: Ensure you have an existing EC2 Key Pair in your AWS region.
2.  **GitHub Secrets**: Add the following secrets to your GitHub repository:
    - `AWS_KEY_PAIR_NAME`: The name of your existing EC2 Key Pair.

### How it works

The workflow in `.github/workflows/deploy.yml` triggers on every push to the `main` branch. It uses the `aws-actions/aws-cloudformation-github-deploy` action to create or update the CloudFormation stack named `aws-vpn-stack`.
