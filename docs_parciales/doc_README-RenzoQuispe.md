# Coautor README.md: Renzo Quispe Villena

## Descripción de scripts

`backup_state.sh`
- Crea una carpeta `backups/`, si no existe, para almacenar todos los archivos de respaldo.
- Se genera el nombre del backup añadiendo un timestamp, con formato `YYYY-MM-DD_HH-MM-SS`, al final.
- Se inserta el estado actual (en el momento de la ejecución del script) del archivo de estado de terraform `terraform.tfstate`. 

`restore_state.sh`
- Lee todos los archivos de respaldo en la carpeta `backups/` y verifica que haya al menos un archivo.
- Muestra una lista de los archivos de respaldo y le pide al usuario escribir el número correspondiente al backup que quiere restaurar.
- Copia el archivo de respaldo a la ruta de `terraform.tfstate` (en `iac/`) y restaura el estado.

Para ejecutar los scripts:
```bash
cd scripts
# Dar permiso de ejecución
chmod +x nombre_script.sh
# Ejecutar el script
./nombre_script.sh
```
