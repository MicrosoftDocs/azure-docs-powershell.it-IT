---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 5354a75e969e084d6457d0566a516705f365476f
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368314"
---
# <a name="get-started-with-azure-powershell"></a>guida introduttiva ad Azure PowerShell

Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager. È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale. Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.

## <a name="install-azure-powershell"></a>Installare Azure PowerShell

Verificare di aver installato l'ultima versione di Azure PowerShell. Per informazioni sulla versione più recente, vedere le [note sulla versione](./release-notes-azureps.md).

1. [Installare Azure PowerShell](install-azurerm-ps.md).

2. Per verificare che l'installazione sia riuscita, eseguire `Get-Module AzureRM -ListAvailable` dalla riga di comando.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).

1. Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.

   ![Icona di Shell](~/media/get-started-azureps/shell-icon.png)

2. Scegliere la sottoscrizione da usare e creare un account di archiviazione.

   ![Creare un account di archiviazione](~/media/get-started-azureps/storage-prompt.png)

Dopo aver creato lo spazio di archiviazione, Cloud Shell aprirà una sessione di PowerShell nel browser.

![Cloud Shell per PowerShell](~/media/get-started-azureps/cloud-powershell.png)

È anche possibile installare Azure PowerShell e usarlo in locale in una sessione di PowerShell.

## <a name="sign-in-to-azure"></a>Accedere ad Azure

Accedere in modo interattivo:

1. Digitare `Connect-AzureRmAccount`. Apparirà una finestra di dialogo che richiede le credenziali di Azure. L'opzione '-Environment' consente di eseguire l'autenticazione per Azure Cina o Azure Germania.

   Ad esempio, Connect-AzureRmAccount -Environment AzureChinaCloud

2. Digitare l'indirizzo di posta elettronica e la password associati all'account. Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.

Dopo aver effettuato l'accesso a un account Azure, è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Creare una macchina virtuale Windows mediante semplici impostazioni predefinite

Il cmdlet `New-AzureRmVM` offre una sintassi semplificata, per facilitare la creazione di una nuova macchina virtuale. È necessario specificare solo due valori di parametri, ovvero il nome della macchina virtuale e il set di credenziali per l'account amministratore locale nella macchina virtuale.

Creare prima di tutto l'oggetto credenziali.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Creare quindi la macchina virtuale.

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

La procedura è semplice. Ma è possibile che ci si domandi se vengono creati altri elementi e come viene configurata la macchina virtuale. È possibile esaminare prima di tutto il gruppo di risorse.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Il gruppo di risorse **cloud-shell-storage-westus** viene creato quando si usa Cloud Shell per la prima volta. Il gruppo di risorse **SampleVM** è stato creato dal cmdlet `New-AzureRmVM`.

Occorre verificare quali altre risorse vengono create nel nuovo gruppo di risorse.

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

È possibile ottenere altri dettagli sulla macchina virtuale. Questo esempio mostra come recuperare informazioni sull'immagine del sistema operativo usata per creare la macchina virtuale.

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Creare una macchina virtuale Linux completamente configurata

L'esempio precedente usa la sintassi semplificata e i valori dei parametri predefiniti per creare una macchina virtuale Windows. In questo esempio vengono specificati valori per tutte le opzioni della macchina virtuale.

### <a name="create-a-resource-group"></a>Creare un gruppo di risorse

Per questo esempio si vuole creare un gruppo di risorse. I gruppi di risorse di Azure consentono di gestire più risorse che si desidera raggruppare insieme in modo logico. Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.

Creare un gruppo di risorse denominato "MyResourceGroup" nell'area westeurope di Azure. A questo scopo, usare il comando seguente:

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

Il nuovo gruppo di risorse verrà usato per includere tutte le risorse necessarie per la nuova macchina virtuale creata. Per creare una nuova macchina virtuale occorre prima creare le altre risorse necessarie e assegnarle a una configurazione. Sarà quindi possibile usare tale configurazione per creare la macchina virtuale. Sarà inoltre necessario disporre di una chiave pubblica SSH denominata `id_rsa.pub` nella directory .ssh del profilo utente.

#### <a name="create-the-required-network-resources"></a>Creare le risorse di rete necessarie

È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale. Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale. Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico. Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a>Creare la configurazione della macchina virtuale

Le risorse necessarie sono ora disponibili, quindi è possibile creare l'oggetto configurazione della macchina virtuale.

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a>Creare la macchina virtuale

È ora possibile creare la macchina virtuale usando l'oggetto configurazione della macchina virtuale.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Ora che la macchina virtuale è stata creata, è possibile accedere alla nuova macchina virtuale Linux tramite SSH con l'indirizzo IP pubblico della macchina virtuale creata:

```bash
ssh xx.xxx.xxx.xxx
```

```output
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

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

È anche possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando seguente:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Ciò che rende potenti Azure e Azure PowerShell è la possibilità di usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestiti. I servizi di piattaforma gestiti possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.

Ad esempio, è possibile usare Azure Powershell per creare un servizio app di Azure. Il servizio app di Azure è un servizio di piattaforma gestito che consente di eseguire l'hosting di app Web senza doversi preoccupare dell'infrastruttura. Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi seguenti:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Elenco delle risorse distribuite

È possibile usare il cmdlet `Get-AzureRmResource` per elencare le risorse in esecuzione in Azure. L'esempio seguente illustra le risorse appena create nel nuovo gruppo di risorse.

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Verrà richiesto di confermare l'eliminazione delle risorse specificate.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

È anche possibile eliminare più risorse contemporaneamente. Ad esempio, il comando seguente elimina l'intero gruppo di risorse "MyResourceGroup" che abbiamo usato per tutti gli esempi di questa esercitazione introduttiva. Il comando elimina il gruppo di risorse e tutte le altre risorse in esso contenute.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Questa operazione può richiedere alcuni minuti.

## <a name="get-samples"></a>Ottenere gli esempi

Per altre informazioni sull'uso di Azure PowerShell, vedere i nostri script più comuni per le [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [macchine virtuali di Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [app Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e i [database SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Passaggi successivi

* [Accedere con Azure PowerShell](authenticate-azureps.md)
* [Gestire le sottoscrizioni di Azure con Azure PowerShell](manage-subscriptions-azureps.md)
* [Creare entità servizio in Azure usando Azure PowerShell](create-azure-service-principal-azureps.md)
* Vedere le note sulla migrazione da una versione precedente: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Ottenere informazioni dalla community:
  * [Forum Azure su MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
