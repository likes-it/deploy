# Define the default target
.DEFAULT_GOAL := help

# Help message
help:
	@echo "Makefile for deploying Ansible playbooks"
	@echo "Usage:"
	@echo "  make pre-prod-deploy    Deploy to the dev environment"
	@echo "  make prod-deploy   Deploy to the prod environment"
	@echo "  make help          Show this help message"

pre-prod-deploy:
	@echo "Deploying to the pre-prod environment..."
	ansible-playbook -i hosts pb-deploy.yml --limit=like-it-pre-prod.coak.fr

prod-deploy:
	@echo "Deploying to the production environment..."
	ansible-playbook -i hosts pb-deploy.yml --limit=like-it.coak.fr 


#gitlab-prod-deploy-run:
#	ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i hosts pb-deploy.yml --limit=ec2-52-47-135-226.eu-west-3.compute.amazonaws.com --vault-password-file .vault_password.txt --key-file .ssh_key
