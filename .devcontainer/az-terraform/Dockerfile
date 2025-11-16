FROM mcr.microsoft.com/azure-cli:2.79.0

# Install tar and gawk which are required by VS Code Server
RUN tdnf install -y tar gawk git unzip && \
    # Install Terraform
    TERRAFORM_VERSION=1.13.5 && \
    curl -fsSL https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_arm64.zip -o terraform.zip && \
    unzip terraform.zip && \
    mv terraform /usr/local/bin/ && \
    rm terraform.zip && \
    terraform version
