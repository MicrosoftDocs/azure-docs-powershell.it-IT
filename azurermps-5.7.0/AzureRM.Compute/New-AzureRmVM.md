---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509988"
---
# <span data-ttu-id="b273a-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-101">New-AzureRmVM</span></span>

## <span data-ttu-id="b273a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b273a-102">SYNOPSIS</span></span>
<span data-ttu-id="b273a-103">Crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b273a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b273a-104">SYNTAX</span></span>

### <span data-ttu-id="b273a-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b273a-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b273a-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b273a-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b273a-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b273a-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b273a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b273a-108">DESCRIPTION</span></span>
<span data-ttu-id="b273a-109">Il cmdlet **New-AzureRmVM** crea una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="b273a-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="b273a-110">Questo cmdlet accetta come input un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="b273a-111">Usa il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="b273a-112">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="b273a-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="b273a-113">`SimpleParameterSet`Fornisce un metodo pratico per creare una VM rendendo facoltativi gli argomenti della creazione di VM comuni.</span><span class="sxs-lookup"><span data-stu-id="b273a-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="b273a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b273a-114">EXAMPLES</span></span>

### <span data-ttu-id="b273a-115">Esempio 1: creare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b273a-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="b273a-116">Questo script di esempio Mostra come creare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="b273a-117">Lo script richiederà un nome utente e una password per la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="b273a-118">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b273a-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="b273a-119">Esempio 2: creare una macchina virtuale da un'immagine utente personalizzata</span><span class="sxs-lookup"><span data-stu-id="b273a-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="b273a-120">Questo esempio accetta un'immagine di sistema operativo personalizzata preimpostata, generalizzata e fissa un disco di dati, applica una nuova rete, distribuisce il disco rigido virtuale e lo esegue.</span><span class="sxs-lookup"><span data-stu-id="b273a-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="b273a-121">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b273a-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="b273a-122">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="b273a-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="b273a-123">Puoi confermare lo stato di accesso usando il cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="b273a-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="b273a-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b273a-124">PARAMETERS</span></span>

### <span data-ttu-id="b273a-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b273a-125">-AddressPrefix</span></span>
<span data-ttu-id="b273a-126">Il prefisso dell'indirizzo per la rete virtuale che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b273a-127">-AllocationMethod</span></span>
<span data-ttu-id="b273a-128">Metodo di allocazione IP per l'IP pubblico che verrà creato per la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b273a-129">-AsJob</span></span>
<span data-ttu-id="b273a-130">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b273a-130">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b273a-131">-AvailabilitySetName</span></span>
<span data-ttu-id="b273a-132">Specifica un nome per il set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="b273a-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-133">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="b273a-133">-Credential</span></span>
<span data-ttu-id="b273a-134">Le credenziali di amministratore per la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-134">The administrator credentials for the VM.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b273a-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="b273a-136">Specifica le dimensioni dei dischi di dati in GB.</span><span class="sxs-lookup"><span data-stu-id="b273a-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b273a-137">-DefaultProfile</span></span>
<span data-ttu-id="b273a-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b273a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="b273a-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="b273a-140">Indica che questo cmdlet non installa l'estensione **Info BG** nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="b273a-141">-DiskFile</span></span>
<span data-ttu-id="b273a-142">Il percorso locale del file del disco rigido virtuale da caricare nel cloud e per creare la VM e deve avere il suffisso ". VHD".</span><span class="sxs-lookup"><span data-stu-id="b273a-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b273a-143">-DomainNameLabel</span></span>
<span data-ttu-id="b273a-144">L'etichetta del sottodominio per il nome di dominio completo (FQDN) della VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="b273a-145">Il modulo sarà necessario `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="b273a-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b273a-146">-ImageName</span></span>
<span data-ttu-id="b273a-147">Il nome dell'immagine amichevole su cui verrà compilata la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="b273a-148">Questi includono: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, coreos, Debian, openSUSE-LEAP, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="b273a-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b273a-149">-LicenseType</span></span>
<span data-ttu-id="b273a-150">Specifica un tipo di licenza, che indica che l'immagine o il disco per la macchina virtuale è stato concesso in licenza locale.</span><span class="sxs-lookup"><span data-stu-id="b273a-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="b273a-151">Questo valore viene usato solo per le immagini che contengono il sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b273a-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="b273a-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b273a-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b273a-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b273a-153">Windows_Client</span></span>
- <span data-ttu-id="b273a-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="b273a-154">Windows_Server</span></span>

