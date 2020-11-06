---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521748"
---
# <span data-ttu-id="7f5c4-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-101">New-AzureRmVM</span></span>

## <span data-ttu-id="7f5c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5c4-103">Crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f5c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f5c4-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f5c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5c4-106">Il cmdlet **New-AzureRmVM** crea una macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="7f5c4-107">Questo cmdlet accetta come input un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="7f5c4-108">Usa il cmdlet New-AzureRmVMConfig per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="7f5c4-109">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="7f5c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f5c4-110">EXAMPLES</span></span>

### <span data-ttu-id="7f5c4-111">Esempio 1: creare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f5c4-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="7f5c4-112">Questo script di esempio Mostra come creare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="7f5c4-113">Questo script usa diversi altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="7f5c4-114">Esempio 2: creare una macchina virtuale da un'immagine utente personalizzata</span><span class="sxs-lookup"><span data-stu-id="7f5c4-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="7f5c4-115">Questo esempio accetta un'immagine di sistema operativo personalizzata preimpostata, generalizzata e fissa un disco di dati, applica una nuova rete, distribuisce il disco rigido virtuale e lo esegue.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="7f5c4-116">Questo script può essere usato per il provisioning automatico perché usa le credenziali di amministratore della macchina virtuale locale in linea invece di chiamare **Get-Credential** che richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="7f5c4-117">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="7f5c4-118">Puoi confermare lo stato di accesso usando il cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="7f5c4-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="7f5c4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f5c4-119">PARAMETERS</span></span>

### <span data-ttu-id="7f5c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5c4-120">-DefaultProfile</span></span>
<span data-ttu-id="7f5c4-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f5c4-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="7f5c4-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="7f5c4-123">Indica che questo cmdlet non installa l'estensione **Info BG** nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="7f5c4-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7f5c4-124">-LicenseType</span></span>
<span data-ttu-id="7f5c4-125">Specifica un tipo di licenza, che indica che l'immagine o il disco per la macchina virtuale è stato concesso in licenza locale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="7f5c4-126">Questo valore viene usato solo per le immagini che contengono il sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="7f5c4-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f5c4-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f5c4-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="7f5c4-128">Windows_Client</span></span> 
- <span data-ttu-id="7f5c4-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="7f5c4-129">Windows_Server</span></span>

<span data-ttu-id="7f5c4-130">Questo valore non può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-130">This value cannot be updated.</span></span>
<span data-ttu-id="7f5c4-131">Se specifichi questo parametro per un aggiornamento, il valore deve corrispondere al valore iniziale per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f5c4-132">-Location</span></span>
<span data-ttu-id="7f5c4-133">Specifica un percorso per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-133">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f5c4-134">-ResourceGroupName</span></span>
<span data-ttu-id="7f5c4-135">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-135">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f5c4-136">-Tags</span></span>
<span data-ttu-id="7f5c4-137">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="7f5c4-138">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="7f5c4-139">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-140">-VM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-140">-VM</span></span>
<span data-ttu-id="7f5c4-141">Specifica una macchina virtuale locale da creare.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="7f5c4-142">Per ottenere un oggetto macchina virtuale, usare il cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="7f5c4-143">Altri cmdlet possono essere usati per configurare la macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage e Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-144">-Zona</span><span class="sxs-lookup"><span data-stu-id="7f5c4-144">-Zone</span></span>
<span data-ttu-id="7f5c4-145">Specifica l'elenco delle aree della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5c4-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f5c4-146">-Confirm</span></span>
<span data-ttu-id="7f5c4-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f5c4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f5c4-148">-WhatIf</span></span>
<span data-ttu-id="7f5c4-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f5c4-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f5c4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5c4-151">CommonParameters</span></span>
<span data-ttu-id="7f5c4-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5c4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5c4-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f5c4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5c4-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f5c4-154">INPUTS</span></span>

## <span data-ttu-id="7f5c4-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f5c4-155">OUTPUTS</span></span>

## <span data-ttu-id="7f5c4-156">Note</span><span class="sxs-lookup"><span data-stu-id="7f5c4-156">NOTES</span></span>

## <span data-ttu-id="7f5c4-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f5c4-157">RELATED LINKS</span></span>

[<span data-ttu-id="7f5c4-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7f5c4-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="7f5c4-160">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="7f5c4-161">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="7f5c4-162">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="7f5c4-163">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f5c4-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="7f5c4-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7f5c4-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="7f5c4-165">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7f5c4-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="7f5c4-166">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="7f5c4-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="7f5c4-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7f5c4-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="7f5c4-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7f5c4-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="7f5c4-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="7f5c4-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


