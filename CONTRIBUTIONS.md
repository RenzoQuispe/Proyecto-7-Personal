# Contribuciones de Renzo Quispe Villena

## Sprint 1
- 2025-06-08: Merge pull request hecho tras conversacion con el equipo. Pull request propuesto por Daren Herrera de feature/infraestructura-inicial sobre develop.
Commit: [`Merge pull request de feature/infraestructura-inicial sobre develop`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/2191248d15bcd7bee823a2defd7897e892516148).
Pull request grupal: [#10](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/10)

- 2025-06-09: Escribí `backup_state.sh` para que copie iac/terraform.tfstate a una carpeta backups con timestamp (tfstate_timestamp.backup). El script debe crear la carpeta si no existe.
Commit: [`feat(script): (Issue #4) agregar script backup_state.sh`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/b42b47eaff3e8e2bee0db265085eab443ad0018c).
Pull request grupal: [#11](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/11)

- 2025-06-09: Escribí `restore_state.sh` para listar los archivos de backups y permita elegir uno mediante menú, y entonces lo copia como iac/terraform.tfstate.  
Commit: [`feat(script): (Issue #5) agregar script restore_state.sh`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/81e0f128599e722a1f872fae66b5a38c3adca2be). 
Pull request grupal: [#11](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/11)

- 2025-06-09: Refactorize `restore_state.sh` para verificar que exista la carpeta backups/, y ademas para que la entrada del usuario tenga que ser un número entero positivo.
Commit: [`refactor(sh): (Issue #5) mejorar manejo de errores en restore_state.sh`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/ea432be4dfdd81ff6183eabccfd4804091fbd573).
Pull request grupal: [#11](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/11)