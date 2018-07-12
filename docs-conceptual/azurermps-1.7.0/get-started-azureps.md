---
title: Introduzione ad Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 3a0d3d1d970f4458e66167fb55c840598ce59e13
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100325"
---
# <a name="getting-started-with-azure-powershell"></a>Introduzione ad Azure PowerShell

Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager. È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale e usarlo in una sessione di PowerShell. Questo articolo offre un'introduzione all'uso e ne illustra i concetti di base.

## <a name="connect"></a>Connettere

Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).

1. Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.

   ![Icona di Shell](~/media/get-started-azureps/shell-icon.png)

2. Scegliere la sottoscrizione da usare e creare un account di archiviazione.

   ![Creare un account di archiviazione](~/media/get-started-azureps/storage-prompt.png)

Dopo aver creato lo spazio di archiviazione, Cloud Shell aprirà una sessione di PowerShell nel browser.

![Cloud Shell per PowerShell](~/media/get-started-azureps/cloud-powershell.png)

È anche possibile installare Azure PowerShell e usarlo in locale in una sessione di PowerShell.

## <a name="install-azure-powershell"></a>Installare Azure PowerShell

Verificare di aver installato l'ultima versione di Azure PowerShell. Per informazioni sulla versione più recente, vedere le [note sulla versione](./release-notes-azureps.md).

1. [Installare Azure PowerShell](install-azurerm-ps.md).

2. Per verificare che l'installazione sia riuscita, eseguire `Get-Module AzureRM -ListAvailable` dalla riga di comando.

## <a name="log-in-to-azure"></a>Accedere ad Azure

Accedere in modo interattivo:

1. Digitare `Login-AzureRmAccount`. Apparirà una finestra di dialogo che richiede le credenziali di Azure. L'opzione '-EnvironmentName' consente di accedere ad Azure per la Cina o Azure per la Germania.

   Ad esempio: Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Digitare l'indirizzo di posta elettronica e la password associati all'account. Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.

Dopo aver effettuato l'accesso a un account Azure, è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.

## <a name="create-a-resource-group"></a>Creare un gruppo di risorse

Quando è tutto pronto, si usa Azure PowerShell per creare risorse in Azure.

Si crea prima un gruppo di risorse. I gruppi di risorse di Azure consentono di gestire più risorse che si desidera raggruppare insieme in modo logico. Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.

Creare un gruppo di risorse denominato "MyResourceGroup" nell'area westeurope di Azure. A tale scopo, digitare il comando seguente:

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Creare una macchina virtuale Windows

Dopo aver creato il gruppo di risorse, si crea una macchina virtuale Windows al suo interno. Per creare una nuova macchina virtuale occorre prima creare le altre risorse necessarie e assegnarle a una configurazione. Sarà quindi possibile usare tale configurazione per creare la macchina virtuale.

### <a name="create-the-required-network-resources"></a>Creare le risorse di rete necessarie

È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale. Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale. Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico. Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Creare la macchina virtuale

Innanzitutto è necessario un insieme di credenziali per il sistema operativo.

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Ora che si dispone delle risorse necessarie, è possibile creare la macchina virtuale. Per questo passaggio, si crea un oggetto di configurazione della macchina virtuale, quindi si usa la configurazione per creare la macchina virtuale.

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Il comando `New-AzureRmVM` genera i risultati dopo che la macchina virtuale è stata creata completamente ed è pronta per essere usata.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Accedere ora alla macchina virtuale Windows Server appena creata usando Desktop remoto e l'indirizzo IP pubblico della macchina virtuale. Il comando seguente consente di visualizzare l'indirizzo IP pubblico creato nello script precedente.

```powershell
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Se si usa un sistema basato su Windows, è possibile eseguire questa operazione dalla riga di comando usando il comando mstsc:

```powershell
mstsc /v:xx.xxx.xx.xxx
```

Fornire la stessa combinazione di nome utente/password usata quando si crea la macchina virtuale per l'accesso.

## <a name="create-a-linux-virtual-machine"></a>Creare una macchina virtuale Linux

Per creare una nuova macchina virtuale occorre prima creare le altre risorse necessarie e assegnarle a una configurazione. Sarà quindi possibile usare tale configurazione per creare la macchina virtuale. Ciò presuppone che il gruppo di risorse sia già stato creato come indicato in precedenza. Sarà inoltre necessario disporre di una chiave pubblica SSH denominata `id_rsa.pub` nella directory .ssh del profilo utente.

### <a name="create-the-required-network-resources"></a>Creare le risorse di rete necessarie

È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale. Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale. Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico. Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Creare la macchina virtuale

Ora che si dispone delle risorse necessarie, è possibile creare la macchina virtuale. Per questo passaggio, si crea un oggetto di configurazione della macchina virtuale, quindi si usa la configurazione per creare la macchina virtuale.

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Ora che la macchina virtuale è stata creata, è possibile accedere alla nuova macchina virtuale Linux tramite SSH con l'indirizzo IP pubblico della macchina virtuale creata:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a>Creazione di altre risorse in Azure

È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server. È possibile creare molti altri tipi di risorse di Azure.

Ad esempio, per creare un bilanciamento del carico di rete di Azure da associare alle macchine virtuali appena create, si può usare il comando seguente:

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

È anche possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando seguente:

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Ciò che rende potenti Azure e Azure PowerShell è la possibilità di usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestiti. I servizi di piattaforma gestiti possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.

Ad esempio, è possibile usare Azure Powershell per creare un servizio app di Azure. Il servizio app di Azure è un servizio di piattaforma gestito che consente di eseguire l'hosting di app Web senza doversi preoccupare dell'infrastruttura. Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi seguenti:

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Elenco delle risorse distribuite

È possibile usare il cmdlet `Get-AzureRmResource` per elencare le risorse in esecuzione in Azure. L'esempio seguente illustra le risorse appena create nel nuovo gruppo di risorse.

```powershell
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Eliminazione di risorse

Per eseguire la pulizia dell'account Azure, si dovranno rimuovere le risorse create in questo esempio. Per eliminare le risorse non più necessarie, si può usare il cmdlet `Remove-AzureRm*`. Per rimuovere la macchina virtuale Windows creata, usare il comando seguente:

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Verrà richiesto di confermare l'eliminazione delle risorse specificate.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

È anche possibile eliminare più risorse contemporaneamente. Ad esempio, il comando seguente elimina l'intero gruppo di risorse "MyResourceGroup" che abbiamo usato per tutti gli esempi di questa esercitazione introduttiva. Il comando elimina il gruppo di risorse e tutte le altre risorse in esso contenute.

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Questa operazione può richiedere alcuni minuti.

## <a name="get-samples"></a>Ottenere gli esempi

Per altre informazioni sull'uso di Azure PowerShell, vedere i nostri script più comuni per le [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [macchine virtuali di Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [app Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e i [database SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Passaggi successivi

* [Accedere ad Azure PowerShell](authenticate-azureps.md)
* [Gestire le sottoscrizioni di Azure con Azure PowerShell](manage-subscriptions-azureps.md)
* [Creare entità servizio in Azure usando Azure PowerShell](create-azure-service-principal-azureps.md)
* Vedere le note sulla migrazione da una versione precedente: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Ottenere informazioni dalla community:
  * [Forum Azure su MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
