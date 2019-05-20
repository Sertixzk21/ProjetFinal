# __VraiVraiProjetFinal__


My goal was to deploy a Wordpress (without necessarily some content on it)


__[Ansible]__

I used a file named __playbook.yml__ (this is where we'll write the commands to install WordPress), another called hosts (this tells Ansible on which servers to run the commands).

I splited my playbook in roles (for the server, php, mysql and wordpress)

And I execute playbook.yml with the following code line :

__ansible-playbook playbook.yml -i hosts -u root__







__[Packer]__

I used a file named scaleway-cloud-courses-template.json where i'm filling the informations needed for the creation of my image. 

I use those code lines "__export SCW_TOKEN=yourToken__" and "__export SCALEWAY_ORGANIZATION=yourOrganizationId__" in my __.bashrc__ file in order to safely add my Token and Organization ID.








__[Terraform]__

In my __scaleway.tf__ file, I define the information of the infrastructure I wish to create.

And my files __variables.tf__ & __variables.tfvars__ are the files where I add my token and ID orgnaization information.

__terraform init__  
__terraform plan -var-file="yourNameFile"__  
__terraform apply -var-file"yourNameFile"__  
 
