```bash
terraform workspace select old-name
terraform state pull > old-name.tfstate
terraform workspace new new-name
terraform state push old-name.tfstate
terraform show # just to confirm that the newly-imported state looks “right”, before we delete the old workspace
terraform workspace delete -force old-name
```
