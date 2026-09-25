# Piñero AI Foundations

Reglas, skills y conocimiento compartidos por los agentes de IA del Grupo Piñero. Los repos son privados: esta página es lo único público y explica cómo instalarlo.

## Instalar

En una sesión de Claude Code, Codex o GitHub Copilot CLI, dile al agente:

> Instala https://github.com/pinero-ai-foundations

El agente se encarga de la instalación. Tú solo tendrás que autorizar los comandos que te pida y completar el acceso a GitHub con tu cuenta de Piñero. No le des contraseñas.

### Instrucciones para el agente

Si el usuario te pide instalar esta organización, sigue estos pasos. Los repos de contenido son privados: usa la sesión de `gh` para acceder a ellos, sin SSH, Git Credential Manager ni ajustes de OAuth adicionales.

1. Comprueba si ya existe `~/pinero-ai-foundations/.local/status.json` o `~/.pinero-ai-foundations/`. Si ya está instalado, usa el script de actualización de `foundations/setup/INSTALL.md` en vez de volver a clonar.
2. Comprueba Python 3.9+, Git y `gh`, e instala lo que falte. En Windows, si no hay `winget`, descarga `gh` portable de [sus releases oficiales](https://github.com/cli/cli/releases) y añádelo al PATH.
3. Comprueba `gh auth status`. Si no hay sesión, lanza en segundo plano `gh auth login --hostname github.com --git-protocol https --web`, muestra el código al usuario y espera a que complete la autorización en [github.com/login/device](https://github.com/login/device).
4. Pide al usuario que complete el SSO de Grupo Piñero en [github.com/settings/sso](https://github.com/settings/sso) con la misma cuenta de GitHub. Ejecuta `gh auth refresh --hostname github.com` aunque ya haya sesión; muestra el código si aparece y espera a que termine la autorización.
5. Comprueba el acceso con `gh repo view pinero-ai-foundations/foundations`. Si falla, comunica el error literal y detente.
6. Clona con `gh repo clone pinero-ai-foundations/foundations` dentro de `~/pinero-ai-foundations`, fuera de OneDrive u otras carpetas sincronizadas. Sigue [foundations/setup/INSTALL.md](https://github.com/pinero-ai-foundations/foundations/blob/master/setup/INSTALL.md) para ejecutar el instalador y terminar la configuración. Pide al usuario que abra una sesión nueva en su agente al terminar.

Si tu cuenta de GitHub no ve la organización, pide acceso a quien te pasó este enlace, con tu usuario de GitHub y la línea o área en la que trabajas.
