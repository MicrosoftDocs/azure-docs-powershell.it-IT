---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 6e2ecda144472bdb35ffe1310f648b277353177b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019404"
---
# <span data-ttu-id="5077d-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-101">New-AzVM</span></span>

## <span data-ttu-id="5077d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5077d-102">SYNOPSIS</span></span>
<span data-ttu-id="5077d-103">Crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="5077d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5077d-104">SYNTAX</span></span>

### <span data-ttu-id="5077d-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5077d-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5077d-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="5077d-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5077d-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5077d-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5077d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5077d-108">DESCRIPTION</span></span>
<span data-ttu-id="5077d-109">Il cmdlet **New-AzVM** crea una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="5077d-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="5077d-110">Questo cmdlet accetta come input un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="5077d-111">Usa il cmdlet New-AzVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="5077d-112">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface e set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="5077d-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="5077d-113">`SimpleParameterSet`Fornisce un metodo pratico per creare una VM rendendo facoltativi gli argomenti della creazione di VM comuni.</span><span class="sxs-lookup"><span data-stu-id="5077d-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="5077d-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5077d-114">EXAMPLES</span></span>

### <span data-ttu-id="5077d-115">Esempio 1: creare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5077d-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="5077d-116">Questo script di esempio Mostra come creare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="5077d-117">Lo script richiederà un nome utente e una password per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="5077d-118">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5077d-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5077d-119">Esempio 2: creare una macchina virtuale da un'immagine utente personalizzata</span><span class="sxs-lookup"><span data-stu-id="5077d-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5077d-120">Questo esempio accetta un'immagine di sistema operativo personalizzata preimpostata, generalizzata e fissa un disco di dati, applica una nuova rete, distribuisce il disco rigido virtuale e lo esegue.</span><span class="sxs-lookup"><span data-stu-id="5077d-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="5077d-121">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5077d-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="5077d-122">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="5077d-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="5077d-123">Puoi confermare lo stato di accesso usando il cmdlet **Get-AzSubscription** .</span><span class="sxs-lookup"><span data-stu-id="5077d-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="5077d-124">Esempio 3: creare una VM da un'immagine Marketplace senza un IP pubblico</span><span class="sxs-lookup"><span data-stu-id="5077d-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5077d-125">Questo esempio serve una nuova rete e distribuisce una VM Windows dal Marketplace senza creare un indirizzo IP pubblico o un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="5077d-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="5077d-126">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5077d-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="5077d-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5077d-127">PARAMETERS</span></span>

