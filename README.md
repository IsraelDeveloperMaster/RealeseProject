
# 🇧🇷 <a href="https://www.developermaster.net/github/github_pt">Português <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20gestures/Backhand%20Index%20Pointing%20Left%20Light%20Skin%20Tone.png" alt="" width="60" height="30" />

# 🇪🇸 <a href="https://www.developermaster.net/github/github_sp">Español <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20gestures/Backhand%20Index%20Pointing%20Left%20Light%20Skin%20Tone.png" alt="" width="60" height="30" />

# 🇬🇧 <a href="https://www.developermaster.net/github/github_en">Inglés <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20gestures/Backhand%20Index%20Pointing%20Left%20Light%20Skin%20Tone.png" alt="" width="60" height="30" />

######

<img src="https://ziadoua.github.io/m3-Markdown-Badges/badges/Android/android1.svg" alt="">

<img src="https://ziadoua.github.io/m3-Markdown-Badges/badges/AndroidStudio/androidstudio1.svg">

<img src="https://ziadoua.github.io/m3-Markdown-Badges/badges/Java/java1.svg" alt="">

<img src="https://ziadoua.github.io/m3-Markdown-Badges/badges/Kotlin/kotlin3.svg">

<img src="https://ziadoua.github.io/m3-Markdown-Badges/badges/Ubuntu/ubuntu1.svg">

<img src="https://user-images.githubusercontent.com/74038190/212748842-9fcbad5b-6173-4175-8a61-521f3dbb7514.gif" width="500">
<br><br>

<img src="https://github-readme-stats.vercel.app/api/top-langs?username=IsraelDeveloperMaster&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"/>

######

# PORTUGUÊS

# 🚀 Kotlin Release Workflow com Release Please

Este repositório contém um aplicativo de exemplo desenvolvido em **Kotlin**, projetado para ensinar como automatizar o processo de criação de versões (releases) utilizando a ferramenta **Release Please** integrada ao **GitHub Actions**.

O objetivo principal é demonstrar como configurar e gerenciar um fluxo de versionamento contínuo e eficiente para projetos Kotlin, seguindo as melhores práticas de automação e semântica de versionamento (**Semantic Versioning**).

## ✨ Funcionalidades

- Aplicação desenvolvida com **Kotlin** e estrutura modular.
- Configuração do **Release Please** para geração automática de changelogs e versões baseadas nos commits.
- Integração com **GitHub Actions** para automação do fluxo de releases.
- Uso de **Semantic Versioning** para garantir releases consistentes.
- **Exemplo prático** de configuração do arquivo `.release-please-config.json`.

## 📋 Pré-requisitos

- Conta no **GitHub**.
- Conhecimento básico de **Kotlin** e **GitHub Actions**.
- **Node.js** instalado para configurar o Release Please CLI (opcional).

## ⚙️ Como funciona?

1. **Commits estruturados**: Os commits seguem o formato do **Conventional Commits** (e.g., `feat: nova funcionalidade`, `fix: correção de bug`).
2. **Pull Request automática**: O **Release Please** cria automaticamente um PR contendo a próxima versão e o changelog correspondente.
3. **Merge do PR**: Após o merge, o GitHub Actions gera a tag e publica a release no repositório.

## 🛠️ Tecnologias utilizadas

- **Kotlin**: Linguagem principal do projeto.
- **Release Please**: Ferramenta de automação de releases.
- **GitHub Actions**: Orquestrador para CI/CD.
- **Conventional Commits**: Padrão para mensagens de commits.

