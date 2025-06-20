## Proyecto 7 - Operaciones y recuperación ante desastres locales para infraestructura Terraform

Quispe Villena Renzo - renzo.quispe.v@uni.pe

URL del repositorio grupal: https://github.com/Grupo-9-CC3S2/Proyecto-7

### Aportes al proyecto
#### Sprint 1
Me encargue del desarrollo de los scripts: backup_state.sh y restore_state.sh:
- El script backup_state.sh copia iac/terraform.tfstate a una carpeta backups con timestamp (tfstate_timestamp.backup). El script debe crear la carpeta si no existe.
- El script restore_state.sh lista los archivos de backups y permita elegir uno mediante menú, y entonces lo copia como iac/terraform.tfstate.
#### Sprint 2
Me encargue de actualizar los scripts backup_state.sh y restore_state.sh:
- El script backup_state verifica que iac/terraform.tfstate existe antes de realizar el backup.
- El script restore_state.sh valida la integridad del formato JSON en el backup, usa jq para verificar que la clave version exista y que vale 4.
#### Sprint 3
Me encargue de actualizar los scripts backup_state.sh y restore_state.sh:
- El script backup_state.sh ahora guarda copias incrementales (solo cambios respecto al backup previo, usando rsync)
- El script restore_state.sh ahora permite restaurar incrementalmente y muestra diferencias entre el backup escogido por el usuario y el terraform.tfstate actual antes de sobrescribir.

### Requisitos técnicos

| Herramientas | Versión       |
| Terraform    | 1.12.1        |
|    Bash      | >= 5.1.16     |
|     jq       | >= 1.6        |
|    rsync     | >= 3.1.0      |

### Funcionamiento de scripts
```markdown
git clone https://github.com/RenzoQuispe/Proyecto-7-Personal.git
cd Proyecto-7-Personal
# Primero tener iniciado terraform en iac/
cd iac
terraform init
terraform apply
# Dar permisos de ejecucion a los scripts
cd ..
chmod +x scripts/backup_state.sh
chmod +x scripts/restore_state.sh
# probar scripts con:   
./scripts/backup_state.sh
./scripts/restore_state.sh
```
Con el script backup_state.sh podemos crear multiples backup de terraform.state, y luego con restore_state.sh podemos listarlos y restaurar terraform.tfstate a un estado anterior.
