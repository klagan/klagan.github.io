---
published: true
tags: vscode
---
## Exporting VSCode extensions
Visual Studio Code does not synchronise your settings between machines, which isn't a bad thing but is a bit of a pain when you use different machines and they are not quite the same.

I managed to get a beautiful version of Visual Studio Code working for me on one mac but when I went to my other mac it was missing some things but I just didnt know what they were.  

I needed a way to fix this.

Turns out it is three steps (for Apple Mac anyway):

---

## one
Install `code` command

I didnt have this installed which is why I wasnt able to run the command on step 2.

	` 'code' is not recognized as an internal or external command ` 

Your OS can not find the VS Code binary code on its path. The VS Code Windows and Linux 	installations should have installed VS Code on your path. Try uninstalling and reinstalling VS Code. If code is still not found, consult the platform specific setup topics for Windows and Linux.

On macOS, you need to manually run the Shell Command: Install 'code' command in PATH command (available through the Command Palette ⇧⌘P). Consult the macOS specific setup topic for details.

[source](https://code.visualstudio.com/docs/editor/command-line#_common-questions)

---

## two
Run: `code --list-extensions | xargs -L 1 echo code --install-extension`

sample output:
```csharp
code --install-extension Angular.ng-template
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension docsmsft.docs-article-templates
code --install-extension docsmsft.docs-authoring-pack
code --install-extension docsmsft.docs-markdown
code --install-extension docsmsft.docs-preview
code --install-extension eamodio.gitlens
code --install-extension HookyQR.beautify
code --install-extension humao.rest-client
code --install-extension johnpapa.Angular2
code --install-extension karigari.chat
code --install-extension mauve.terraform
code --install-extension mermade.openapi-lint
code --install-extension ms-azure-devops.azure-pipelines
code --install-extension ms-azuretools.vscode-azureappservice
code --install-extension ms-azuretools.vscode-azurefunctions
code --install-extension ms-azuretools.vscode-azurestorage
code --install-extension ms-azuretools.vscode-azureterraform
code --install-extension ms-azuretools.vscode-cosmosdb
code --install-extension ms-azuretools.vscode-service-fabric-reliable-services
code --install-extension MS-CEINTL.vscode-language-pack-en-GB
code --install-extension ms-docfx.DocFX
code --install-extension ms-mssql.mssql
code --install-extension ms-mssql.sqlops-debug
code --install-extension ms-python.python
code --install-extension ms-vscode.autorest
code --install-extension ms-vscode.azure-account
code --install-extension ms-vscode.azurecli
code --install-extension ms-vscode.cpptools
code --install-extension ms-vscode.csharp
code --install-extension ms-vscode.github-issues-prs
code --install-extension ms-vscode.PowerShell
code --install-extension ms-vscode.Theme-MarkdownKit
code --install-extension ms-vscode.Theme-MaterialKit
code --install-extension ms-vscode.Theme-TomorrowKit
code --install-extension ms-vscode.typescript-javascript-grammar
code --install-extension ms-vscode.vs-keybindings
code --install-extension ms-vscode.vscode-node-azure-pack
code --install-extension ms-vscode.vscode-typescript-tslint-plugin
code --install-extension ms-vscode.wordcount
code --install-extension ms-vsliveshare.vsliveshare
code --install-extension ms-vsliveshare.vsliveshare-audio
code --install-extension ms-vsliveshare.vsliveshare-pack
code --install-extension ms-vsts.team
code --install-extension msazurermtools.azurerm-vscode-tools
code --install-extension PeterJausovec.vscode-docker
code --install-extension redhat.vscode-yaml
code --install-extension run-at-scale.terraform-doc-snippets
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension thenikso.github-plus-theme
code --install-extension tht13.html-preview-vscode
code --install-extension VisualStudioExptTeam.vscodeintellicode
code --install-extension VisualStudioOnlineApplicationInsights.application-insights
code --install-extension vsciot-vscode.azure-iot-toolkit
code --install-extension vsciot-vscode.vscode-arduino
code --install-extension vsciot-vscode.vscode-iot-workbench
```
---

## three 
Now I **think** you just run these commands on the destination machine.  I will try tomorrow and see what happens.

---
