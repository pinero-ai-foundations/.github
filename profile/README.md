# Piñero AI Foundations

Reglas, skills y conocimiento compartidos por los agentes de IA del Grupo Piñero. Los repos son privados: esta página es lo único público y explica cómo instalarlo.

## Instalar

1. **Instala Claude y entra con tu cuenta de Piñero**, no con una personal.
   - Windows: la app de escritorio, desde [claude.ai/download](https://claude.ai/download). Pasa a la pestaña **Code**; desde Chat no se puede instalar. Si te pide una carpeta, cualquiera vale.
   - Linux: `curl -fsSL https://claude.ai/install.sh | bash` y después `claude`.
2. **Pega esto tal cual** en una sesión nueva:

   ```text
   Instala Piñero AI Foundations en esta máquina. El repo es privado: no intentes abrir su URL ni uses SSH, Git Credential Manager ni ajustes de OAuth. La única sesión que hace falta es la de gh.
   1. Comprueba Python 3.9+, Git y gh, e instala lo que falte. Si no hay winget, descarga gh portable de sus releases oficiales (github.com/cli/cli/releases) y añádelo a mi PATH.
   2. Si `gh auth status` no tiene sesión, lanza tú en segundo plano `gh auth login --hostname github.com --git-protocol https --web` y enséñame el código. Yo lo pego en el navegador y pulso Authorize junto a pinero-ai-foundations.
   3. Antes de comprobar el acceso, pídeme que entre con la misma cuenta de GitHub en https://github.com/settings/sso y complete el SSO de Grupo Piñero. Después ejecuta `gh auth refresh --hostname github.com`, aunque `gh auth status` indique que ya hay sesión. Enséñame el código si aparece y espera a que complete la autorización en el navegador.
   4. Comprueba el acceso con `gh repo view pinero-ai-foundations/foundations`. Si falla, para y dime el error literal.
   5. Clona con `gh repo clone pinero-ai-foundations/foundations` en ~/pinero-ai-foundations (fuera de OneDrive o cualquier carpeta sincronizada) y sigue foundations/setup/INSTALL.md.
   ```

3. **Lo que te toca a ti:** aprobar los comandos que te pida el agente, entrar en el SSO de Grupo Piñero y, cuando te enseñe un código, pegarlo en [github.com/login/device](https://github.com/login/device) y pulsar **Authorize** junto a `pinero-ai-foundations`. Usa la misma cuenta de GitHub en todos los pasos. No le des contraseñas.
4. **Al terminar, abre una sesión nueva** en Code: las reglas del grupo se cargan al empezar la sesión.

Si tu cuenta de GitHub no ve la organización, pide acceso a quien te pasó este enlace, con tu usuario de GitHub y la línea o área en la que trabajas.
