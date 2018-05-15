---
title: Introduzione ad Azure PowerShell | Microsoft Docs
description: ''
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: c6fdfcdb262e5fe2b8babf14ef2f2760af31f898
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="d9584-102">Introduzione ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9584-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="d9584-103">Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando e per la creazione di script di automazione che funzionano con Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d9584-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="d9584-104">È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale e usarlo in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9584-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="d9584-105">Questo articolo offre un'introduzione all'uso e ne illustra i concetti di base.</span><span class="sxs-lookup"><span data-stu-id="d9584-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="d9584-106">Connettere</span><span class="sxs-lookup"><span data-stu-id="d9584-106">Connect</span></span>

<span data-ttu-id="d9584-107">Il modo più semplice per iniziare è [avviare Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="d9584-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="d9584-108">Avviare Cloud Shell dal riquadro di spostamento in alto nel portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icona di Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="d9584-110">Scegliere la sottoscrizione da usare e creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d9584-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![Creare un account di archiviazione](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="d9584-112">Dopo aver creato lo spazio di archiviazione, Cloud Shell aprirà una sessione di PowerShell nel browser.</span><span class="sxs-lookup"><span data-stu-id="d9584-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell per PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="d9584-114">È anche possibile installare Azure PowerShell e usarlo in locale in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9584-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="d9584-115">Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9584-115">Install Azure PowerShell</span></span>

<span data-ttu-id="d9584-116">Verificare di aver installato l'ultima versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9584-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="d9584-117">Per informazioni sulla versione più recente, vedere le [note sulla versione](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d9584-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="d9584-118">[Installare Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d9584-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="d9584-119">Per verificare che l'installazione sia riuscita, eseguire `Get-Module AzureRM -ListAvailable` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d9584-119">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="log-in-to-azure"></a><span data-ttu-id="d9584-120">Accedere ad Azure</span><span class="sxs-lookup"><span data-stu-id="d9584-120">Log in to Azure</span></span>

<span data-ttu-id="d9584-121">Accedere in modo interattivo:</span><span class="sxs-lookup"><span data-stu-id="d9584-121">Sign on interactively:</span></span>

1. <span data-ttu-id="d9584-122">Digitare `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="d9584-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="d9584-123">Apparirà una finestra di dialogo che richiede le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="d9584-124">L'opzione '-EnvironmentName' consente di accedere ad Azure per la Cina o Azure per la Germania.</span><span class="sxs-lookup"><span data-stu-id="d9584-124">Option '-EnvironmentName' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="d9584-125">Ad esempio: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="d9584-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="d9584-126">Digitare l'indirizzo di posta elettronica e la password associati all'account.</span><span class="sxs-lookup"><span data-stu-id="d9584-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="d9584-127">Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="d9584-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="d9584-128">Dopo aver effettuato l'accesso a un account Azure, è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d9584-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="d9584-129">Creare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9584-129">Create a resource group</span></span>

<span data-ttu-id="d9584-130">Quando è tutto pronto, si usa Azure PowerShell per creare risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="d9584-131">Si crea prima un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9584-131">First, create a Resource Group.</span></span> <span data-ttu-id="d9584-132">I gruppi di risorse di Azure consentono di gestire più risorse che si desidera raggruppare insieme in modo logico.</span><span class="sxs-lookup"><span data-stu-id="d9584-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="d9584-133">Ad esempio, è possibile creare un gruppo di risorse per un'applicazione o un progetto e aggiungere una macchina virtuale, un database e un servizio rete CDN al suo interno.</span><span class="sxs-lookup"><span data-stu-id="d9584-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="d9584-134">Creare un gruppo di risorse denominato "MyResourceGroup" nell'area westeurope di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="d9584-135">A tale scopo, digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d9584-135">To do so type the following command:</span></span>

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

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="d9584-136">Creare una macchina virtuale Windows</span><span class="sxs-lookup"><span data-stu-id="d9584-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="d9584-137">Dopo aver creato il gruppo di risorse, si crea una macchina virtuale Windows al suo interno.</span><span class="sxs-lookup"><span data-stu-id="d9584-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="d9584-138">Per creare una nuova macchina virtuale occorre prima creare le altre risorse necessarie e assegnarle a una configurazione.</span><span class="sxs-lookup"><span data-stu-id="d9584-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="d9584-139">Sarà quindi possibile usare tale configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="d9584-140">Creare le risorse di rete necessarie</span><span class="sxs-lookup"><span data-stu-id="d9584-140">Create the required network resources</span></span>

<span data-ttu-id="d9584-141">È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="d9584-142">Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="d9584-143">Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="d9584-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="d9584-144">Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.</span><span class="sxs-lookup"><span data-stu-id="d9584-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="d9584-145">Creare la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d9584-145">Create the virtual machine</span></span>

<span data-ttu-id="d9584-146">Innanzitutto è necessario un insieme di credenziali per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d9584-146">First we need a set of credentials for the OS.</span></span>

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="d9584-147">Ora che si dispone delle risorse necessarie, è possibile creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="d9584-148">Per questo passaggio, si crea un oggetto di configurazione della macchina virtuale, quindi si usa la configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="d9584-149">Il comando `New-AzureRmVM` genera i risultati dopo che la macchina virtuale è stata creata completamente ed è pronta per essere usata.</span><span class="sxs-lookup"><span data-stu-id="d9584-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="d9584-150">Accedere ora alla macchina virtuale Windows Server appena creata usando Desktop remoto e l'indirizzo IP pubblico della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-150">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="d9584-151">Il comando seguente consente di visualizzare l'indirizzo IP pubblico creato nello script precedente.</span><span class="sxs-lookup"><span data-stu-id="d9584-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="d9584-152">Se si usa un sistema basato su Windows, è possibile eseguire questa operazione dalla riga di comando usando il comando mstsc:</span><span class="sxs-lookup"><span data-stu-id="d9584-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="d9584-153">Fornire la stessa combinazione di nome utente/password usata quando si crea la macchina virtuale per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d9584-153">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="d9584-154">Creare una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="d9584-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="d9584-155">Per creare una nuova macchina virtuale occorre prima creare le altre risorse necessarie e assegnarle a una configurazione.</span><span class="sxs-lookup"><span data-stu-id="d9584-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="d9584-156">Sarà quindi possibile usare tale configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="d9584-157">Ciò presuppone che il gruppo di risorse sia già stato creato come indicato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d9584-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="d9584-158">Sarà inoltre necessario disporre di una chiave pubblica SSH denominata `id_rsa.pub` nella directory .ssh del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="d9584-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="d9584-159">Creare le risorse di rete necessarie</span><span class="sxs-lookup"><span data-stu-id="d9584-159">Create the required network resources</span></span>

<span data-ttu-id="d9584-160">È prima necessario creare una configurazione di subnet da usare con il processo di creazione della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="d9584-161">Si crea anche un indirizzo IP pubblico in modo che sia possibile connettersi a questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="d9584-162">Si crea quindi un gruppo di sicurezza di rete per proteggere l'accesso all'indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="d9584-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="d9584-163">Infine si crea la scheda di interfaccia di rete virtuale usando tutte le risorse precedenti.</span><span class="sxs-lookup"><span data-stu-id="d9584-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="d9584-164">Creare la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d9584-164">Create the virtual machine</span></span>

<span data-ttu-id="d9584-165">Ora che si dispone delle risorse necessarie, è possibile creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="d9584-166">Per questo passaggio, si crea un oggetto di configurazione della macchina virtuale, quindi si usa la configurazione per creare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9584-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

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

<span data-ttu-id="d9584-167">Ora che la macchina virtuale è stata creata, è possibile accedere alla nuova macchina virtuale Linux tramite SSH con l'indirizzo IP pubblico della macchina virtuale creata:</span><span class="sxs-lookup"><span data-stu-id="d9584-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="d9584-168">Creazione di altre risorse in Azure</span><span class="sxs-lookup"><span data-stu-id="d9584-168">Creating other resources in Azure</span></span>

<span data-ttu-id="d9584-169">È stato descritto come creare un gruppo di risorse, una macchina virtuale Linux e una macchina virtuale di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d9584-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="d9584-170">È possibile creare molti altri tipi di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="d9584-171">Ad esempio, per creare un bilanciamento del carico di rete di Azure da associare alle macchine virtuali appena create, si può usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d9584-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="d9584-172">È anche possibile creare una nuova rete virtuale privata (nota come "VNet" all'interno di Azure) per l'infrastruttura usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d9584-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="d9584-173">Ciò che rende potenti Azure e Azure PowerShell è la possibilità di usarli non solo per ottenere un'infrastruttura basata su cloud, ma anche per creare servizi di piattaforma gestiti.</span><span class="sxs-lookup"><span data-stu-id="d9584-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="d9584-174">I servizi di piattaforma gestiti possono anche essere combinati con l'infrastruttura per creare soluzioni ancora più potenti.</span><span class="sxs-lookup"><span data-stu-id="d9584-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="d9584-175">Ad esempio, è possibile usare Azure Powershell per creare un servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="d9584-176">Il servizio app di Azure è un servizio di piattaforma gestito che consente di eseguire l'hosting di app Web senza doversi preoccupare dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d9584-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="d9584-177">Dopo aver creato il servizio app di Azure, è possibile creare due nuove app Web di Azure all'interno del servizio app usando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9584-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="d9584-178">Elenco delle risorse distribuite</span><span class="sxs-lookup"><span data-stu-id="d9584-178">Listing deployed resources</span></span>

<span data-ttu-id="d9584-179">È possibile usare il cmdlet `Get-AzureRmResource` per elencare le risorse in esecuzione in Azure.</span><span class="sxs-lookup"><span data-stu-id="d9584-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="d9584-180">L'esempio seguente illustra le risorse appena create nel nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9584-180">The following example shows the resources we just created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="d9584-181">Eliminazione di risorse</span><span class="sxs-lookup"><span data-stu-id="d9584-181">Deleting resources</span></span>

<span data-ttu-id="d9584-182">Per eseguire la pulizia dell'account Azure, si dovranno rimuovere le risorse create in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="d9584-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="d9584-183">Per eliminare le risorse non più necessarie, si può usare il cmdlet `Remove-AzureRm*`.</span><span class="sxs-lookup"><span data-stu-id="d9584-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="d9584-184">Per rimuovere la macchina virtuale Windows creata, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d9584-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="d9584-185">Verrà richiesto di confermare l'eliminazione delle risorse specificate.</span><span class="sxs-lookup"><span data-stu-id="d9584-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d9584-186">È anche possibile eliminare più risorse contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="d9584-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="d9584-187">Ad esempio, il comando seguente elimina l'intero gruppo di risorse "MyResourceGroup" che abbiamo usato per tutti gli esempi di questa esercitazione introduttiva.</span><span class="sxs-lookup"><span data-stu-id="d9584-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="d9584-188">Il comando elimina il gruppo di risorse e tutte le altre risorse in esso contenute.</span><span class="sxs-lookup"><span data-stu-id="d9584-188">This removes the resource group and all of the resources in it.</span></span>

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d9584-189">Questa operazione può richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="d9584-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="d9584-190">Ottenere gli esempi</span><span class="sxs-lookup"><span data-stu-id="d9584-190">Get samples</span></span>

<span data-ttu-id="d9584-191">Per altre informazioni sull'uso di Azure PowerShell, vedere i nostri script più comuni per le [macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [macchine virtuali di Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), le [app Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e i [database SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="d9584-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d9584-192">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="d9584-192">Next steps</span></span>

* [<span data-ttu-id="d9584-193">Accedere ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9584-193">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="d9584-194">Gestire le sottoscrizioni di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9584-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="d9584-195">Creare entità servizio in Azure usando Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9584-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="d9584-196">Vedere le note sulla migrazione da una versione precedente: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="d9584-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="d9584-197">Ottenere informazioni dalla community:</span><span class="sxs-lookup"><span data-stu-id="d9584-197">Get help from the community:</span></span>
  * [<span data-ttu-id="d9584-198">Forum Azure su MSDN</span><span class="sxs-lookup"><span data-stu-id="d9584-198">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="d9584-199">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="d9584-199">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