### <span data-ttu-id="5077d-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5077d-128">-AddressPrefix</span></span>
<span data-ttu-id="5077d-129">Il prefisso dell'indirizzo per la rete virtuale che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5077d-130">-AllocationMethod</span></span>
<span data-ttu-id="5077d-131">Metodo di allocazione IP per l'IP pubblico che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5077d-132">-AsJob</span></span>
<span data-ttu-id="5077d-133">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5077d-133">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="5077d-134">-AvailabilitySetName</span></span>
<span data-ttu-id="5077d-135">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="5077d-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-136">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="5077d-136">-Credential</span></span>
<span data-ttu-id="5077d-137">Le credenziali di amministratore per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5077d-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5077d-139">Specifica le dimensioni dei dischi di dati in GB.</span><span class="sxs-lookup"><span data-stu-id="5077d-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5077d-140">-DefaultProfile</span></span>
<span data-ttu-id="5077d-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5077d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="5077d-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="5077d-143">Indica che questo cmdlet non installa l'estensione **Info BG** nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="5077d-144">-DiskFile</span></span>
<span data-ttu-id="5077d-145">Il percorso locale del file del disco rigido virtuale da caricare nel cloud e per creare la VM e deve avere il suffisso ". VHD".</span><span class="sxs-lookup"><span data-stu-id="5077d-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5077d-146">-DomainNameLabel</span></span>
<span data-ttu-id="5077d-147">L'etichetta del sottodominio per il nome di dominio completo (FQDN) della VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="5077d-148">Il modulo sarà necessario `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="5077d-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5077d-149">-EnableUltraSSD</span></span>
<span data-ttu-id="5077d-150">Usare i dischi UltraSSD per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5077d-151">-EvictionPolicy</span></span>
<span data-ttu-id="5077d-152">Criteri di eliminazione per la macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="5077d-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="5077d-153">Solo il valore supportato è "deallocate".</span><span class="sxs-lookup"><span data-stu-id="5077d-153">Only supported value is 'Deallocate'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-154">-HostId</span><span class="sxs-lookup"><span data-stu-id="5077d-154">-HostId</span></span>
<span data-ttu-id="5077d-155">ID dell'host</span><span class="sxs-lookup"><span data-stu-id="5077d-155">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-156">-Immagine</span><span class="sxs-lookup"><span data-stu-id="5077d-156">-Image</span></span>
<span data-ttu-id="5077d-157">Il nome dell'immagine amichevole su cui verrà compilata la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="5077d-158">Questi includono: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, coreos, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="5077d-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5077d-159">-LicenseType</span></span>
<span data-ttu-id="5077d-160">Specifica un tipo di licenza, che indica che l'immagine o il disco per la macchina virtuale è stato concesso in licenza locale.</span><span class="sxs-lookup"><span data-stu-id="5077d-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5077d-161">Questo valore viene usato solo per le immagini che contengono il sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5077d-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="5077d-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5077d-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5077d-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5077d-163">Windows_Client</span></span>
- <span data-ttu-id="5077d-164">Windows_Server questo valore non può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5077d-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="5077d-165">Se specifichi questo parametro per un aggiornamento, il valore deve corrispondere al valore iniziale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="5077d-166">-Linux</span></span>
<span data-ttu-id="5077d-167">Indica se il file su disco è per Linux VM, se specificato; o Windows, se non specificato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5077d-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-168">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5077d-168">-Location</span></span>
<span data-ttu-id="5077d-169">Specifica un percorso per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-169">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5077d-170">-MaxPrice</span></span>
<span data-ttu-id="5077d-171">Prezzo massimo della fatturazione di una macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="5077d-171">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-172">-Nome</span><span class="sxs-lookup"><span data-stu-id="5077d-172">-Name</span></span>
<span data-ttu-id="5077d-173">Il nome della risorsa VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-173">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-174">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="5077d-174">-OpenPorts</span></span>
<span data-ttu-id="5077d-175">Un elenco di porte da aprire nel gruppo di sicurezza della rete (NSG) per la VM creata.</span><span class="sxs-lookup"><span data-stu-id="5077d-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="5077d-176">Il valore predefinito dipende dal tipo di immagine scelto (ad esempio, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="5077d-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-177">-Priorità</span><span class="sxs-lookup"><span data-stu-id="5077d-177">-Priority</span></span>
<span data-ttu-id="5077d-178">Priorità per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="5077d-179">Solo i valori supportati sono "regolari", "spot" e "low".</span><span class="sxs-lookup"><span data-stu-id="5077d-179">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5077d-180">"Normale" è per la normale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-180">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5077d-181">"Spot" è per la macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="5077d-181">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5077d-182">"Basso" è anche per la macchina virtuale spot, ma è sostituito da "spot".</span><span class="sxs-lookup"><span data-stu-id="5077d-182">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5077d-183">Usare "spot" invece di "low".</span><span class="sxs-lookup"><span data-stu-id="5077d-183">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-184">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5077d-184">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5077d-185">ID risorsa del gruppo di posizionamento di prossimità da usare con questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-185">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-186">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="5077d-186">-PublicIpAddressName</span></span>
<span data-ttu-id="5077d-187">Nome di un nuovo indirizzo IP pubblico (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-187">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="5077d-188">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="5077d-188">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5077d-189">-ResourceGroupName</span></span>
<span data-ttu-id="5077d-190">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5077d-190">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-191">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5077d-191">-SecurityGroupName</span></span>
<span data-ttu-id="5077d-192">Il nome di un nuovo (o esistente) gruppo di sicurezza di rete (NSG) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-192">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="5077d-193">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="5077d-193">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-194">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="5077d-194">-Size</span></span>
<span data-ttu-id="5077d-195">Dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-195">The Virtual Machine Size.</span></span>  <span data-ttu-id="5077d-196">Il valore predefinito è: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="5077d-196">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-197">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5077d-197">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5077d-198">Prefisso dell'indirizzo per la subnet che verrà creata per la VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-198">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-199">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5077d-199">-SubnetName</span></span>
<span data-ttu-id="5077d-200">Nome di una nuova subnet (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-200">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="5077d-201">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="5077d-201">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-202">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5077d-202">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5077d-203">Se il parametro è presente, alla VM viene assegnata un'identità di sistema gestita generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5077d-203">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-204">-Tag</span><span class="sxs-lookup"><span data-stu-id="5077d-204">-Tag</span></span>
<span data-ttu-id="5077d-205">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="5077d-205">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5077d-206">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="5077d-206">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5077d-207">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="5077d-207">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-208">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5077d-208">-UserAssignedIdentity</span></span>
<span data-ttu-id="5077d-209">Il nome di un'identità del servizio gestito che deve essere assegnata alla VM.</span><span class="sxs-lookup"><span data-stu-id="5077d-209">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-210">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5077d-210">-VirtualNetworkName</span></span>
<span data-ttu-id="5077d-211">Nome di una nuova rete virtuale (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="5077d-211">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="5077d-212">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="5077d-212">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-213">-VM</span><span class="sxs-lookup"><span data-stu-id="5077d-213">-VM</span></span>
<span data-ttu-id="5077d-214">Specifica una macchina virtuale locale da creare.</span><span class="sxs-lookup"><span data-stu-id="5077d-214">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="5077d-215">Per ottenere un oggetto macchina virtuale, usare il cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5077d-215">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="5077d-216">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzVMOperatingSystem, set-AzVMSourceImage e Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="5077d-216">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-217">-Zona</span><span class="sxs-lookup"><span data-stu-id="5077d-217">-Zone</span></span>
<span data-ttu-id="5077d-218">Specifica l'elenco delle aree della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5077d-218">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-219">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5077d-219">-Confirm</span></span>
<span data-ttu-id="5077d-220">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5077d-220">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5077d-221">-WhatIf</span></span>
<span data-ttu-id="5077d-222">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5077d-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5077d-223">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5077d-223">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5077d-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5077d-224">CommonParameters</span></span>
<span data-ttu-id="5077d-225">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5077d-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5077d-226">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5077d-226">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5077d-227">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5077d-227">INPUTS</span></span>

### <span data-ttu-id="5077d-228">System. String</span><span class="sxs-lookup"><span data-stu-id="5077d-228">System.String</span></span>

### <span data-ttu-id="5077d-229">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5077d-229">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5077d-230">System. String []</span><span class="sxs-lookup"><span data-stu-id="5077d-230">System.String[]</span></span>

### <span data-ttu-id="5077d-231">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5077d-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5077d-232">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5077d-232">OUTPUTS</span></span>

### <span data-ttu-id="5077d-233">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5077d-233">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="5077d-234">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5077d-234">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5077d-235">Note</span><span class="sxs-lookup"><span data-stu-id="5077d-235">NOTES</span></span>

## <span data-ttu-id="5077d-236">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5077d-236">RELATED LINKS</span></span>

[<span data-ttu-id="5077d-237">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-237">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5077d-238">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-238">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="5077d-239">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-239">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="5077d-240">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-240">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="5077d-241">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-241">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="5077d-242">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5077d-242">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="5077d-243">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5077d-243">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="5077d-244">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5077d-244">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="5077d-245">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5077d-245">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="5077d-246">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5077d-246">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="5077d-247">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5077d-247">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="5077d-248">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5077d-248">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


