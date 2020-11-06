---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507588"
---
# <span data-ttu-id="a3c4a-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="a3c4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c4a-103">Crea un VMSS.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3c4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3c4a-104">SYNTAX</span></span>

### <span data-ttu-id="a3c4a-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3c4a-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c4a-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c4a-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c4a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="a3c4a-108">Il cmdlet **New-AzureRmVmss** crea un set di scale della macchina virtuale (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="a3c4a-109">Usa il set di parametri Simple ( `SimpleParameterSet` ) per creare rapidamente una vmss preimpostata e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="a3c4a-110">Usa il set di parametri predefinito ( `DefaultParameter` ) per scenari più avanzati quando devi configurare con precisione ogni componente di vmss e ogni risorsa associata prima della creazione.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="a3c4a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3c4a-111">EXAMPLES</span></span>

### <span data-ttu-id="a3c4a-112">Esempio 1: creare un VMSS usando il **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a3c4a-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="a3c4a-113">Il comando precedente crea il seguente nome `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="a3c4a-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="a3c4a-114">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a3c4a-114">A Resource Group</span></span>
* <span data-ttu-id="a3c4a-115">Una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a3c4a-115">A virtual network</span></span>
* <span data-ttu-id="a3c4a-116">Un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a3c4a-116">A load balancer</span></span>
* <span data-ttu-id="a3c4a-117">Un IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a3c4a-117">A public IP</span></span>
* <span data-ttu-id="a3c4a-118">VMSS con 2 istanze</span><span class="sxs-lookup"><span data-stu-id="a3c4a-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="a3c4a-119">L'immagine predefinita scelta per le VM in VMSS è `2016-Datacenter Windows Server` e l'USK è `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="a3c4a-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="a3c4a-120">Esempio 2: creare un VMSS usando il **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a3c4a-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="a3c4a-121">L'esempio complesso precedente crea un VMSS, in seguito è una spiegazione di quanto sta accadendo:</span><span class="sxs-lookup"><span data-stu-id="a3c4a-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="a3c4a-122">Il primo comando crea un gruppo di risorse con il nome e il percorso specificati.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="a3c4a-123">Il secondo comando usa il cmdlet **New-AzureRmStorageAccount** per creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-123">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="a3c4a-124">Il terzo comando usa quindi il cmdlet **Get-AzureRmStorageAccount** per ottenere l'account di archiviazione creato nel secondo comando e archivia il risultato nella variabile $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-124">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="a3c4a-125">Il quinto comando usa il cmdlet **New-AzureRmVirtualNetworkSubnetConfig** per creare una subnet e archivia il risultato nella variabile denominata $subnet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-125">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="a3c4a-126">Il sesto comando usa il cmdlet **New-AzureRmVirtualNetwork** per creare una rete virtuale e archivia il risultato nella variabile denominata $VNet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-126">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="a3c4a-127">Il settimo comando USA **Get-AzureRmVirtualNetwork** per ottenere informazioni sulla rete virtuale creata nel sesto comando e archivia le informazioni nella variabile denominata $VNet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-127">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="a3c4a-128">Il comando ottavo e nono usa la **nuova-AzureRmPublicIpAddress** e **Get-AzureRmPublicIpAddress** per creare e ottenere informazioni da tale indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-128">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="a3c4a-129">I comandi archiviano le informazioni nella variabile denominata $PubIP.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="a3c4a-130">Il decimo comando usa il cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** per creare un bilanciamento del carico frontend e archivia il risultato nella variabile denominata $frontend.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="a3c4a-131">L'undicesimo comando usa il **nuovo-AzureRmLoadBalancerBackendAddressPoolConfig** per creare una configurazione del pool di indirizzi back-end e archivia il risultato nella variabile denominata $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-131">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="a3c4a-132">Il dodicesimo comando usa il **nuovo-AzureRmLoadBalancerProbeConfig** per creare un probe e archivia le informazioni sulla sonda nella variabile denominata $Probe.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-132">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="a3c4a-133">Il comando tredicesimo usa il cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** per creare una configurazione del pool NAT (Network Address Translation) in ingresso per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-133">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="a3c4a-134">Il comando quattordicesima usa il **nuovo-AzureRmLoadBalancerRuleConfig** per creare una configurazione della regola di bilanciamento del carico e archivia il risultato nella variabile denominata $LBRule.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-134">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="a3c4a-135">Il comando quindicesimo usa il cmdlet **New-AzureRmLoadBalancer** per creare un bilanciamento del carico e archivia il risultato nella variabile denominata $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-135">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="a3c4a-136">Il comando sedicesimo USA **Get-AzureRmLoadBalancer** per ottenere informazioni sul bilanciamento del carico creato nel quindicesimo comando e archivia le informazioni nella variabile denominata $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-136">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="a3c4a-137">Il comando diciassettesimo usa il cmdlet **New-AzureRmVmssIPConfig** per creare una configurazione IP di vmss e archivia le informazioni nella variabile denominata $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-137">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="a3c4a-138">Il comando diciottesimo usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-138">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="a3c4a-139">Il comando diciannovesimo usa il cmdlet **New-AzureRmVmss** per creare vmss.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-139">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="a3c4a-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3c4a-140">PARAMETERS</span></span>

