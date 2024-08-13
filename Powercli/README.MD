---
Title: Powercli scripts
Description: Powercli scripts para soluções vmware.
Author: Carascoza
Date: 13/08/20224
---

# Uso do PowerCLi 

>[!IMPORTANT]
>Antes de gerenciar o vSphere Auto Deploy com regras criadas com cmdlets PowerCLI, você deve instalar o PowerCLI.

## Instalação PowerCLi online 

Instalação online 
```powershell
Install-Module VMware.PowerCLI -Scope CurrentUser
```
link oficial : https://developer.vmware.com/docs/15315/GUID-ACD2320C-D00F-4CCE-B968-B3C41A95C085.html

## Instalar o PowerCLI offline

Você pode instalar todos os módulos VMware PowerCLI no modo off-line usando um ZIP arquivo.

Talvez seja necessário instalar o PowerCLI em uma máquina local sem conectividade com a Internet devido a motivos de segurança e restrições de implantação. Se você estiver usando esse ambiente, você pode baixar o arquivo PowerCLI ZIP em um computador com acesso à Internet, transferir o arquivo ZIP para sua máquina local e instalar o PowerCLI.

### Pré-requisitos
Verifique se o sistema é compatível com o PowerCLI. Consulte a Matriz de Compatibilidade (https://code.vmware.com/web/tool/vmware-powercli).

Verifique se o PowerShell está disponível em seu sistema. Para Linux e macOS, você deve instalar o PowerShell (https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell).

Para Windows, se você tiver o PowerCLI 6.5 R1 ou anterior, desinstale-o.

Baixe o arquivo PowerCLI ZIP (https://code.vmware.com/web/tool/vmware-powercli) e transfira o arquivo ZIP para sua máquina local.

### Procedimento
Abra o PowerShell em seu local máquina.
Para exibir os caminhos de pasta para os quais você pode extrair o PowerCLI ZIP , execute o comando:

```powershell
$env:PSModulePath
```
Extraia o conteúdo do arquivo PowerCLI ZIP para uma das pastas listadas.
Para Windows, execute o comando para desbloquear os arquivos copiados.

```powershell
Get-ChildItem -Path 'folder_path' -Recurse | Unblock-File
```

Substitua pelo caminho para a pasta onde você extraiu o conteúdo do arquivo ZIP.folder_path

(Opcional) Verifique se os módulos VMware PowerCLI foram instalados com sucesso.

```powershell
Get-Module VMware* -ListAvailable
```

