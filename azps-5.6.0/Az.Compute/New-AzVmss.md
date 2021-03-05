---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: f80441cb3555d78974c5a838e829cb2ab350183f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988440"
---
# <span data-ttu-id="a9808-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-101">New-AzVmss</span></span>

## <span data-ttu-id="a9808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9808-102">SYNOPSIS</span></span>
<span data-ttu-id="a9808-103">Crea un VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9808-103">Creates a VMSS.</span></span>

## <span data-ttu-id="a9808-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9808-104">SYNTAX</span></span>

### <span data-ttu-id="a9808-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="a9808-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9808-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9808-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9808-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9808-107">DESCRIPTION</span></span>
<span data-ttu-id="a9808-108">Il cmdlet **New-AzVmss crea** un set di scalabilità delle macchine virtuali (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="a9808-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="a9808-109">Usare il set di parametri semplice ( ) per `SimpleParameterSet` creare rapidamente un VMSS pre-impostato e risorse associate.</span><span class="sxs-lookup"><span data-stu-id="a9808-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="a9808-110">Usare il set di parametri predefinito ( ) per scenari più avanzati quando è necessario configurare con precisione ogni componente del sistema VMSS e ogni risorsa associata `DefaultParameter` prima della creazione.</span><span class="sxs-lookup"><span data-stu-id="a9808-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="a9808-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9808-111">EXAMPLES</span></span>

### <span data-ttu-id="a9808-112">Esempio 1: creare un VMSS usando il **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a9808-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="a9808-113">Il comando precedente crea quanto segue con il `$vmssName` nome:</span><span class="sxs-lookup"><span data-stu-id="a9808-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="a9808-114">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a9808-114">A Resource Group</span></span>
* <span data-ttu-id="a9808-115">Una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a9808-115">A virtual network</span></span>
* <span data-ttu-id="a9808-116">Servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a9808-116">A load balancer</span></span>
* <span data-ttu-id="a9808-117">Un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a9808-117">A public IP</span></span>
* <span data-ttu-id="a9808-118">VMSS con 2 istanze</span><span class="sxs-lookup"><span data-stu-id="a9808-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="a9808-119">L'immagine predefinita scelta per le macchine virtuali nel sistema VMSS è `2016-Datacenter Windows Server` e lo SKU è `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="a9808-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="a9808-120">Esempio 2: crea un VMSS utilizzando il **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a9808-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="a9808-121">Nell'esempio complesso riportato sopra viene creato un VMSS, di seguito è riportata una spiegazione di quello che accade:</span><span class="sxs-lookup"><span data-stu-id="a9808-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="a9808-122">Il primo comando crea un gruppo di risorse con il nome e il percorso specificati.</span><span class="sxs-lookup"><span data-stu-id="a9808-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="a9808-123">Il secondo comando usa il cmdlet **New-AzStorageAccount** per creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a9808-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="a9808-124">Il terzo comando usa quindi il cmdlet **Get-AzStorageAccount** per ottenere l'account di archiviazione creato nel secondo comando e archivia il risultato nella $STOAccount variabile.</span><span class="sxs-lookup"><span data-stu-id="a9808-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="a9808-125">Il quinto comando usa il cmdlet **New-AzVirtualNetworkSubnetConfig** per creare una subnet e archiviare il risultato nella variabile $SubNet.</span><span class="sxs-lookup"><span data-stu-id="a9808-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="a9808-126">Il sesto comando usa il cmdlet **New-AzVirtualNetwork** per creare una rete virtuale e archivia il risultato nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="a9808-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="a9808-127">Il settimo comando usa **Get-AzVirtualNetwork** per ottenere informazioni sulla rete virtuale creata nel sesto comando e le archivia nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="a9808-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="a9808-128">L'ottavo e il nono comando usa **New-AzPublicIpAddress** e **Get- AzureRmPublicIpAddress** per creare e ottenere informazioni da tale indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a9808-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="a9808-129">I comandi archiviano le informazioni nella variabile denominata $PubIP.</span><span class="sxs-lookup"><span data-stu-id="a9808-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="a9808-130">Il decimo comando usa il cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** per creare una bilanciamento del carico frontend e archivia il risultato nella variabile $Frontend.</span><span class="sxs-lookup"><span data-stu-id="a9808-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="a9808-131">L'undicesimo comando usa **New-AzLoadBalancerBackendAddressPoolConfig** per creare una configurazione del pool di indirizzi back-end e archivia il risultato nella variabile $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="a9808-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="a9808-132">Il dodicesimo comando usa **New-AzLoadBalancerProbeConfig** per creare una classe e archiviare le informazioni relative all'ambiente nella variabile $Probe.</span><span class="sxs-lookup"><span data-stu-id="a9808-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="a9808-133">Il tredicesimo comando usa il cmdlet **New-AzLoadBalancerInboundNatPoolConfig per** creare una configurazione di pool NAT (Network Address Translation) in ingresso di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a9808-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="a9808-134">Il quattordicesimo comando usa **New-AzLoadBalancerRuleConfig** per creare una configurazione di regola di bilanciamento del carico e archivia il risultato nella variabile $LBRule.</span><span class="sxs-lookup"><span data-stu-id="a9808-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="a9808-135">Il quindicesimo comando usa il cmdlet **New-AzLoadBalancer** per creare una bilanciamento del carico e archivia il risultato nella variabile $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="a9808-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="a9808-136">Il sediciesimo comando usa **Get-AzLoadBalancer** per ottenere informazioni sulla bilanciamento del carico creata nel quindicesimo comando e archivia le informazioni nella variabile $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="a9808-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="a9808-137">Il diciassettesesimo comando usa il cmdlet **New-AzVmssIPConfig** per creare una configurazione IP VMSS e archivia le informazioni nella variabile denominata $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="a9808-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="a9808-138">Il diciottesimo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione VMSS e archivia il risultato nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9808-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="a9808-139">Il comando #D0 /c0 #D1 usa il cmdlet **New-AzVmss** per creare VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9808-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="a9808-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9808-140">PARAMETERS</span></span>

### <span data-ttu-id="a9808-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="a9808-141">-AllocationMethod</span></span>
<span data-ttu-id="a9808-142">Metodo di allocazione per l'indirizzo IP pubblico del set di scale (statico o dinamico).</span><span class="sxs-lookup"><span data-stu-id="a9808-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="a9808-143">Se non viene fornito alcun valore, l'allocazione sarà statica.</span><span class="sxs-lookup"><span data-stu-id="a9808-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9808-144">-AsJob</span></span>
<span data-ttu-id="a9808-145">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a9808-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a9808-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="a9808-146">-BackendPoolName</span></span>
<span data-ttu-id="a9808-147">Nome del pool di indirizzi back-end da usare nella bilanciamento del carico per questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="a9808-148">Se non viene fornito alcun valore, verrà creato un nuovo pool back-end con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a9808-149">-BackendPort</span></span>
<span data-ttu-id="a9808-150">Numeri di porta back-end usati dal servizio di bilanciamento del carico set di scala per comunicare con le macchine virtuali nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="a9808-151">Se non si specifica alcun valore, verranno usate le porte 3389 e 5985 per Windows VMS e la porta 22 per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="a9808-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="a9808-152">-Credential</span></span>
<span data-ttu-id="a9808-153">Credenziali di amministratore (nome utente e password) per le macchine virtuali in questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="a9808-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a9808-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="a9808-155">Specifica le dimensioni dei dischi dati in GB.</span><span class="sxs-lookup"><span data-stu-id="a9808-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9808-156">-DefaultProfile</span></span>
<span data-ttu-id="a9808-157">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9808-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9808-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a9808-158">-DomainNameLabel</span></span>
<span data-ttu-id="a9808-159">Etichetta del nome di dominio per il nome di Fully-Qualified (FQDN) del set di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="a9808-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="a9808-160">Primo componente del nome di dominio assegnato automaticamente al set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="a9808-161">I nomi di dominio assegnati automaticamente usano il formato ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a9808-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="a9808-162">Se non viene fornito alcun valore, l'etichetta predefinita del nome di dominio sarà la concatenazione di <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="a9808-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-163">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="a9808-163">-EnableUltraSSD</span></span>
<span data-ttu-id="a9808-164">Usare dischi UltraSSD per le macchine virtuali nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="a9808-165">-EncryptionAtHost</span></span>
<span data-ttu-id="a9808-166">Questo parametro abiliterà la crittografia per tutti i dischi, incluso il disco Risorsa/Temp nell'host stesso.</span><span class="sxs-lookup"><span data-stu-id="a9808-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="a9808-167">Impostazione predefinita: la crittografia nell'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a9808-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="a9808-168">-EvictionPolicy</span></span>
<span data-ttu-id="a9808-169">Criterio di sgomento per il set di scalabilità delle macchine virtuali con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="a9808-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="a9808-170">Solo i valori supportati sono "Deassegnazione" ed "Elimina".</span><span class="sxs-lookup"><span data-stu-id="a9808-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="a9808-171">-FrontendPoolName</span></span>
<span data-ttu-id="a9808-172">Nome del pool di indirizzi frontend da usare nella bilanciamento del carico set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="a9808-173">Se non viene fornito alcun valore, verrà creato un nuovo pool di indirizzi Frontend con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="a9808-174">-HostGroupId</span></span>
<span data-ttu-id="a9808-175">Specifica il gruppo host dedicato in cui risiederà il set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9808-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a9808-176">-ImageName</span></span>
<span data-ttu-id="a9808-177">Nome dell'immagine per le macchine virtuali in questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="a9808-178">Se non viene fornito alcun valore, verrà usata l'immagine "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="a9808-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a9808-179">-InstanceCount</span></span>
<span data-ttu-id="a9808-180">Il numero di immagini della macchina virtuale nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="a9808-181">Se non viene fornito alcun valore, verranno create 2 istanze.</span><span class="sxs-lookup"><span data-stu-id="a9808-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a9808-182">-LoadBalancerName</span></span>
<span data-ttu-id="a9808-183">Nome della bilanciamento del carico da usare con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="a9808-184">Se non si imposta alcun valore, verrà creata una nuova bilanciamento del carico con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-185">-Location</span><span class="sxs-lookup"><span data-stu-id="a9808-185">-Location</span></span>
<span data-ttu-id="a9808-186">Posizione di Azure in cui verrà creato il set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="a9808-187">Se non viene specificato alcun valore, la posizione verrà dedotto dalla posizione delle altre risorse a cui si fa riferimento nei parametri.</span><span class="sxs-lookup"><span data-stu-id="a9808-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="a9808-188">-MaxPrice</span></span>
<span data-ttu-id="a9808-189">Prezzo massimo per la fatturazione di un set di scalabilità delle macchine virtuali con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="a9808-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="a9808-190">-NatBackendPort</span></span>
<span data-ttu-id="a9808-191">Porta back-end per la traduzione degli indirizzi di rete in ingresso.</span><span class="sxs-lookup"><span data-stu-id="a9808-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="a9808-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="a9808-193">Fault Domain count for each placement group.</span><span class="sxs-lookup"><span data-stu-id="a9808-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-194">-Priority</span><span class="sxs-lookup"><span data-stu-id="a9808-194">-Priority</span></span>
<span data-ttu-id="a9808-195">Priorità della macchina virtuale nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="a9808-196">Solo i valori supportati sono "Normale", "Posizione" e "Basso".</span><span class="sxs-lookup"><span data-stu-id="a9808-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="a9808-197">"Normale" è per la macchina virtuale normale.</span><span class="sxs-lookup"><span data-stu-id="a9808-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="a9808-198">"Spot" è per una macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="a9808-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="a9808-199">"Low" è anche per la macchina virtuale spot, ma viene sostituito da "Spot".</span><span class="sxs-lookup"><span data-stu-id="a9808-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="a9808-200">Usare "Spot" invece di "Low".</span><span class="sxs-lookup"><span data-stu-id="a9808-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a9808-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a9808-202">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="a9808-203">-PublicIpAddressName</span></span>
<span data-ttu-id="a9808-204">Nome dell'indirizzo IP pubblico da usare con questo set di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="a9808-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="a9808-205">Se non viene fornito alcun valore, verrà creato un nuovo IPAddress pubblico con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9808-206">-ResourceGroupName</span></span>
<span data-ttu-id="a9808-207">Specifica il nome del gruppo di risorse del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="a9808-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="a9808-208">Se non viene specificato alcun valore, verrà creato un nuovo Gruppo di risorse con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="a9808-209">-ScaleInPolicy</span></span>
<span data-ttu-id="a9808-210">Regole da seguire quando si ridimensiona un set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a9808-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="a9808-211">I valori possibili sono " Default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="a9808-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="a9808-212">"Impostazione predefinita" quando un set di scalabilità delle macchine virtuali viene ridimensionato, viene prima bilanciato tra le aree, se si tratta di un set di scala di zona.</span><span class="sxs-lookup"><span data-stu-id="a9808-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="a9808-213">Quindi, verrà bilanciato il più possibile tra i domini di errore.</span><span class="sxs-lookup"><span data-stu-id="a9808-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="a9808-214">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno le più recenti non protette dalla scalabilità.</span><span class="sxs-lookup"><span data-stu-id="a9808-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="a9808-215">Quando il set di scale di una macchina virtuale viene ridimensionato, per la rimozione vengono scelte le macchine virtuali meno recenti che non sono protette dal scale-in.</span><span class="sxs-lookup"><span data-stu-id="a9808-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="a9808-216">Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.</span><span class="sxs-lookup"><span data-stu-id="a9808-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="a9808-217">All'interno di ogni area vengono scelte le macchine virtuali meno recenti non protette per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="a9808-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="a9808-218">Nel caso di un set di scale per macchine virtuali in fase di ridimensionamento, per la rimozione verranno scelte le macchine virtuali più recenti non protette dal scale-in.</span><span class="sxs-lookup"><span data-stu-id="a9808-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="a9808-219">Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.</span><span class="sxs-lookup"><span data-stu-id="a9808-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="a9808-220">All'interno di ogni area vengono scelte le macchine virtuali più recenti non protette per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="a9808-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="a9808-221">-SecurityGroupName</span></span>
<span data-ttu-id="a9808-222">Nome del gruppo di sicurezza di rete da applicare a questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="a9808-223">Se non viene fornito alcun valore, verrà creato e applicato al set di scale un gruppo di sicurezza di rete predefinito con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a9808-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="a9808-225">Usare questa opzione per creare il set di scale in un singolo gruppo di posizionamento, il valore predefinito è più gruppi</span><span class="sxs-lookup"><span data-stu-id="a9808-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="a9808-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="a9808-227">Specifica che le estensioni non vengono eseguite nelle macchine virtuali con overprovisioning aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a9808-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9808-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="a9808-229">Prefisso dell'indirizzo della subnet che verrà utilizzata da questo ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="a9808-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="a9808-230">Le impostazioni predefinite della subnet (192.168.1.0/24) verranno applicate se non viene fornito alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a9808-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a9808-231">-SubnetName</span></span>
<span data-ttu-id="a9808-232">Nome della subnet da usare con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="a9808-233">Se non viene specificato alcun valore, verrà creata una nuova subnet con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a9808-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a9808-235">Se il parametro è presente, alle macchine virtuali nel set di scalabilità viene (o sono) assegnate un'identità di sistema gestita generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a9808-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a9808-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="a9808-237">Modalità dei criteri di aggiornamento per le istanze di VM in questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="a9808-238">I criteri di aggiornamento possono specificare aggiornamenti automatici, manuali o in sequenza.</span><span class="sxs-lookup"><span data-stu-id="a9808-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a9808-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="a9808-240">Nome di un'identità del servizio gestito che deve essere assegnata alle macchine virtuali nel set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9808-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a9808-242">Specifica **l'oggetto VirtualMachineScaleSet** che contiene le proprietà del sistema VMSS creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9808-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a9808-243">-VirtualNetworkName</span></span>
<span data-ttu-id="a9808-244">Il nome della rete virtuale da usare con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="a9808-245">Se non viene fornito alcun valore, verrà creata una nuova rete virtuale con lo stesso nome del set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a9808-246">-VMScaleSetName</span></span>
<span data-ttu-id="a9808-247">Specifica il nome del sistema VMS creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9808-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a9808-248">-VmSize</span></span>
<span data-ttu-id="a9808-249">Le dimensioni delle istanze della macchina virtuale in questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="a9808-250">Se non si Standard_DS1_v2 Size, verrà usata una dimensione predefinita (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="a9808-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9808-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="a9808-252">Prefisso dell'indirizzo della rete virtuale usata con questo set di scale.</span><span class="sxs-lookup"><span data-stu-id="a9808-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="a9808-253">Le impostazioni predefinite per i prefissi degli indirizzi di rete virtuale (192.168.0.0/16) verranno usate se non viene fornito alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a9808-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="a9808-254">-Zone</span></span>
<span data-ttu-id="a9808-255">Elenco di aree di disponibilità che denota l'indirizzo IP allocato per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a9808-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9808-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9808-256">-Confirm</span></span>
<span data-ttu-id="a9808-257">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9808-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9808-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9808-258">-WhatIf</span></span>
<span data-ttu-id="a9808-259">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9808-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9808-260">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9808-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9808-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9808-261">CommonParameters</span></span>
<span data-ttu-id="a9808-262">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9808-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9808-263">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9808-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9808-264">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9808-264">INPUTS</span></span>

### <span data-ttu-id="a9808-265">System.String</span><span class="sxs-lookup"><span data-stu-id="a9808-265">System.String</span></span>

### <span data-ttu-id="a9808-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9808-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a9808-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9808-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9808-268">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9808-268">OUTPUTS</span></span>

### <span data-ttu-id="a9808-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a9808-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a9808-270">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9808-270">NOTES</span></span>

## <span data-ttu-id="a9808-271">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9808-271">RELATED LINKS</span></span>

[<span data-ttu-id="a9808-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a9808-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a9808-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a9808-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a9808-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a9808-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="a9808-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a9808-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


