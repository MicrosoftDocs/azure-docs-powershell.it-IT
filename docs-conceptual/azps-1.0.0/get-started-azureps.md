---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982910"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="e2cdb-102">guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="e2cdb-103">Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="e2cdb-104">È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="e2cdb-105">Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="e2cdb-106">Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-106">Install Azure PowerShell</span></span>

<span data-ttu-id="e2cdb-107">Verificare di aver installato l'ultima versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="e2cdb-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e2cdb-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="e2cdb-109">[Installare Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e2cdb-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="e2cdb-110">Per verificare che l'installazione sia riuscita, eseguire `Get-InstalledModule Az -AllVersions` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="e2cdb-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-111">Azure Cloud Shell</span></span>

<span data-ttu-id="e2cdb-112">Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="e2cdb-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="e2cdb-113">Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icona di Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="e2cdb-115">Scegliere la sottoscrizione da usare e creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Creare un account di archiviazione](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="e2cdb-117">Dopo aver creato lo spazio di archiviazione, Cloud Shell aprirà una sessione di PowerShell nel browser.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell per PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="e2cdb-119">Accedere ad Azure</span><span class="sxs-lookup"><span data-stu-id="e2cdb-119">Sign in to Azure</span></span>

<span data-ttu-id="e2cdb-120">Accedere in modo interattivo:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-120">Sign on interactively:</span></span>

1. <span data-ttu-id="e2cdb-121">Digitare `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="e2cdb-122">L'argomento `-Environment` consente di eseguire l'autenticazione per un'area o un cloud diverso.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="e2cdb-123">Ad esempio, per connettersi ad Azure Cina:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="e2cdb-124">Si otterrà un token da usare in https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="e2cdb-125">Aprire questa pagina nel browser e immettere il token per accedere con le credenziali di Azure e autorizzare Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="e2cdb-126">Dopo aver effettuato l'accesso a un account Azure, è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="e2cdb-127">Per altre informazioni sul processo di accesso e i metodi di autenticazione disponibili, vedere [Accedere con Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e2cdb-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="e2cdb-128">Creare una macchina virtuale Windows mediante semplici impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="e2cdb-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="e2cdb-129">Il cmdlet `New-AzVM` offre una sintassi semplificata, per facilitare la creazione di una nuova macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="e2cdb-130">È necessario specificare solo due valori di parametri, ovvero il nome della macchina virtuale e il set di credenziali per l'account amministratore locale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="e2cdb-131">Creare prima di tutto l'oggetto credenziali.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="e2cdb-132">Creare quindi la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
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

<span data-ttu-id="e2cdb-133">Per determinare quali altri elementi vengono creati e come viene configurata la VM,</span><span class="sxs-lookup"><span data-stu-id="e2cdb-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="e2cdb-134">È possibile esaminare prima di tutto il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="e2cdb-135">Il gruppo di risorse **cloud-shell-storage-westus** viene creato quando si usa Cloud Shell per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="e2cdb-136">Il gruppo di risorse **SampleVM** è stato creato dal cmdlet `New-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="e2cdb-137">Occorre verificare quali altre risorse vengono create nel nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
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

<span data-ttu-id="e2cdb-138">È possibile ottenere altri dettagli sulla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="e2cdb-139">Questo esempio illustra come recuperare informazioni sull'immagine del sistema operativo usata per creare la VM.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="e2cdb-140">Creare una macchina virtuale Linux completamente configurata</span><span class="sxs-lookup"><span data-stu-id="e2cdb-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="e2cdb-141">L'esempio precedente usa la sintassi semplificata e i valori dei parametri predefiniti per creare una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="e2cdb-142">In questo esempio vengono specificati valori per tutte le opzioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="e2cdb-143">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e2cdb-143">Create a resource group</span></span>

<span data-ttu-id="e2cdb-144">In questo esempio si vuole creare un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="e2cdb-145">I gruppi di risorse di Azure consentono di gestire più risorse che si desidera raggruppare insieme in modo logico.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="e2cdb-146">Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="e2cdb-147">Creare un gruppo di risorse denominato "MyResourceGroup" nell'area uswest2 di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="e2cdb-148">A questo scopo, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="e2cdb-149">Il nuovo gruppo di risorse verrà usato per includere tutte le risorse necessarie per la nuova macchina virtuale creata.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="e2cdb-150">Per creare una nuova VM Linux, è prima di tutto necessario creare le altre risorse richieste e assegnarle a una configurazione.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="e2cdb-151">Sarà quindi possibile usare tale configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="e2cdb-152">Sarà inoltre necessario disporre di una chiave pubblica SSH denominata `id_rsa.pub` nella directory `.ssh` del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="e2cdb-153">Creare le risorse di rete necessarie</span><span class="sxs-lookup"><span data-stu-id="e2cdb-153">Create the required network resources</span></span>

