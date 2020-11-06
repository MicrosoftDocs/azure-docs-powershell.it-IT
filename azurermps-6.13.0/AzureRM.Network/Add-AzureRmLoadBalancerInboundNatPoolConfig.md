---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2245fa10d160fc0f6b085a039214f9bcd72404a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510919"
---
# <span data-ttu-id="beeaa-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="beeaa-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="beeaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="beeaa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beeaa-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beeaa-103">SYNTAX</span></span>

### <span data-ttu-id="beeaa-104">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="beeaa-104">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beeaa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="beeaa-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beeaa-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beeaa-106">DESCRIPTION</span></span>

## <span data-ttu-id="beeaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beeaa-107">EXAMPLES</span></span>

### <span data-ttu-id="beeaa-108">1: aggiungere</span><span class="sxs-lookup"><span data-stu-id="beeaa-108">1: Add</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="beeaa-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="beeaa-109">PARAMETERS</span></span>

### <span data-ttu-id="beeaa-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="beeaa-110">-BackendPort</span></span>
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

### <span data-ttu-id="beeaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beeaa-111">-DefaultProfile</span></span>
<span data-ttu-id="beeaa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beeaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beeaa-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="beeaa-113">-EnableFloatingIP</span></span>
<span data-ttu-id="beeaa-114">Configura l'endpoint di una macchina virtuale per le funzionalità IP mobili necessarie per configurare un gruppo di disponibilità di SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="beeaa-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="beeaa-115">Questa impostazione è obbligatoria quando si usano i gruppi di disponibilità di SQL AlwaysOn in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="beeaa-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="beeaa-116">Questa impostazione non può essere modificata dopo la creazione dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="beeaa-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="beeaa-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="beeaa-117">-EnableTcpReset</span></span>
<span data-ttu-id="beeaa-118">Ricevere la reimpostazione TCP bidirezionale sul timeout di inattività del flusso TCP o la terminazione imprevista della connessione.</span><span class="sxs-lookup"><span data-stu-id="beeaa-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="beeaa-119">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="beeaa-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="beeaa-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="beeaa-120">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="beeaa-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="beeaa-121">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="beeaa-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="beeaa-122">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="beeaa-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="beeaa-123">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="beeaa-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="beeaa-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="beeaa-125">Timeout per la connessione inattiva TCP.</span><span class="sxs-lookup"><span data-stu-id="beeaa-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="beeaa-126">Il valore può essere impostato tra 4 e 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="beeaa-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="beeaa-127">Il valore predefinito è 4 minuti.</span><span class="sxs-lookup"><span data-stu-id="beeaa-127">The default value is 4 minutes.</span></span> <span data-ttu-id="beeaa-128">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="beeaa-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="beeaa-129">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeaa-129">-LoadBalancer</span></span>
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

### <span data-ttu-id="beeaa-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="beeaa-130">-Name</span></span>
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

### <span data-ttu-id="beeaa-131">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="beeaa-131">-Protocol</span></span>
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

### <span data-ttu-id="beeaa-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="beeaa-132">-Confirm</span></span>
<span data-ttu-id="beeaa-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beeaa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beeaa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beeaa-134">-WhatIf</span></span>
<span data-ttu-id="beeaa-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beeaa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="beeaa-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beeaa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beeaa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beeaa-137">CommonParameters</span></span>
<span data-ttu-id="beeaa-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beeaa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beeaa-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beeaa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beeaa-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="beeaa-140">INPUTS</span></span>

### <span data-ttu-id="beeaa-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeaa-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="beeaa-142">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="beeaa-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="beeaa-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beeaa-143">OUTPUTS</span></span>

### <span data-ttu-id="beeaa-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="beeaa-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="beeaa-145">Note</span><span class="sxs-lookup"><span data-stu-id="beeaa-145">NOTES</span></span>

## <span data-ttu-id="beeaa-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beeaa-146">RELATED LINKS</span></span>
