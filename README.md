# VraiVraiProjetFinal


My goal was to deploy a Wordpress (without necessarily some content on it)


[Ansible]

I used a file named playbook.yml (this is where we'll write the commands to install WordPress), another called hosts (this tells Ansible on which servers to run the commands).

I splited my playbook in roles (for the server, php, mysql and wordpress)

And I execute playbook.yml with the following code line :

ansible-playbook playbook.yml -i hosts -u user -K







[Packer]

I used a file named scaleway-cloud-courses-template.json where i'm filling the informations needed for the creation of my image. 

I use those code lines "export SCW_TOKEN=yourToken" and "export SCALEWAY_ORGANIZATION=yourOrganizationId" in my .bashrc file in order to safely add my Token and Organization ID.








[Terraform]

In my scaleway.tf file, I define the information of the infrastructure I wish to create.

And my files variables.tf & variables.tfvars are the files where I add my token and ID orgnaization information.

terraform init
terraform plan -var-file="yourNameFile"
terraform apply -var-file"yourNameFile"
