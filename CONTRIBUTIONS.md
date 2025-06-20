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

## Sprint 2
- 2025-06-13: Merge pull request hecho tras conversacion con el equipo. Pull request propuesto por Daren Herrera de docs/readme-video sobre develop.
Commit: [`Merge pull request #23 de docs/readme-video sobre develop`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/02838dc6f994392e745d091e6d4337439ec8ed6c).
Pull request grupal: [#23](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/23)

- 2025-06-13: Actualize el script `backup_state`, ahora verifica que iac/terraform.tfstate existe antes de realizar el backup.
Commit: [`feat(script): (Issue #18) actualizar script backup_state.sh con validacion de existencia de iac/terraform.tfstate`](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25/commits/b3e8b45db32c7eaea74306f60717fa86f22e40d5).
Pull request grupal: [#25](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25)

- 2025-06-13: Actualize el script `restore_state.sh`, ahora valida la integridad del formato JSON en el backup, usa jq para verificar que la clave version exista y que vale 4.
Commit: [`feat(script): (Issue #19) actualizar script restore_state.sh con validación de integridad JSON y clave version`](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25/commits/429ac9da9d83c5bc05c674ba4e142b10e1335e83). 
Pull request grupal: [#25](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25)

- 2025-06-15: Refactorize `restore_state.sh` para verificar que "version" : 4.
Commit: [`refactor(sh): (Issue #19) actualizar script restore_state.sh con verificacion de "version": 4`](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25/commits/46af8323d4009a8724ddacb29f8ce99332753be1).
Pull request grupal: [#25](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/25)

- 2025-06-15: Merge pull request hecho tras conversacion con el equipo. Pull request propuesto por Daren Herrera de feat/balanceador-logica sobre develop.
Commit: [`Merge pull request #26 de feat/balanceador-logica sobre develop`](https://github.com/Grupo-9-CC3S2/Proyecto-7/commit/850380ecffed09f2b92c685c97d50802f7424748).
Pull request grupal: [#26](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/26)

## Sprint 3
- 2025-06-19: Actualize el script backup_state.sh, ahora guarda copias incrementales (solo cambios respecto al backup previo, usando rsync)
Commit: [`feat(script): (Issue #31) actualizar script backup_state.sh con logica de copias incrementales usando rsync`](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/36/commits/eb782a01525737d4c4a9c480eea376160f00197c).
Pull request grupal: [#36](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/36)

- 2025-06-19: Actualize script restore_state.sh, ahora permite restaurar incrementalmente y muestra diferencias entre el backup escogido por el usuario y el terraform.tfstate actual antes de sobrescribir.
Commit: [`feat(script): (Issue #32) actualizar script restore_state.sh con logica de restauracion incremental y mostrar diferencias antes de sobrescribir`](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/36/commits/6f2f9e2adcf3bbc49396e608b8eb5540003166ca).
Pull request grupal: [#36](https://github.com/Grupo-9-CC3S2/Proyecto-7/pull/36)
