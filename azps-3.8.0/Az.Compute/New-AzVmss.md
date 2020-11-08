---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 914d942620eea7517b2bac635399fd7d1b3c1307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021633"
---
# <span data-ttu-id="253fc-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-101">New-AzVmss</span></span>

## <span data-ttu-id="253fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="253fc-102">SYNOPSIS</span></span>
<span data-ttu-id="253fc-103">Crea un VMSS.</span><span class="sxs-lookup"><span data-stu-id="253fc-103">Creates a VMSS.</span></span>

## <span data-ttu-id="253fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="253fc-104">SYNTAX</span></span>

### <span data-ttu-id="253fc-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="253fc-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="253fc-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="253fc-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="253fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="253fc-107">DESCRIPTION</span></span>
<span data-ttu-id="253fc-108">Il cmdlet **New-AzVmss** crea un set di scale della macchina virtuale (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="253fc-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="253fc-109">Usa il set di parametri Simple ( `SimpleParameterSet` ) per creare rapidamente una vmss preimpostata e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="253fc-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="253fc-110">Usa il set di parametri predefinito ( `DefaultParameter` ) per scenari più avanzati quando devi configurare con precisione ogni componente di vmss e ogni risorsa associata prima della creazione.</span><span class="sxs-lookup"><span data-stu-id="253fc-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="253fc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="253fc-111">EXAMPLES</span></span>

### <span data-ttu-id="253fc-112">Esempio 1: creare un VMSS usando il **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="253fc-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="253fc-113">Il comando precedente crea il seguente nome `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="253fc-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="253fc-114">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="253fc-114">A Resource Group</span></span>
* <span data-ttu-id="253fc-115">Una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="253fc-115">A virtual network</span></span>
* <span data-ttu-id="253fc-116">Un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="253fc-116">A load balancer</span></span>
* <span data-ttu-id="253fc-117">Un IP pubblico</span><span class="sxs-lookup"><span data-stu-id="253fc-117">A public IP</span></span>
* <span data-ttu-id="253fc-118">VMSS con 2 istanze</span><span class="sxs-lookup"><span data-stu-id="253fc-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="253fc-119">L'immagine predefinita scelta per le VM in VMSS è `2016-Datacenter Windows Server` e l'USK è `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="253fc-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="253fc-120">Esempio 2: creare un VMSS usando il **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="253fc-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="253fc-121">L'esempio complesso precedente crea un VMSS, in seguito è una spiegazione di quanto sta accadendo:</span><span class="sxs-lookup"><span data-stu-id="253fc-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="253fc-122">Il primo comando crea un gruppo di risorse con il nome e il percorso specificati.</span><span class="sxs-lookup"><span data-stu-id="253fc-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="253fc-123">Il secondo comando usa il cmdlet **New-AzStorageAccount** per creare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="253fc-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="253fc-124">Il terzo comando usa quindi il cmdlet **Get-AzStorageAccount** per ottenere l'account di archiviazione creato nel secondo comando e archivia il risultato nella variabile $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="253fc-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="253fc-125">Il quinto comando usa il cmdlet **New-AzVirtualNetworkSubnetConfig** per creare una subnet e archivia il risultato nella variabile denominata $subnet.</span><span class="sxs-lookup"><span data-stu-id="253fc-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="253fc-126">Il sesto comando usa il cmdlet **New-AzVirtualNetwork** per creare una rete virtuale e archivia il risultato nella variabile denominata $VNet.</span><span class="sxs-lookup"><span data-stu-id="253fc-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="253fc-127">Il settimo comando USA **Get-AzVirtualNetwork** per ottenere informazioni sulla rete virtuale creata nel sesto comando e archivia le informazioni nella variabile denominata $VNet.</span><span class="sxs-lookup"><span data-stu-id="253fc-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="253fc-128">Il comando ottavo e nono usa la **nuova-AzPublicIpAddress** e **Get-AzureRmPublicIpAddress** per creare e ottenere informazioni da tale indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="253fc-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="253fc-129">I comandi archiviano le informazioni nella variabile denominata $PubIP.</span><span class="sxs-lookup"><span data-stu-id="253fc-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="253fc-130">Il decimo comando usa il cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** per creare un bilanciamento del carico frontend e archivia il risultato nella variabile denominata $frontend.</span><span class="sxs-lookup"><span data-stu-id="253fc-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="253fc-131">L'undicesimo comando usa il **nuovo-AzLoadBalancerBackendAddressPoolConfig** per creare una configurazione del pool di indirizzi back-end e archivia il risultato nella variabile denominata $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="253fc-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="253fc-132">Il dodicesimo comando usa il **nuovo-AzLoadBalancerProbeConfig** per creare un probe e archivia le informazioni sulla sonda nella variabile denominata $Probe.</span><span class="sxs-lookup"><span data-stu-id="253fc-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="253fc-133">Il comando tredicesimo usa il cmdlet **New-AzLoadBalancerInboundNatPoolConfig** per creare una configurazione del pool NAT (Network Address Translation) in ingresso per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="253fc-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="253fc-134">Il comando quattordicesima usa il **nuovo-AzLoadBalancerRuleConfig** per creare una configurazione della regola di bilanciamento del carico e archivia il risultato nella variabile denominata $LBRule.</span><span class="sxs-lookup"><span data-stu-id="253fc-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="253fc-135">Il comando quindicesimo usa il cmdlet **New-AzLoadBalancer** per creare un bilanciamento del carico e archivia il risultato nella variabile denominata $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="253fc-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="253fc-136">Il comando sedicesimo USA **Get-AzLoadBalancer** per ottenere informazioni sul bilanciamento del carico creato nel quindicesimo comando e archivia le informazioni nella variabile denominata $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="253fc-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="253fc-137">Il comando diciassettesimo usa il cmdlet **New-AzVmssIPConfig** per creare una configurazione IP di vmss e archivia le informazioni nella variabile denominata $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="253fc-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="253fc-138">Il comando diciottesimo usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="253fc-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="253fc-139">Il comando diciannovesimo usa il cmdlet **New-AzVmss** per creare vmss.</span><span class="sxs-lookup"><span data-stu-id="253fc-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="253fc-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="253fc-140">PARAMETERS</span></span>

### <span data-ttu-id="253fc-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="253fc-141">-AllocationMethod</span></span>
<span data-ttu-id="253fc-142">Metodo di assegnazione per l'indirizzo IP pubblico del set di proporzioni (statico o dinamico).</span><span class="sxs-lookup"><span data-stu-id="253fc-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="253fc-143">Se non viene specificato alcun valore, l'allocazione sarà statica.</span><span class="sxs-lookup"><span data-stu-id="253fc-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="253fc-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="253fc-144">-AsJob</span></span>
<span data-ttu-id="253fc-145">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="253fc-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="253fc-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="253fc-146">-BackendPoolName</span></span>
<span data-ttu-id="253fc-147">Nome del pool di indirizzi di backend da usare in bilanciamento del carico per questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="253fc-148">Se non viene specificato alcun valore, verrà creato un nuovo pool di backend con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="253fc-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="253fc-149">-BackendPort</span></span>
<span data-ttu-id="253fc-150">Numeri di porta backend usati dal bilanciamento del carico impostato su scala per comunicare con le VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="253fc-151">Se non sono specificati valori, le porte 3389 e 5985 verranno usate per le VM di Windows e la porta 22 verrà usata per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="253fc-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="253fc-152">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="253fc-152">-Credential</span></span>
<span data-ttu-id="253fc-153">Credenziali di amministratore (nome utente e password) per VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="253fc-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="253fc-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="253fc-155">Specifica le dimensioni dei dischi di dati in GB.</span><span class="sxs-lookup"><span data-stu-id="253fc-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="253fc-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253fc-156">-DefaultProfile</span></span>
<span data-ttu-id="253fc-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="253fc-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="253fc-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="253fc-158">-DomainNameLabel</span></span>
<span data-ttu-id="253fc-159">L'etichetta del nome di dominio per il nome di dominio pubblico Fully-Qualified (FQDN) per questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="253fc-160">Questo è il primo componente del nome di dominio assegnato automaticamente al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="253fc-161">I nomi di dominio assegnati automaticamente usano il modulo ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="253fc-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="253fc-162">Se non viene specificato alcun valore, l'etichetta del nome di dominio predefinito sarà la concatenazione di <ScaleSetName> e <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="253fc-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="253fc-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="253fc-163">-EnableUltraSSD</span></span>
<span data-ttu-id="253fc-164">Usare i dischi UltraSSD per le VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="253fc-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="253fc-165">-EvictionPolicy</span></span>
<span data-ttu-id="253fc-166">Criteri di eliminazione per il set di scale della macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="253fc-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="253fc-167">Solo i valori supportati sono "deallocate" e "Delete".</span><span class="sxs-lookup"><span data-stu-id="253fc-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="253fc-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="253fc-168">-FrontendPoolName</span></span>
<span data-ttu-id="253fc-169">Nome del pool di indirizzi frontend da usare nel set di bilanciamento del carico di scala.</span><span class="sxs-lookup"><span data-stu-id="253fc-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="253fc-170">Se non viene specificato alcun valore, verrà creato un nuovo pool di indirizzi frontend con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="253fc-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="253fc-171">-ImageName</span></span>
<span data-ttu-id="253fc-172">Nome dell'immagine per VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="253fc-173">Se non viene specificato alcun valore, verrà usata l'immagine "Windows Server 2016 datacenter".</span><span class="sxs-lookup"><span data-stu-id="253fc-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="253fc-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="253fc-174">-InstanceCount</span></span>
<span data-ttu-id="253fc-175">Numero di immagini VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="253fc-176">Se non viene specificato alcun valore, verranno create 2 istanze.</span><span class="sxs-lookup"><span data-stu-id="253fc-176">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="253fc-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="253fc-177">-LoadBalancerName</span></span>
<span data-ttu-id="253fc-178">Il nome del bilanciamento del carico da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="253fc-179">Se non viene specificato alcun valore, viene creato un nuovo gruppo di bilanciamento del carico che usa lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="253fc-180">-Posizione</span><span class="sxs-lookup"><span data-stu-id="253fc-180">-Location</span></span>
<span data-ttu-id="253fc-181">Posizione di Azure in cui verrà creato questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="253fc-182">Se non viene specificato alcun valore, la posizione verrà dedotta dalla posizione di altre risorse a cui si fa riferimento nei parametri.</span><span class="sxs-lookup"><span data-stu-id="253fc-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="253fc-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="253fc-183">-MaxPrice</span></span>
<span data-ttu-id="253fc-184">Prezzo massimo della fatturazione di un set di scale della macchina virtuale con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="253fc-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="253fc-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="253fc-185">-NatBackendPort</span></span>
<span data-ttu-id="253fc-186">Porta backend per la traduzione degli indirizzi di rete in ingresso.</span><span class="sxs-lookup"><span data-stu-id="253fc-186">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="253fc-187">-Priorità</span><span class="sxs-lookup"><span data-stu-id="253fc-187">-Priority</span></span>
<span data-ttu-id="253fc-188">Priorità per la macchina virtuale nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-188">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="253fc-189">Solo i valori supportati sono "regolari", "spot" e "low".</span><span class="sxs-lookup"><span data-stu-id="253fc-189">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="253fc-190">"Normale" è per la normale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="253fc-190">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="253fc-191">"Spot" è per la macchina virtuale spot.</span><span class="sxs-lookup"><span data-stu-id="253fc-191">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="253fc-192">"Basso" è anche per la macchina virtuale spot, ma è sostituito da "spot".</span><span class="sxs-lookup"><span data-stu-id="253fc-192">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="253fc-193">Usare "spot" invece di "low".</span><span class="sxs-lookup"><span data-stu-id="253fc-193">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="253fc-194">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="253fc-194">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="253fc-195">ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-195">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="253fc-196">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="253fc-196">-PublicIpAddressName</span></span>
<span data-ttu-id="253fc-197">Nome dell'indirizzo IP pubblico da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-197">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="253fc-198">Se non viene specificato alcun valore, verrà creato un nuovo IPAddress pubblico con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-198">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="253fc-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="253fc-199">-ResourceGroupName</span></span>
<span data-ttu-id="253fc-200">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="253fc-200">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="253fc-201">Se non viene specificato alcun valore, verrà creato un nuovo ResourceGroup con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-201">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="253fc-202">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="253fc-202">-ScaleInPolicy</span></span>
<span data-ttu-id="253fc-203">Regole da seguire durante la scalabilità in una scala macchina virtuale impostata.</span><span class="sxs-lookup"><span data-stu-id="253fc-203">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="253fc-204">I valori possibili sono: "default", "OldestVM" e "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="253fc-204">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="253fc-205">"Impostazione predefinita" quando un set di scale di una macchina virtuale viene ridimensionato, il set di proporzioni sarà prima di tutto bilanciato tra le zone se si tratta di un set di scala zonale.</span><span class="sxs-lookup"><span data-stu-id="253fc-205">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="253fc-206">Verrà quindi bilanciato tra i domini di errore il più lontano possibile.</span><span class="sxs-lookup"><span data-stu-id="253fc-206">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="253fc-207">All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno quelle più recenti che non sono protette da scale-in.</span><span class="sxs-lookup"><span data-stu-id="253fc-207">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="253fc-208">' OldestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali meno recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="253fc-208">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="253fc-209">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="253fc-209">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="253fc-210">All'interno di ogni zona le macchine virtuali meno recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="253fc-210">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="253fc-211">' NewestVM ' quando un set di scale della macchina virtuale viene ridimensionato, le macchine virtuali più recenti che non sono protette da scale-in verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="253fc-211">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="253fc-212">Per i set di scale della macchina virtuale zonale, il set di proporzioni verrà prima bilanciato tra le aree.</span><span class="sxs-lookup"><span data-stu-id="253fc-212">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="253fc-213">All'interno di ogni zona le macchine virtuali più recenti che non sono protette verranno scelte per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="253fc-213">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="253fc-214">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="253fc-214">-SecurityGroupName</span></span>
<span data-ttu-id="253fc-215">Il nome del gruppo di sicurezza di rete da applicare al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-215">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="253fc-216">Se non viene specificato alcun valore, un gruppo di sicurezza di rete predefinito con lo stesso nome del set di proporzioni verrà creato e applicato al set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-216">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="253fc-217">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="253fc-217">-SinglePlacementGroup</span></span>
<span data-ttu-id="253fc-218">Usare questa opzione per creare il set di proporzioni in un singolo gruppo di posizionamento, il valore predefinito è più gruppi</span><span class="sxs-lookup"><span data-stu-id="253fc-218">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="253fc-219">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="253fc-219">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="253fc-220">Specifica che le estensioni non vengono eseguite sulle VM extra provisioning.</span><span class="sxs-lookup"><span data-stu-id="253fc-220">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="253fc-221">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="253fc-221">-SubnetAddressPrefix</span></span>
<span data-ttu-id="253fc-222">Il prefisso dell'indirizzo della subnet che verrà usato da questo Scalet.</span><span class="sxs-lookup"><span data-stu-id="253fc-222">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="253fc-223">Le impostazioni di subnet predefinite (192.168.1.0/24) verranno applicate se non viene specificato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="253fc-223">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="253fc-224">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="253fc-224">-SubnetName</span></span>
<span data-ttu-id="253fc-225">Nome della subnet da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-225">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="253fc-226">Verrà creata una nuova subnet con lo stesso nome del set di proporzioni se non viene specificato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="253fc-226">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="253fc-227">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="253fc-227">-SystemAssignedIdentity</span></span>
<span data-ttu-id="253fc-228">Se il parametro è presente, le VM (s) nel set di proporzioni è (sono) assegnato un'identità di sistema gestita che viene generata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="253fc-228">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="253fc-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="253fc-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="253fc-230">Modalità di aggiornamento dei criteri per le istanze VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-230">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="253fc-231">I criteri di aggiornamento possono specificare aggiornamenti automatici, manuali o a rotazione.</span><span class="sxs-lookup"><span data-stu-id="253fc-231">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="253fc-232">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="253fc-232">-UserAssignedIdentity</span></span>
<span data-ttu-id="253fc-233">Nome dell'identità di un servizio gestito che deve essere assegnata alle VM nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-233">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="253fc-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="253fc-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="253fc-235">Specifica l'oggetto **VirtualMachineScaleSet** che contiene le proprietà della vmss creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="253fc-235">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="253fc-236">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="253fc-236">-VirtualNetworkName</span></span>
<span data-ttu-id="253fc-237">Nome della rete virtuale da usare con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-237">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="253fc-238">Se non viene specificato alcun valore, verrà creata una nuova rete virtuale con lo stesso nome del set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-238">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="253fc-239">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="253fc-239">-VMScaleSetName</span></span>
<span data-ttu-id="253fc-240">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="253fc-240">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="253fc-241">-VmSize</span><span class="sxs-lookup"><span data-stu-id="253fc-241">-VmSize</span></span>
<span data-ttu-id="253fc-242">Dimensioni delle istanze VM in questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-242">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="253fc-243">Se non è specificata alcuna dimensione, verrà usata una dimensione predefinita (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="253fc-243">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="253fc-244">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="253fc-244">-VnetAddressPrefix</span></span>
<span data-ttu-id="253fc-245">Prefisso dell'indirizzo per la rete virtuale usata con questo set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="253fc-245">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="253fc-246">Se non viene specificato alcun valore, verranno usate le impostazioni predefinite del prefisso dell'indirizzo di rete virtuale (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="253fc-246">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="253fc-247">-Zona</span><span class="sxs-lookup"><span data-stu-id="253fc-247">-Zone</span></span>
<span data-ttu-id="253fc-248">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="253fc-248">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="253fc-249">-Confermare</span><span class="sxs-lookup"><span data-stu-id="253fc-249">-Confirm</span></span>
<span data-ttu-id="253fc-250">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="253fc-250">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="253fc-251">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="253fc-251">-WhatIf</span></span>
<span data-ttu-id="253fc-252">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="253fc-252">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="253fc-253">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="253fc-253">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="253fc-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253fc-254">CommonParameters</span></span>
<span data-ttu-id="253fc-255">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253fc-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253fc-256">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="253fc-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253fc-257">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="253fc-257">INPUTS</span></span>

### <span data-ttu-id="253fc-258">System. String</span><span class="sxs-lookup"><span data-stu-id="253fc-258">System.String</span></span>

### <span data-ttu-id="253fc-259">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="253fc-259">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="253fc-260">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="253fc-260">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="253fc-261">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="253fc-261">OUTPUTS</span></span>

### <span data-ttu-id="253fc-262">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="253fc-262">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="253fc-263">Note</span><span class="sxs-lookup"><span data-stu-id="253fc-263">NOTES</span></span>

## <span data-ttu-id="253fc-264">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="253fc-264">RELATED LINKS</span></span>

[<span data-ttu-id="253fc-265">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-265">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="253fc-266">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-266">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="253fc-267">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-267">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="253fc-268">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-268">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="253fc-269">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-269">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="253fc-270">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-270">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="253fc-271">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="253fc-271">Update-AzVmss</span></span>](./Update-AzVmss.md)


