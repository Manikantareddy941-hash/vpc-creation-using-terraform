# Creation of AWS VPC using Terraform (VS Code) — Step by Step

## 1) Install requirements
- Install **Terraform**
- Install **AWS CLI**
- Install **VS Code**
- (Recommended) Install VS Code extension: **HashiCorp Terraform**

## 2) Configure AWS access
- Open terminal and run:
  - `aws configure`
- Enter:
  - Access Key
  - Secret Key
  - Region (example: `ap-south-1`)
  - Output format: `json`

## 3) Create project folder
- Run:
  - `mkdir terraform-vpc`
  - `cd terraform-vpc`
  - `code .`

## 4) Create Terraform files
Inside the folder create these files:
- `provider.tf`
- `main.tf`
- `variables.tf`
- `outputs.tf`
- `README.md`

## 5) Write Terraform code
- Add provider configuration in `provider.tf`
- Add VPC + subnet + IGW + NAT + route table resources in `main.tf`
- Add variables in `variables.tf`
- Add outputs in `outputs.tf`

## 6) Run Terraform (VS Code Terminal)
Run these commands one by one:
- `terraform init`
- `terraform fmt`
- `terraform validate`
- `terraform plan`
- `terraform apply`

## 7) Verify in AWS Console
Go to:
- AWS Console → **VPC Dashboard**
Check:
- VPC created
- Public + Private subnet created
- IGW attached
- NAT Gateway running
- Route tables linked correctly

## 8) Delete resources (important)
When done practice:
- `terraform destroy`

## Notes
- NAT Gateway costs money → always destroy after practice
- Don’t upload AWS keys or `.tfstate` files to GitHub
