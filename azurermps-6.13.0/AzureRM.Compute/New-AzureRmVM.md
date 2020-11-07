---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686462"
---
# <span data-ttu-id="fce10-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-101">New-AzureRmVM</span></span>

## <span data-ttu-id="fce10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fce10-102">SYNOPSIS</span></span>
<span data-ttu-id="fce10-103">Crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fce10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fce10-104">SYNTAX</span></span>

### <span data-ttu-id="fce10-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fce10-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fce10-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="fce10-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce10-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fce10-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fce10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fce10-108">DESCRIPTION</span></span>
<span data-ttu-id="fce10-109">Il cmdlet **New-AzureRmVM** crea una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="fce10-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="fce10-110">Questo cmdlet accetta come input un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="fce10-111">Usa il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="fce10-112">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="fce10-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="fce10-113">`SimpleParameterSet`Fornisce un metodo pratico per creare una VM rendendo facoltativi gli argomenti della creazione di VM comuni.</span><span class="sxs-lookup"><span data-stu-id="fce10-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="fce10-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fce10-114">EXAMPLES</span></span>

### <span data-ttu-id="fce10-115">Esempio 1: creare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fce10-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="fce10-116">Questo script di esempio Mostra come creare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="fce10-117">Lo script richiederà un nome utente e una password per la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="fce10-118">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce10-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="fce10-119">Esempio 2: creare una macchina virtuale da un'immagine utente personalizzata</span><span class="sxs-lookup"><span data-stu-id="fce10-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="fce10-120">Questo esempio accetta un'immagine di sistema operativo personalizzata preimpostata, generalizzata e fissa un disco di dati, applica una nuova rete, distribuisce il disco rigido virtuale e lo esegue.</span><span class="sxs-lookup"><span data-stu-id="fce10-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="fce10-121">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fce10-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="fce10-122">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="fce10-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="fce10-123">Puoi confermare lo stato di accesso usando il cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="fce10-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="fce10-124">Esempio 3: creare una VM da un'immagine Marketplace senza un IP pubblico</span><span class="sxs-lookup"><span data-stu-id="fce10-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="fce10-125">Questo esempio serve una nuova rete e distribuisce una VM Windows dal Marketplace senza creare un indirizzo IP pubblico o un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="fce10-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="fce10-126">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fce10-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="fce10-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fce10-127">PARAMETERS</span></span>

