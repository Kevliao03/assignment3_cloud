# Before running the playbooks, make sure to activate the correct virtual environment:

python3 -m venv assignment3_env

# Activate the virtual environment

source assignment3_env/bin/activate

# Install the required packages (MUST BE IN THE VIRTUAL ENVIRONMENT)

pip install ansible openstacksdk python-openstackclient

# source the OpenStack RC file

source CH-822922-openrc.sh
(my chameleon CLI password is kurt4979 i think)

# Deactivate the virtual environment when done working on project

deactivate

# Run the playbooks

ansible-playbook -i Inventory -e "@variables.yaml" playbook_master.yaml

ansible-playbook -i Inventory -e "@variables.yaml" playbook_retrieve_facts_vms.yaml

ansible-playbook -i Inventory -e "@variables.yaml" playbook_step_by_step.yaml
