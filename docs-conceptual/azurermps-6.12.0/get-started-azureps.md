---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 09/11/2018
ms.openlocfilehash: 5378cdb9d70aa0d2dc617d06d3c887ec20eb7767
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575825"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="54168-102">guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54168-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="54168-103">Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="54168-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="54168-104">È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="54168-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="54168-105">Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.</span><span class="sxs-lookup"><span data-stu-id="54168-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="54168-106">Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54168-106">Install Azure PowerShell</span></span>

<span data-ttu-id="54168-107">Verificare di aver installato l'ultima versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54168-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="54168-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="54168-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="54168-109">[Installare Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="54168-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="54168-110">Per verificare che l'installazione sia riuscita, eseguire `Get-Module AzureRM -ListAvailable` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="54168-110">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="54168-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="54168-111">Azure Cloud Shell</span></span>

<span data-ttu-id="54168-112">Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="54168-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="54168-113">Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icona di Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="54168-115">Scegliere la sottoscrizione da usare e creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54168-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Creare un account di archiviazione](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="54168-117">Dopo aver creato lo spazio di archiviazione, Cloud Shell aprirà una sessione di PowerShell nel browser.</span><span class="sxs-lookup"><span data-stu-id="54168-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell per PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="54168-119">È anche possibile installare Azure PowerShell e usarlo in locale in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54168-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="54168-120">Accedere ad Azure</span><span class="sxs-lookup"><span data-stu-id="54168-120">Sign in to Azure</span></span>

<span data-ttu-id="54168-121">Accedere in modo interattivo:</span><span class="sxs-lookup"><span data-stu-id="54168-121">Sign on interactively:</span></span>

1. <span data-ttu-id="54168-122">Digitare `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="54168-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="54168-123">Verrà visualizzata una finestra di dialogo in cui vengono richieste le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-123">You'll get a dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="54168-124">L'opzione '-Environment' consente di eseguire l'autenticazione per Azure Cina o Azure Germania.</span><span class="sxs-lookup"><span data-stu-id="54168-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="54168-125">Ad esempio, Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="54168-125">for example, Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="54168-126">Digitare l'indirizzo di posta elettronica e la password associati all'account.</span><span class="sxs-lookup"><span data-stu-id="54168-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="54168-127">Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="54168-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="54168-128">Dopo aver effettuato l'accesso a un account Azure, è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="54168-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="54168-129">Creare una macchina virtuale Windows mediante semplici impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="54168-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="54168-130">Il cmdlet `New-AzureRmVM` offre una sintassi semplificata, per facilitare la creazione di una nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="54168-131">È necessario specificare solo due valori di parametri, ovvero il nome della macchina virtuale e il set di credenziali per l'account amministratore locale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="54168-132">Creare prima di tutto l'oggetto credenziali.</span><span class="sxs-lookup"><span data-stu-id="54168-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="54168-133">Creare quindi la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-133">Next, create the VM.</span></span>

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

<span data-ttu-id="54168-134">Per determinare quali altri elementi vengono creati e come viene configurata la VM,</span><span class="sxs-lookup"><span data-stu-id="54168-134">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="54168-135">È possibile esaminare prima di tutto il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54168-135">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="54168-136">Il gruppo di risorse **cloud-shell-storage-westus** viene creato quando si usa Cloud Shell per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="54168-136">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="54168-137">Il gruppo di risorse **SampleVM** è stato creato dal cmdlet `New-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="54168-137">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="54168-138">Occorre verificare quali altre risorse vengono create nel nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54168-138">Now, what other resources were created in this new resource group?</span></span>

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

<span data-ttu-id="54168-139">È possibile ottenere altri dettagli sulla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-139">Let's get some more details about the VM.</span></span> <span data-ttu-id="54168-140">Questo esempio illustra come recuperare informazioni sull'immagine del sistema operativo usata per creare la VM.</span><span class="sxs-lookup"><span data-stu-id="54168-140">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="54168-141">Creare una macchina virtuale Linux completamente configurata</span><span class="sxs-lookup"><span data-stu-id="54168-141">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="54168-142">L'esempio precedente usa la sintassi semplificata e i valori dei parametri predefiniti per creare una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="54168-142">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="54168-143">In questo esempio vengono specificati valori per tutte le opzioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-143">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="54168-144">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="54168-144">Create a resource group</span></span>

<span data-ttu-id="54168-145">In questo esempio si vuole creare un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54168-145">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="54168-146">I gruppi di risorse di Azure consentono di gestire più risorse che si desidera raggruppare insieme in modo logico.</span><span class="sxs-lookup"><span data-stu-id="54168-146">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="54168-147">Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.</span><span class="sxs-lookup"><span data-stu-id="54168-147">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="54168-148">Creare un gruppo di risorse denominato "MyResourceGroup" nell'area westeurope di Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-148">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="54168-149">A questo scopo, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="54168-149">To do so type the following command:</span></span>

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

