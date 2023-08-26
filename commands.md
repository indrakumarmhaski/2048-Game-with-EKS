List of commands used in the project, along with a brief summary of each:


1. `aws configure`:
   - Command to configure AWS CLI with account credentials and preferences.

2. `eksctl create cluster --name demo-cluster --region us-east-1 --fargate`:
   - Creates an Amazon EKS cluster named "demo-cluster" in the "us-east-1" region using AWS Fargate for pod execution.

3. `eksctl create fargateprofile --cluster demo-cluster --region us-east-1 --name alb-sample-app --namespace game-2048`:
   - Creates a Fargate profile for the "game-2048" namespace in the "demo-cluster" EKS cluster to run pods with AWS Fargate.

4. `kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml`:
   - Deploys the 2048 game application and AWS Load Balancer Controller using the provided YAML configuration.

5. `eksctl utils associate-iam-oidc-provider --cluster demo-cluster --approve --region us-east-1`:
   - Associates an IAM OIDC provider with the EKS cluster, enabling IAM roles for service accounts.

6. `curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/install/iam_policy.json`:
   - Downloads the AWS IAM policy JSON file for the AWS Load Balancer Controller.

7. `aws iam create-policy --policy-name PolicyName --policy-document file://iam_policy.json`:
   - Creates an IAM policy using the specified policy document JSON file.

8. `eksctl create iamserviceaccount --cluster=demo-cluster --region us-east-1 --namespace=kube-system --name=aws-load-balancer-controller --role-name AmazonEKSLoadBalancerControllerRole --attach-policy-arn=arn:aws:I am::<Replace_With_AWS_Account_ID>:policy/AWSLoadBalancerControllerIAMPolicy --approve`:
   - Creates an IAM service account and associated IAM role for the AWS Load Balancer Controller.

9. `helm repo add eks https://aws.github.io/eks-charts`:
   - Adds the Helm repository named "eks" with the specified URL to Helm's configuration.

10. `helm install aws-load-balancer-controller eks/aws-load-balancer-controller -n kube-system --set clusterName=demo-cluster --set serviceAccount.create=false --set serviceAccount.name=aws-load-balancer-controller --set region=us-east-1 --set vpcId=<Replace_With_VPC_ID>`:
    - Installs the AWS Load Balancer Controller using Helm, with specified configuration options, in the `kube-system` namespace.

These commands collectively set up an Amazon EKS cluster, deploy the AWS Load Balancer Controller, and configure various resources to enable efficient and secure management of Kubernetes applications on AWS.
