## Proyecto 7 - Operaciones y recuperación ante desastres locales para infraestructura Terraform

Quispe Villena Renzo - renzo.quispe.v@uni.pe

URL del repositorio grupal: https://github.com/Grupo-9-CC3S2/Proyecto-7

### Aportes al proyecto

Me encargue del desarrollo de los scripts: backup_state.sh y restore_state.sh
- El script backup_state.sh copia iac/terraform.tfstate a una carpeta backups con timestamp (tfstate_timestamp.backup). El script debe crear la carpeta si no existe.
- El script restore_state.sh lista los archivos de backups y permita elegir uno mediante menú, y entonces lo copia como iac/terraform.tfstate.

### Funcionamiento de scripts
```markdown
git clone https://github.com/Grupo-9-CC3S2/Proyecto-7.git
cd Proyecto-7
# Primero tener iniciado terraform en iac/
cd iac
terraform init
terraform apply
# Dar permisos de ejecucion a los scripts
cd ..
chmod +x scripts/backup_state.sh
chmod +x scripts/restore_state.sh
# probar scripts    
./scripts/backup_state.sh
./scripts/restore_state.sh
```
Con el script backup_state.sh podemos crear multiples backup de terraform.state, y luego con restore_state.sh podemos listarlos y restaurar terraform.state a un estado anterior.
