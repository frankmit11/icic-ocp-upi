# Quick notes:
- For inventory file, make sure to replace any text that is surrounded by `<like this>`. These values should be in the TLS cert, the SSH key and the image registry credentials.
- We thought it would be nice to be able to add multiple SSH keys to the OCP nodes. We didn't think there was a good way to do it automatically so the we manually edited the bootstrap.ign file where all SSH keys are listed to include a new SSH key.


# Generating ignition files
After editing the inventory.yaml to suit your needs, you should be able to just run "ansible-playbook -i inventory.yaml 01-preparation.yaml" and the bootstrap, master and worker.ign files should be generated.
