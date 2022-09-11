# Development Environment

The best development environment is nothing without tools! Here are some PowerShell Scripts to install my preferred selection. *Admin Rights may be needed to execute these Scripts.*

## Chocolatey & Tools

Install from **PowerShell**:

* Chocolatey [https://chocolatey.org](https://chocolatey.org)
* [Git](https://chocolatey.org/packages/git)
* [Azure-CLI](https://chocolatey.org/packages/azure-cli) + [Azure-CLI Extension for Azure DevOps](https://marketplace.visualstudio.com/items?itemName=ms-vsts.cli)
* [Google Chrome](https://chocolatey.org/packages/GoogleChrome)
* [Microsoft Edge](https://chocolatey.org/packages/microsoft-edge)

```powershell
# Install Choco
[Net.ServicePointManager]::SecurityProtocol = [Net.ServicePointManager]::SecurityProtocol -bor [Net.SecurityProtocolType]::Tls12
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
# Install Git
choco install -y git
choco upgrade -y git
# Install Azure CLI
choco install -y azure-cli 
choco upgrade -y azure-cli
# Install Google Chrome
choco install -y googlechrome
choco upgrade -y googlechrome
# Install Microsoft Edge
choco install -y microsoft-edge
choco upgrade -y microsoft-edge
# Reload the PATH variable
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine")
# Install Azure CLI Extension for Azure-DevOps
az extension add --name azure-devops
```

## Power Platform CLI for Windows

[https://docs.microsoft.com/en-us/power-platform/developer/cli/introduction#install-microsoft-power-platform-cli](https://docs.microsoft.com/en-us/power-platform/developer/cli/introduction#install-microsoft-power-platform-cli)

```cmd
pac install latest
```

## Chocolatey & VSCode & VSCode Extensions for AL

```powershell
# Install Choco
[Net.ServicePointManager]::SecurityProtocol = [Net.ServicePointManager]::SecurityProtocol -bor [Net.SecurityProtocolType]::Tls12
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
# Install VSCode
choco install -y vscode
choco upgrade -y vscode
# Reload the PATH variable
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine")
# Install VS-Code Extensions for AL
try { code --install-extension microsoft-IsvExpTools.powerplatform-vscode | Out-Null } catch {}
try { code --install-extension megel.mme2k-powerapps-helper | Out-Null } catch {}
try { code --install-extension davidanson.vscode-markdownlint | Out-Null } catch {}
try { code --install-extension hnw.vscode-auto-open-markdown-preview | Out-Null } catch {}
try { code --install-extension eriklynd.json-tools | Out-Null } catch {}
try { code --install-extension donjayamanne.githistory | Out-Null } catch {}
try { code --install-extension eamodio.gitlens | Out-Null } catch {}
try { code --install-extension heaths.vscode-guid | Out-Null } catch {}
try { code --install-extension streetsidesoftware.code-spell-checker | Out-Null } catch {}  
```

## Full Tooling

Use this to install everything on a new virtual machine to get started...

```Powershell
# Install Choco
[Net.ServicePointManager]::SecurityProtocol = [Net.ServicePointManager]::SecurityProtocol -bor [Net.SecurityProtocolType]::Tls12
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
# Install Git
choco install -y git
choco upgrade -y git
# Install Azure CLI
choco install -y azure-cli 
choco upgrade -y azure-cli
# Install Google Chrome
choco install -y googlechrome
choco upgrade -y googlechrome
# Install Microsoft Edge
choco install -y microsoft-edge
choco upgrade -y microsoft-edge
# Reload the PATH variable
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine")
# Install Azure CLI Extension for Azure-DevOps
az extension add --name azure-devops

# Install VSCode
choco install -y vscode
choco upgrade -y vscode
# Reload the PATH variable
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine")
# Install VS-Code Extensions for AL
try { code --install-extension microsoft-IsvExpTools.powerplatform-vscode | Out-Null } catch {}
try { code --install-extension megel.mme2k-powerapps-helper | Out-Null } catch {}
try { code --install-extension davidanson.vscode-markdownlint | Out-Null } catch {}
try { code --install-extension hnw.vscode-auto-open-markdown-preview | Out-Null } catch {}
try { code --install-extension eriklynd.json-tools | Out-Null } catch {}
try { code --install-extension donjayamanne.githistory | Out-Null } catch {}
try { code --install-extension eamodio.gitlens | Out-Null } catch {}
try { code --install-extension heaths.vscode-guid | Out-Null } catch {}
try { code --install-extension streetsidesoftware.code-spell-checker | Out-Null } catch {}
```