### <span data-ttu-id="fce10-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fce10-128">-AddressPrefix</span></span>
<span data-ttu-id="fce10-129">Il prefisso dell'indirizzo per la rete virtuale che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="fce10-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fce10-130">-AllocationMethod</span></span>
<span data-ttu-id="fce10-131">Metodo di allocazione IP per l'IP pubblico che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="fce10-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fce10-132">-AsJob</span></span>
<span data-ttu-id="fce10-133">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="fce10-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fce10-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="fce10-134">-AvailabilitySetName</span></span>
<span data-ttu-id="fce10-135">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="fce10-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="fce10-136">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="fce10-136">-Credential</span></span>
<span data-ttu-id="fce10-137">Le credenziali di amministratore per la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="fce10-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="fce10-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="fce10-139">Specifica le dimensioni dei dischi di dati in GB.</span><span class="sxs-lookup"><span data-stu-id="fce10-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="fce10-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce10-140">-DefaultProfile</span></span>
<span data-ttu-id="fce10-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fce10-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce10-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="fce10-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="fce10-143">Indica che questo cmdlet non installa l'estensione **Info BG** nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="fce10-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="fce10-144">-DiskFile</span></span>
<span data-ttu-id="fce10-145">Il percorso locale del file del disco rigido virtuale da caricare nel cloud e per creare la VM e deve avere il suffisso ". VHD".</span><span class="sxs-lookup"><span data-stu-id="fce10-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="fce10-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fce10-146">-DomainNameLabel</span></span>
<span data-ttu-id="fce10-147">L'etichetta del sottodominio per il nome di dominio completo (FQDN) della VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="fce10-148">Il modulo sarà necessario `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="fce10-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="fce10-149">-Immagine</span><span class="sxs-lookup"><span data-stu-id="fce10-149">-Image</span></span>
<span data-ttu-id="fce10-150">Il nome dell'immagine amichevole su cui verrà compilata la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="fce10-151">Questi includono: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, coreos, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="fce10-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="fce10-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fce10-152">-LicenseType</span></span>
<span data-ttu-id="fce10-153">Specifica un tipo di licenza, che indica che l'immagine o il disco per la macchina virtuale è stato concesso in licenza locale.</span><span class="sxs-lookup"><span data-stu-id="fce10-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="fce10-154">Questo valore viene usato solo per le immagini che contengono il sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fce10-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="fce10-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fce10-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fce10-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="fce10-156">Windows_Client</span></span>
- <span data-ttu-id="fce10-157">Windows_Server questo valore non può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fce10-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="fce10-158">Se specifichi questo parametro per un aggiornamento, il valore deve corrispondere al valore iniziale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="fce10-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="fce10-159">-Linux</span></span>
<span data-ttu-id="fce10-160">Indica se il file su disco è per Linux VM, se specificato; o Windows, se non specificato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fce10-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="fce10-161">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fce10-161">-Location</span></span>
<span data-ttu-id="fce10-162">Specifica un percorso per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="fce10-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="fce10-163">-Name</span></span>
<span data-ttu-id="fce10-164">Il nome della risorsa VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="fce10-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="fce10-165">-OpenPorts</span></span>
<span data-ttu-id="fce10-166">Un elenco di porte da aprire nel gruppo di sicurezza della rete (NSG) per la VM creata.</span><span class="sxs-lookup"><span data-stu-id="fce10-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="fce10-167">Il valore predefinito dipende dal tipo di immagine scelto (ad esempio, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="fce10-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="fce10-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fce10-168">-PublicIpAddressName</span></span>
<span data-ttu-id="fce10-169">Nome di un nuovo indirizzo IP pubblico (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="fce10-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="fce10-170">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="fce10-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="fce10-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce10-171">-ResourceGroupName</span></span>
<span data-ttu-id="fce10-172">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fce10-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fce10-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fce10-173">-SecurityGroupName</span></span>
<span data-ttu-id="fce10-174">Il nome di un nuovo (o esistente) gruppo di sicurezza di rete (NSG) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="fce10-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="fce10-175">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="fce10-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="fce10-176">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="fce10-176">-Size</span></span>
<span data-ttu-id="fce10-177">Dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="fce10-178">Il valore predefinito è: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="fce10-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="fce10-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fce10-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="fce10-180">Prefisso dell'indirizzo per la subnet che verrà creata per la VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="fce10-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fce10-181">-SubnetName</span></span>
<span data-ttu-id="fce10-182">Nome di una nuova subnet (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="fce10-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="fce10-183">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="fce10-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="fce10-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fce10-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fce10-185">Se il parametro è presente, alla VM viene assegnata un'identità di sistema gestita generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fce10-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="fce10-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="fce10-186">-Tag</span></span>
<span data-ttu-id="fce10-187">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="fce10-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="fce10-188">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="fce10-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="fce10-189">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="fce10-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="fce10-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fce10-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="fce10-191">Il nome di un'identità del servizio gestito che deve essere assegnata alla VM.</span><span class="sxs-lookup"><span data-stu-id="fce10-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="fce10-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fce10-192">-VirtualNetworkName</span></span>
<span data-ttu-id="fce10-193">Nome di una nuova rete virtuale (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="fce10-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="fce10-194">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="fce10-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="fce10-195">-VM</span><span class="sxs-lookup"><span data-stu-id="fce10-195">-VM</span></span>
<span data-ttu-id="fce10-196">Specifica una macchina virtuale locale da creare.</span><span class="sxs-lookup"><span data-stu-id="fce10-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="fce10-197">Per ottenere un oggetto macchina virtuale, usare il cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="fce10-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="fce10-198">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="fce10-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="fce10-199">-Zona</span><span class="sxs-lookup"><span data-stu-id="fce10-199">-Zone</span></span>
<span data-ttu-id="fce10-200">Specifica l'elenco delle aree della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fce10-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="fce10-201">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fce10-201">-Confirm</span></span>
<span data-ttu-id="fce10-202">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce10-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce10-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce10-203">-WhatIf</span></span>
<span data-ttu-id="fce10-204">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fce10-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fce10-205">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fce10-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce10-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce10-206">CommonParameters</span></span>
<span data-ttu-id="fce10-207">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce10-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce10-208">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce10-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce10-209">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fce10-209">INPUTS</span></span>

### <span data-ttu-id="fce10-210">System. String</span><span class="sxs-lookup"><span data-stu-id="fce10-210">System.String</span></span>

### <span data-ttu-id="fce10-211">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fce10-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fce10-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="fce10-212">System.String[]</span></span>

### <span data-ttu-id="fce10-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fce10-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fce10-214">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fce10-214">OUTPUTS</span></span>

### <span data-ttu-id="fce10-215">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fce10-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="fce10-216">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fce10-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fce10-217">Note</span><span class="sxs-lookup"><span data-stu-id="fce10-217">NOTES</span></span>

## <span data-ttu-id="fce10-218">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fce10-218">RELATED LINKS</span></span>

[<span data-ttu-id="fce10-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="fce10-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="fce10-221">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="fce10-222">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="fce10-223">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="fce10-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fce10-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="fce10-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fce10-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="fce10-226">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fce10-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="fce10-227">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="fce10-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="fce10-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fce10-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="fce10-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="fce10-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="fce10-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="fce10-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


