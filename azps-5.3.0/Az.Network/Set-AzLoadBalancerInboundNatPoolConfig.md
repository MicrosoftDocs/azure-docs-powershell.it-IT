---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488893"
---
# <span data-ttu-id="8e44a-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e44a-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8e44a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e44a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e44a-103">Imposta una configurazione del pool NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8e44a-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8e44a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e44a-104">SYNTAX</span></span>

### <span data-ttu-id="8e44a-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e44a-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e44a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e44a-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e44a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e44a-107">DESCRIPTION</span></span>
<span data-ttu-id="8e44a-108">Il cmdlet **set-AzLoadBalancerInboundNatPoolConfig** imposta una configurazione del pool NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8e44a-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="8e44a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e44a-109">EXAMPLES</span></span>

### <span data-ttu-id="8e44a-110">Esempio 1: impostare</span><span class="sxs-lookup"><span data-stu-id="8e44a-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="8e44a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e44a-111">PARAMETERS</span></span>

### <span data-ttu-id="8e44a-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8e44a-112">-BackendPort</span></span>
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

### <span data-ttu-id="8e44a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e44a-113">-DefaultProfile</span></span>
<span data-ttu-id="8e44a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e44a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e44a-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8e44a-115">-EnableFloatingIP</span></span>
<span data-ttu-id="8e44a-116">Configura l'endpoint di una macchina virtuale per le funzionalità IP mobili necessarie per configurare un gruppo di disponibilità di SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="8e44a-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="8e44a-117">Questa impostazione è obbligatoria quando si usano i gruppi di disponibilità di SQL AlwaysOn in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e44a-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="8e44a-118">Questa impostazione non può essere modificata dopo la creazione dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="8e44a-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="8e44a-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8e44a-119">-EnableTcpReset</span></span>
<span data-ttu-id="8e44a-120">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="8e44a-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="8e44a-121">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="8e44a-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8e44a-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e44a-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="8e44a-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8e44a-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="8e44a-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="8e44a-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="8e44a-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="8e44a-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="8e44a-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8e44a-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8e44a-127">Timeout per la connessione inattiva TCP.</span><span class="sxs-lookup"><span data-stu-id="8e44a-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="8e44a-128">Il valore può essere impostato tra 4 e 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="8e44a-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="8e44a-129">Il valore predefinito è 4 minuti.</span><span class="sxs-lookup"><span data-stu-id="8e44a-129">The default value is 4 minutes.</span></span> <span data-ttu-id="8e44a-130">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="8e44a-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8e44a-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e44a-131">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e44a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e44a-132">-Name</span></span>
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

### <span data-ttu-id="8e44a-133">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="8e44a-133">-Protocol</span></span>
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

### <span data-ttu-id="8e44a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e44a-134">-Confirm</span></span>
<span data-ttu-id="8e44a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e44a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e44a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e44a-136">-WhatIf</span></span>
<span data-ttu-id="8e44a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e44a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e44a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e44a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e44a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e44a-139">CommonParameters</span></span>
<span data-ttu-id="8e44a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e44a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e44a-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e44a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e44a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e44a-142">INPUTS</span></span>

### <span data-ttu-id="8e44a-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e44a-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="8e44a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8e44a-144">System.String</span></span>

### <span data-ttu-id="8e44a-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8e44a-145">System.Int32</span></span>

### <span data-ttu-id="8e44a-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e44a-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="8e44a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e44a-147">OUTPUTS</span></span>

### <span data-ttu-id="8e44a-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8e44a-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8e44a-149">Note</span><span class="sxs-lookup"><span data-stu-id="8e44a-149">NOTES</span></span>

## <span data-ttu-id="8e44a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e44a-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e44a-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e44a-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8e44a-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e44a-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8e44a-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e44a-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8e44a-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e44a-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
