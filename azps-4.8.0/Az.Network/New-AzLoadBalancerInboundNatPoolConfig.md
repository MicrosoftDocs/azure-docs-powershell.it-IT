---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188479"
---
# <span data-ttu-id="90c83-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90c83-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="90c83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90c83-102">SYNOPSIS</span></span>
<span data-ttu-id="90c83-103">Crea una configurazione del pool NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="90c83-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="90c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90c83-104">SYNTAX</span></span>

### <span data-ttu-id="90c83-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90c83-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c83-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90c83-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c83-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90c83-107">DESCRIPTION</span></span>
<span data-ttu-id="90c83-108">Il cmdlet **New-AzLoadBalancerInboundNatPoolConfig** crea una configurazione del pool NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="90c83-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="90c83-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90c83-109">EXAMPLES</span></span>

### <span data-ttu-id="90c83-110">Esempio 1: nuovo</span><span class="sxs-lookup"><span data-stu-id="90c83-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="90c83-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90c83-111">PARAMETERS</span></span>

### <span data-ttu-id="90c83-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="90c83-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c83-113">-DefaultProfile</span></span>
<span data-ttu-id="90c83-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90c83-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c83-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="90c83-115">-EnableFloatingIP</span></span>
<span data-ttu-id="90c83-116">Configura l'endpoint di una macchina virtuale per le funzionalità IP mobili necessarie per configurare un gruppo di disponibilità di SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="90c83-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="90c83-117">Questa impostazione è obbligatoria quando si usano i gruppi di disponibilità di SQL AlwaysOn in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90c83-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="90c83-118">Questa impostazione non può essere modificata dopo la creazione dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="90c83-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="90c83-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="90c83-119">-EnableTcpReset</span></span>
<span data-ttu-id="90c83-120">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="90c83-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="90c83-121">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="90c83-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="90c83-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c83-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90c83-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="90c83-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="90c83-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="90c83-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="90c83-127">Timeout per la connessione inattiva TCP.</span><span class="sxs-lookup"><span data-stu-id="90c83-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="90c83-128">Il valore può essere impostato tra 4 e 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="90c83-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="90c83-129">Il valore predefinito è 4 minuti.</span><span class="sxs-lookup"><span data-stu-id="90c83-129">The default value is 4 minutes.</span></span> <span data-ttu-id="90c83-130">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="90c83-130">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="90c83-131">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="90c83-132">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90c83-133">-Confirm</span></span>
<span data-ttu-id="90c83-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90c83-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c83-135">-WhatIf</span></span>
<span data-ttu-id="90c83-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90c83-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90c83-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90c83-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c83-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c83-138">CommonParameters</span></span>
<span data-ttu-id="90c83-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c83-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c83-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c83-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c83-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90c83-141">INPUTS</span></span>

### <span data-ttu-id="90c83-142">System. String</span><span class="sxs-lookup"><span data-stu-id="90c83-142">System.String</span></span>

### <span data-ttu-id="90c83-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="90c83-143">System.Int32</span></span>

### <span data-ttu-id="90c83-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c83-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="90c83-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90c83-145">OUTPUTS</span></span>

### <span data-ttu-id="90c83-146">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="90c83-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="90c83-147">Note</span><span class="sxs-lookup"><span data-stu-id="90c83-147">NOTES</span></span>

## <span data-ttu-id="90c83-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90c83-148">RELATED LINKS</span></span>

[<span data-ttu-id="90c83-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90c83-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90c83-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90c83-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90c83-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90c83-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90c83-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90c83-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)