<span data-ttu-id="e2cdb-154">È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="e2cdb-155">Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="e2cdb-156">Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="e2cdb-157">Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="e2cdb-158">Creare la configurazione della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e2cdb-158">Create the VM configuration</span></span>

<span data-ttu-id="e2cdb-159">Le risorse necessarie sono ora disponibili, quindi è possibile creare l'oggetto configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="e2cdb-160">Creare la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e2cdb-160">Create the virtual machine</span></span>

<span data-ttu-id="e2cdb-161">È ora possibile creare la macchina virtuale usando l'oggetto configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="e2cdb-162">Ora che la VM è stata creata, si può accedere alla nuova macchina virtuale Linux usando SSH con l'indirizzo IP pubblico della VM creata:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="e2cdb-163">Creazione di altre risorse in Azure</span><span class="sxs-lookup"><span data-stu-id="e2cdb-163">Creating other resources in Azure</span></span>

<span data-ttu-id="e2cdb-164">È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="e2cdb-165">È possibile creare molti altri tipi di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="e2cdb-166">Ad esempio, per creare un bilanciamento del carico di rete di Azure da associare alle macchine virtuali appena create, si può usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="e2cdb-167">È anche possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="e2cdb-168">Ciò che rende potenti Azure e Azure PowerShell è la possibilità di usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestiti.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="e2cdb-169">I servizi di piattaforma gestiti possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="e2cdb-170">Ad esempio, è possibile usare Azure Powershell per creare un servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="e2cdb-171">Il servizio app di Azure è un servizio di piattaforma gestito che consente di eseguire l'hosting di app Web senza doversi preoccupare dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="e2cdb-172">Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="e2cdb-173">Elenco delle risorse distribuite</span><span class="sxs-lookup"><span data-stu-id="e2cdb-173">Listing deployed resources</span></span>

<span data-ttu-id="e2cdb-174">È possibile usare il cmdlet `Get-AzResource` per elencare le risorse in esecuzione in Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="e2cdb-175">L'esempio seguente illustra le risorse create nel nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="e2cdb-176">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="e2cdb-176">Deleting resources</span></span>

<span data-ttu-id="e2cdb-177">Per eseguire la pulizia dell'account Azure, si dovranno rimuovere le risorse create in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="e2cdb-178">Per eliminare le risorse non più necessarie, si può usare il cmdlet `Remove-Az*`.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="e2cdb-179">Per rimuovere la macchina virtuale Windows creata, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="e2cdb-180">Verrà richiesto di confermare che si vuole rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="e2cdb-181">È anche possibile eliminare più risorse contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-181">You can also delete many resources at once.</span></span> <span data-ttu-id="e2cdb-182">Il comando seguente, ad esempio, elimina il gruppo di risorse "MyResourceGroup" finora usato per tutti gli esempi.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="e2cdb-183">Verranno eliminate anche tutte le risorse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="e2cdb-184">A seconda del numero e del tipo di risorse, il completamento dell'attività può richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="e2cdb-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="e2cdb-185">Ottenere gli esempi</span><span class="sxs-lookup"><span data-stu-id="e2cdb-185">Get samples</span></span>

<span data-ttu-id="e2cdb-186">Per altre informazioni sull'uso di Azure PowerShell, vedere i nostri script più comuni per le [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [macchine virtuali di Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [app Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e i [database SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="e2cdb-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e2cdb-187">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="e2cdb-187">Next steps</span></span>

* [<span data-ttu-id="e2cdb-188">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="e2cdb-189">Gestire le sottoscrizioni di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="e2cdb-190">Creare entità servizio in Azure usando Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2cdb-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="e2cdb-191">Ottenere informazioni dalla community:</span><span class="sxs-lookup"><span data-stu-id="e2cdb-191">Get help from the community:</span></span>
  * [<span data-ttu-id="e2cdb-192">Forum Azure su MSDN</span><span class="sxs-lookup"><span data-stu-id="e2cdb-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="e2cdb-193">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="e2cdb-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