<span data-ttu-id="b273a-155">Questo valore non può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b273a-155">This value cannot be updated.</span></span>
<span data-ttu-id="b273a-156">Se specifichi questo parametro per un aggiornamento, il valore deve corrispondere al valore iniziale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="b273a-157">-Linux</span></span>
<span data-ttu-id="b273a-158">Indica se il file su disco è per Linux VM, se specificato; o Windows, se non specificato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b273a-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-159">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b273a-159">-Location</span></span>
<span data-ttu-id="b273a-160">Specifica un percorso per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="b273a-161">-Name</span></span>
<span data-ttu-id="b273a-162">Il nome della risorsa VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="b273a-163">-OpenPorts</span></span>
<span data-ttu-id="b273a-164">Un elenco di porte da aprire nel gruppo di sicurezza della rete (NSG) per la VM creata.</span><span class="sxs-lookup"><span data-stu-id="b273a-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="b273a-165">Il valore predefinito dipende dal tipo di immagine scelto (ad esempio, Windows: 3389, 5985 e Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="b273a-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="b273a-166">-PublicIpAddressName</span></span>
<span data-ttu-id="b273a-167">Nome di un nuovo indirizzo IP pubblico (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="b273a-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="b273a-168">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="b273a-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b273a-169">-ResourceGroupName</span></span>
<span data-ttu-id="b273a-170">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b273a-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b273a-171">-SecurityGroupName</span></span>
<span data-ttu-id="b273a-172">Il nome di un nuovo (o esistente) gruppo di sicurezza di rete (NSG) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="b273a-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="b273a-173">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="b273a-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-174">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="b273a-174">-Size</span></span>
<span data-ttu-id="b273a-175">Dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="b273a-176">Il valore predefinito è: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="b273a-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b273a-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="b273a-178">Prefisso dell'indirizzo per la subnet che verrà creata per la VM.</span><span class="sxs-lookup"><span data-stu-id="b273a-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b273a-179">-SubnetName</span></span>
<span data-ttu-id="b273a-180">Nome di una nuova subnet (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="b273a-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="b273a-181">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="b273a-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="b273a-182">-Tag</span></span>
<span data-ttu-id="b273a-183">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="b273a-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b273a-184">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="b273a-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b273a-185">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="b273a-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b273a-186">-VirtualNetworkName</span></span>
<span data-ttu-id="b273a-187">Nome di una nuova rete virtuale (o esistente) per la VM creata da usare.</span><span class="sxs-lookup"><span data-stu-id="b273a-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="b273a-188">Se non specificato, verrà generato un nome.</span><span class="sxs-lookup"><span data-stu-id="b273a-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-189">-VM</span><span class="sxs-lookup"><span data-stu-id="b273a-189">-VM</span></span>
<span data-ttu-id="b273a-190">Specifica una macchina virtuale locale da creare.</span><span class="sxs-lookup"><span data-stu-id="b273a-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="b273a-191">Per ottenere un oggetto macchina virtuale, usare il cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="b273a-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="b273a-192">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="b273a-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-193">-Zona</span><span class="sxs-lookup"><span data-stu-id="b273a-193">-Zone</span></span>
<span data-ttu-id="b273a-194">Specifica l'elenco delle aree della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b273a-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-195">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b273a-195">-Confirm</span></span>
<span data-ttu-id="b273a-196">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b273a-196">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b273a-197">-WhatIf</span></span>
<span data-ttu-id="b273a-198">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b273a-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b273a-199">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b273a-199">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b273a-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b273a-200">CommonParameters</span></span>
<span data-ttu-id="b273a-201">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b273a-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b273a-202">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b273a-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b273a-203">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b273a-203">INPUTS</span></span>

### <span data-ttu-id="b273a-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b273a-204">PSVirtualMachine</span></span>
<span data-ttu-id="b273a-205">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b273a-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="b273a-206">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b273a-206">OUTPUTS</span></span>

### <span data-ttu-id="b273a-207">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b273a-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b273a-208">Note</span><span class="sxs-lookup"><span data-stu-id="b273a-208">NOTES</span></span>

## <span data-ttu-id="b273a-209">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b273a-209">RELATED LINKS</span></span>

[<span data-ttu-id="b273a-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b273a-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b273a-212">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b273a-213">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b273a-214">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b273a-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b273a-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="b273a-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b273a-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="b273a-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b273a-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="b273a-218">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b273a-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="b273a-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b273a-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="b273a-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="b273a-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="b273a-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b273a-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