## 📚 Configuração do projeto

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/IsraelDeveloperMaster/RealeseProject.git
   ```

2. **Configure o Release Please**:
   Adicione o arquivo `.release-please-config.json` na raiz do projeto:
   ```json
   {
     "branches": ["main"],
     "release-type": "java",
     "package-name": "nome-do-pacote"
   }
   ```

3. **Ative o GitHub Actions**:
   Certifique-se de que as ações estão habilitadas no repositório.

   4. **Ajuste o workflow do Release Please**:
      Edite ou crie o arquivo `.github/workflows/release-please.yml`:
      ```yaml
      name: Release Please

      on:
        push:
          branches:
            - master

      jobs:
        release:
          runs-on: ubuntu-latest
          steps:
            - uses: googleapis/release-please-action@v4
              id: release
              with:
                release-type: simple
   
            - name: Checkout 🛬
              if: ${{ steps.release.outputs.release_created }}
              uses: actions/checkout@v4
      
            - name: Tag major and minor versions 🏷
              if: ${{ steps.release.outputs.release_created }}
              run: |
           
              git config user.name github-actions[bot]
              git config user.email 41898282+github-actions[bot]@users.noreply.github.com
              git remote add gh-token "https://${{ secrets.PASSWORD_GITHUB }}@github.com/googleapis/release-please-action.git"
              git tag -d v${{ steps.release.outputs.major }} || true
              git tag -d v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
              git push origin :v${{ steps.release.outputs.major }} || true
              git push origin :v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
              git tag -a v${{ steps.release.outputs.major }} -m "Release v${{ steps.release.outputs.major }}"
              git tag -a v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} -m "Release v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}"
              git push origin v${{ steps.release.outputs.major }}
              git push origin v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}
   
      ```

## 🚀 Como contribuir

Sinta-se à vontade para abrir **issues** ou enviar **pull requests** com melhorias, sugestões ou correções.

## 📝 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

# ESPAÑOL


# 🚀 Flujo de Lanzamiento en Kotlin con Release Please

Este repositorio contiene una aplicación de ejemplo desarrollada en **Kotlin**, diseñada para enseñar cómo automatizar el proceso de creación de versiones (releases) utilizando la herramienta **Release Please** integrada con **GitHub Actions**.

El objetivo principal es demostrar cómo configurar y gestionar un flujo de versionado continuo y eficiente para proyectos en Kotlin, siguiendo las mejores prácticas de automatización y versionado semántico (**Semantic Versioning**).

## ✨ Funcionalidades

- Aplicación desarrollada en **Kotlin** con estructura modular.
- Configuración de **Release Please** para la generación automática de changelogs y versiones basadas en los commits.
- Integración con **GitHub Actions** para automatizar el flujo de lanzamientos.
- Uso de **Semantic Versioning** para garantizar versiones consistentes.
- **Ejemplo práctico** de configuración del archivo `.release-please-config.json`.

## 📋 Requisitos previos

- Cuenta en **GitHub**.
- Conocimientos básicos de **Kotlin** y **GitHub Actions**.
- **Node.js** instalado para configurar el Release Please CLI (opcional).

## ⚙️ ¿Cómo funciona?

1. **Commits estructurados**: Los commits siguen el formato de **Conventional Commits** (por ejemplo, `feat: nueva funcionalidad`, `fix: corrección de bug`).
2. **Pull Request automática**: **Release Please** crea automáticamente un PR que contiene la próxima versión y el changelog correspondiente.
3. **Merge del PR**: Tras el merge, **GitHub Actions** genera la etiqueta (tag) y publica la release en el repositorio.

## 🛠️ Tecnologías utilizadas

- **Kotlin**: Lenguaje principal del proyecto.
- **Release Please**: Herramienta para automatización de lanzamientos.
- **GitHub Actions**: Orquestador para CI/CD.
- **Conventional Commits**: Estándar para mensajes de commits.

## 📚 Configuración del proyecto

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/IsraelDeveloperMaster/RealeseProject.git
   ```

2. **Configura Release Please**:
   Añade el archivo `.release-please-config.json` en la raíz del proyecto:
   ```json
   {
     "branches": ["main"],
     "release-type": "java",
     "package-name": "nombre-del-paquete"
   }
   ```

3. **Activa GitHub Actions**:
   Asegúrate de que las acciones están habilitadas en el repositorio.

4. **Ajusta el workflow de Release Please**:
   Edita o crea el archivo `.github/workflows/release-please.yml`:
   ```yaml
   name: Release Please

   on:
     push:
       branches:
         - master

   jobs:
     release:
       runs-on: ubuntu-latest
       steps:
         - uses: googleapis/release-please-action@v4
           id: release
           with:
             release-type: simple

         - name: Checkout 🛬
           if: ${{ steps.release.outputs.release_created }}
           uses: actions/checkout@v4

         - name: Tag major and minor versions 🏷
           if: ${{ steps.release.outputs.release_created }}
           run: |
             git config user.name github-actions[bot]
             git config user.email 41898282+github-actions[bot]@users.noreply.github.com
             git remote add gh-token "https://${{ secrets.PASSWORD_GITHUB }}@github.com/googleapis/release-please-action.git"
             git tag -d v${{ steps.release.outputs.major }} || true
             git tag -d v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
             git push origin :v${{ steps.release.outputs.major }} || true
             git push origin :v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} || true
             git tag -a v${{ steps.release.outputs.major }} -m "Release v${{ steps.release.outputs.major }}"
             git tag -a v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }} -m "Release v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}"
             git push origin v${{ steps.release.outputs.major }}
             git push origin v${{ steps.release.outputs.major }}.${{ steps.release.outputs.minor }}
   ```

## 🚀 Cómo contribuir

No dudes en abrir **issues** o enviar **pull requests** con mejoras, sugerencias o correcciones.

## 📝 Licencia

Este proyecto está licenciado bajo la [Licencia MIT](LICENSE).