### <span data-ttu-id="a3c4a-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="a3c4a-141">-AllocationMethod</span></span>
<span data-ttu-id="a3c4a-142">Metodo di assegnazione per l'indirizzo IP pubblico del set di proporzioni (statico o dinamico).</span><span class="sxs-lookup"><span data-stu-id="a3c4a-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="a3c4a-143">Se non viene specificato alcun valore, l'allocazione sarà statica.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="a3c4a-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c4a-144">-AsJob</span></span>
<span data-ttu-id="a3c4a-145">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a3c4a-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-146">-BackendPoolName</span></span>
<span data-ttu-id="a3c4a-147">Nome del pool di indirizzi di backend da usare in bilanciamento del carico per questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="a3c4a-148">Se non viene specificato alcun valore, verrà creato un nuovo pool di backend con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="a3c4a-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a3c4a-149">-BackendPort</span></span>
<span data-ttu-id="a3c4a-150">Numeri di porta backend usati dal bilanciamento del carico impostato su scala per comunicare con le VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="a3c4a-151">Se non sono specificati valori, le porte 3389 e 5985 verranno usate per le VM di Windows e la porta 22 verrà usata per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="a3c4a-152">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="a3c4a-152">-Credential</span></span>
<span data-ttu-id="a3c4a-153">Credenziali di amministratore (nome utente e password) per VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="a3c4a-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a3c4a-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="a3c4a-155">Specifica le dimensioni dei dischi di dati in GB.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="a3c4a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c4a-156">-DefaultProfile</span></span>
<span data-ttu-id="a3c4a-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3c4a-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a3c4a-158">-DomainNameLabel</span></span>
<span data-ttu-id="a3c4a-159">L'etichetta del nome di dominio per il nome di dominio pubblico Fully-Qualified (FQDN) per questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="a3c4a-160">Questo è il primo componente del nome di dominio assegnato automaticamente al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="a3c4a-161">I nomi di dominio assegnati automaticamente usano il modulo ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a3c4a-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="a3c4a-162">Se non viene specificato alcun valore, l'etichetta del nome di dominio predefinito sarà la concatenazione di <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="a3c4a-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="a3c4a-163">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-163">-FrontendPoolName</span></span>
<span data-ttu-id="a3c4a-164">Nome del pool di indirizzi frontend da usare nel set di bilanciamento del carico di scala.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-164">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="a3c4a-165">Se non viene specificato alcun valore, verrà creato un nuovo pool di indirizzi frontend con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-165">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="a3c4a-166">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-166">-ImageName</span></span>
<span data-ttu-id="a3c4a-167">Nome dell'immagine per VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-167">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="a3c4a-168">Se non viene specificato alcun valore, verrà usata l'immagine "Windows Server 2016 datacenter".</span><span class="sxs-lookup"><span data-stu-id="a3c4a-168">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="a3c4a-169">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a3c4a-169">-InstanceCount</span></span>
<span data-ttu-id="a3c4a-170">Numero di immagini VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-170">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="a3c4a-171">Se non viene specificato alcun valore, verranno create 2 istanze.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-171">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="a3c4a-172">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-172">-LoadBalancerName</span></span>
<span data-ttu-id="a3c4a-173">Il nome del bilanciamento del carico da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-173">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="a3c4a-174">Se non viene specificato alcun valore, viene creato un nuovo gruppo di bilanciamento del carico che usa lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-174">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="a3c4a-175">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a3c4a-175">-Location</span></span>
<span data-ttu-id="a3c4a-176">Posizione di Azure in cui verrà creato questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-176">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="a3c4a-177">Se non viene specificato alcun valore, la posizione verrà dedotta dalla posizione di altre risorse a cui si fa riferimento nei parametri.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-177">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="a3c4a-178">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="a3c4a-178">-NatBackendPort</span></span>
<span data-ttu-id="a3c4a-179">Porta backend per la traduzione degli indirizzi di rete in ingresso.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-179">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="a3c4a-180">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-180">-PublicIpAddressName</span></span>
<span data-ttu-id="a3c4a-181">Nome dell'indirizzo IP pubblico da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-181">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="a3c4a-182">Se non viene specificato alcun valore, verrà creato un nuovo IPAddress pubblico con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-182">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="a3c4a-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-183">-ResourceGroupName</span></span>
<span data-ttu-id="a3c4a-184">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-184">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="a3c4a-185">Se non viene specificato alcun valore, verrà creato un nuovo ResourceGroup con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-185">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c4a-186">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-186">-SecurityGroupName</span></span>
<span data-ttu-id="a3c4a-187">Il nome del gruppo di sicurezza di rete da applicare al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-187">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="a3c4a-188">Se non viene specificato alcun valore, un gruppo di sicurezza di rete predefinito con lo stesso nome del set di proporzioni verrà creato e applicato al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-188">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="a3c4a-189">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a3c4a-189">-SinglePlacementGroup</span></span>
<span data-ttu-id="a3c4a-190">Usare questa opzione per creare il set di proporzioni in un singolo gruppo di posizionamento, il valore predefinito è più gruppi</span><span class="sxs-lookup"><span data-stu-id="a3c4a-190">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="a3c4a-191">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a3c4a-191">-SubnetAddressPrefix</span></span>
<span data-ttu-id="a3c4a-192">Il prefisso dell'indirizzo della subnet che verrà usato da questo Scalet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-192">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="a3c4a-193">Le impostazioni di subnet predefinite (192.168.1.0/24) verranno applicate se non viene specificato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-193">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="a3c4a-194">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-194">-SubnetName</span></span>
<span data-ttu-id="a3c4a-195">Nome della subnet da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-195">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="a3c4a-196">Verrà creata una nuova subnet con lo stesso nome del set di proporzioni se non viene specificato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-196">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="a3c4a-197">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a3c4a-197">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a3c4a-198">Se il parametro è presente, le VM (s) nel set di proporzioni è (sono) assegnato un'identità di sistema gestita che viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-198">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="a3c4a-199">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a3c4a-199">-UpgradePolicyMode</span></span>
<span data-ttu-id="a3c4a-200">Modalità di aggiornamento dei criteri per le istanze VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-200">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="a3c4a-201">I criteri di aggiornamento possono specificare aggiornamenti automatici, manuali o a rotazione.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-201">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="a3c4a-202">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a3c4a-202">-UserAssignedIdentity</span></span>
<span data-ttu-id="a3c4a-203">Nome dell'identità di un servizio gestito che deve essere assegnata alle VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-203">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="a3c4a-204">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3c4a-204">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a3c4a-205">Specifica l'oggetto **VirtualMachineScaleSet** che contiene le proprietà della vmss creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-205">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c4a-206">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-206">-VirtualNetworkName</span></span>
<span data-ttu-id="a3c4a-207">Nome della rete virtuale da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-207">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="a3c4a-208">Se non viene specificato alcun valore, verrà creata una nuova rete virtuale con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-208">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="a3c4a-209">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a3c4a-209">-VMScaleSetName</span></span>
<span data-ttu-id="a3c4a-210">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-210">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c4a-211">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a3c4a-211">-VmSize</span></span>
<span data-ttu-id="a3c4a-212">Dimensioni delle istanze VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-212">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="a3c4a-213">Se non è specificata alcuna dimensione, verrà usata una dimensione predefinita (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="a3c4a-213">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="a3c4a-214">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a3c4a-214">-VnetAddressPrefix</span></span>
<span data-ttu-id="a3c4a-215">Prefisso dell'indirizzo per la rete virtuale usata con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-215">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="a3c4a-216">Se non viene specificato alcun valore, verranno usate le impostazioni predefinite del prefisso dell'indirizzo di rete virtuale (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="a3c4a-216">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="a3c4a-217">-Zona</span><span class="sxs-lookup"><span data-stu-id="a3c4a-217">-Zone</span></span>
<span data-ttu-id="a3c4a-218">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-218">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="a3c4a-219">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3c4a-219">-Confirm</span></span>
<span data-ttu-id="a3c4a-220">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c4a-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c4a-221">-WhatIf</span></span>
<span data-ttu-id="a3c4a-222">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c4a-223">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c4a-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c4a-224">CommonParameters</span></span>
<span data-ttu-id="a3c4a-225">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c4a-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c4a-226">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3c4a-226">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c4a-227">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3c4a-227">INPUTS</span></span>

### <span data-ttu-id="a3c4a-228">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c4a-228">System.String</span></span>

### <span data-ttu-id="a3c4a-229">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3c4a-229">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="a3c4a-230">Parametri: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3c4a-230">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

### <span data-ttu-id="a3c4a-231">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a3c4a-231">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a3c4a-232">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3c4a-232">OUTPUTS</span></span>

### <span data-ttu-id="a3c4a-233">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3c4a-233">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a3c4a-234">Note</span><span class="sxs-lookup"><span data-stu-id="a3c4a-234">NOTES</span></span>

## <span data-ttu-id="a3c4a-235">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3c4a-235">RELATED LINKS</span></span>

[<span data-ttu-id="a3c4a-236">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-236">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-237">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-237">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-238">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-238">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-239">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-239">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-240">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-240">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-241">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-241">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a3c4a-242">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a3c4a-242">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