<span data-ttu-id="54168-150">Il nuovo gruppo di risorse verrà usato per includere tutte le risorse necessarie per la nuova macchina virtuale creata.</span><span class="sxs-lookup"><span data-stu-id="54168-150">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="54168-151">Per creare una nuova VM Linux, è prima di tutto necessario creare le altre risorse richieste e assegnarle a una configurazione.</span><span class="sxs-lookup"><span data-stu-id="54168-151">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="54168-152">Sarà quindi possibile usare tale configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-152">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="54168-153">Sarà inoltre necessario disporre di una chiave pubblica SSH denominata `id_rsa.pub` nella directory .ssh del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="54168-153">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="54168-154">Creare le risorse di rete necessarie</span><span class="sxs-lookup"><span data-stu-id="54168-154">Create the required network resources</span></span>

<span data-ttu-id="54168-155">È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-155">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="54168-156">Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-156">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="54168-157">Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="54168-157">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="54168-158">Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.</span><span class="sxs-lookup"><span data-stu-id="54168-158">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-vm-configuration"></a><span data-ttu-id="54168-159">Creare la configurazione della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="54168-159">Create the VM configuration</span></span>

<span data-ttu-id="54168-160">Le risorse necessarie sono ora disponibili, quindi è possibile creare l'oggetto configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-160">Now that we have the required resources we can create the VM configuration object.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="54168-161">Creare la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="54168-161">Create the virtual machine</span></span>

<span data-ttu-id="54168-162">È ora possibile creare la macchina virtuale usando l'oggetto configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54168-162">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="54168-163">Ora che la VM è stata creata, si può accedere alla nuova macchina virtuale Linux usando SSH con l'indirizzo IP pubblico della VM creata:</span><span class="sxs-lookup"><span data-stu-id="54168-163">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="54168-164">Creazione di altre risorse in Azure</span><span class="sxs-lookup"><span data-stu-id="54168-164">Creating other resources in Azure</span></span>

<span data-ttu-id="54168-165">È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="54168-165">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="54168-166">È possibile creare molti altri tipi di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-166">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="54168-167">Ad esempio, per creare un bilanciamento del carico di rete di Azure da associare alle macchine virtuali appena create, si può usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="54168-167">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="54168-168">È anche possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="54168-168">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="54168-169">Ciò che rende potenti Azure e Azure PowerShell è la possibilità di usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestiti.</span><span class="sxs-lookup"><span data-stu-id="54168-169">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="54168-170">I servizi di piattaforma gestiti possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.</span><span class="sxs-lookup"><span data-stu-id="54168-170">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="54168-171">Ad esempio, è possibile usare Azure Powershell per creare un servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-171">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="54168-172">Il servizio app di Azure è un servizio di piattaforma gestito che consente di eseguire l'hosting di app Web senza doversi preoccupare dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="54168-172">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="54168-173">Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="54168-173">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="54168-174">Elenco delle risorse distribuite</span><span class="sxs-lookup"><span data-stu-id="54168-174">Listing deployed resources</span></span>

<span data-ttu-id="54168-175">È possibile usare il cmdlet `Get-AzureRmResource` per elencare le risorse in esecuzione in Azure.</span><span class="sxs-lookup"><span data-stu-id="54168-175">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="54168-176">L'esempio seguente illustra le risorse create nel nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54168-176">The following example shows the resources we created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="54168-177">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="54168-177">Deleting resources</span></span>

<span data-ttu-id="54168-178">Per eseguire la pulizia dell'account Azure, si dovranno rimuovere le risorse create in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="54168-178">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="54168-179">Per eliminare le risorse non più necessarie, si può usare il cmdlet `Remove-AzureRm*`.</span><span class="sxs-lookup"><span data-stu-id="54168-179">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="54168-180">Per rimuovere la macchina virtuale Windows creata, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="54168-180">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="54168-181">Verrà richiesto di confermare che si vuole rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="54168-181">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="54168-182">È anche possibile eliminare più risorse contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="54168-182">You can also delete many resources at once.</span></span> <span data-ttu-id="54168-183">Il comando seguente, ad esempio, elimina il gruppo di risorse "MyResourceGroup" finora usato per tutti gli esempi.</span><span class="sxs-lookup"><span data-stu-id="54168-183">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="54168-184">Verranno eliminate anche tutte le risorse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="54168-184">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="54168-185">A seconda del numero e del tipo di risorse, il completamento dell'attività può richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="54168-185">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="54168-186">Ottenere gli esempi</span><span class="sxs-lookup"><span data-stu-id="54168-186">Get samples</span></span>

<span data-ttu-id="54168-187">Per altre informazioni sull'uso di Azure PowerShell, vedere i nostri script più comuni per le [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [macchine virtuali di Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [app Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e i [database SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="54168-187">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="54168-188">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="54168-188">Next steps</span></span>

* [<span data-ttu-id="54168-189">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54168-189">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="54168-190">Gestire le sottoscrizioni di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54168-190">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="54168-191">Creare entità servizio in Azure usando Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="54168-191">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="54168-192">Vedere le note sulla versione in merito alla migrazione da una versione precedente: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes)</span><span class="sxs-lookup"><span data-stu-id="54168-192">Read the release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="54168-193">Ottenere informazioni dalla community:</span><span class="sxs-lookup"><span data-stu-id="54168-193">Get help from the community:</span></span>
  * [<span data-ttu-id="54168-194">Forum Azure su MSDN</span><span class="sxs-lookup"><span data-stu-id="54168-194">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="54168-195">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="54168-195">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
