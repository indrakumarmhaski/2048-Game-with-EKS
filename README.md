# 2048-Game-with-EKS
A cloud-native application deployment using Amazon EKS and AWS Fargate


**Introduction:**
In this project, I had the opportunity to explore cutting-edge technologies that enable seamless orchestration, scalability, and security for containerized applications.

**Project Overview:**
The project revolves around creating an Amazon EKS cluster and deploying the 2048 game application. But wait, there's more! We didn't just stop at deployment; we optimized the setup using Fargate for serverless container execution, enhancing resource utilization and reducing management overhead.

**Step 1: EKS Cluster Creation and Fargate Profile:**
The journey began with the creation of an Amazon EKS cluster named "demo-cluster" in the US East region. But what makes this cluster truly exciting is the utilization of AWS Fargate as the execution environment. This decision brought serverless benefits to the Kubernetes world, enabling hassle-free scaling and resource management.

**Step 2: AWS Load Balancer Controller Integration:**
To ensure optimal load balancing and traffic distribution, we integrated the AWS Load Balancer Controller into our EKS cluster. This ingenious solution automates the creation and management of Application Load Balancers, streamlining the deployment of Kubernetes services and enhancing their accessibility.

**Step 3: IAM Roles for Service Accounts:**
Security is paramount, and we didn't compromise. By associating an IAM OIDC provider with our EKS cluster, we unlocked the power of IAM roles for service accounts. This means each pod gets its own IAM role, enabling granular access controls while maintaining simplicity and centralizing identity management.

**Step 4: Helm Charts for Seamless Deployment:**
For streamlined application deployment, we harnessed the capabilities of Helm charts. These pre-packaged templates allowed us to effortlessly install the AWS Load Balancer Controller, complete with customizable configurations. The charts provided a consistent way to manage Kubernetes applications, saving time and effort.


**Key Takeaways:**
- Amazon EKS and Fargate offer a powerful duo for orchestrating containerized applications with flexibility and efficiency.
- The AWS Load Balancer Controller simplifies load balancing and enhances application availability in Kubernetes environments.
- IAM roles for service accounts enhance security by providing fine-grained access controls to pods.
- Helm charts simplify the deployment process, allowing for consistent and repeatable application releases.

**Conclusion:**
From orchestrating containers to managing access controls, every component played a vital role in creating a robust and efficient infrastructure. This project has not only enhanced my technical skills but has also fueled my enthusiasm for embracing innovation in the world of cloud computing.

