---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018987"
---
# <span data-ttu-id="23ad1-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="23ad1-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="23ad1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="23ad1-103">Crea endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="23ad1-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="23ad1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23ad1-104">SYNTAX</span></span>

### <span data-ttu-id="23ad1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="23ad1-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23ad1-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="23ad1-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ad1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23ad1-107">DESCRIPTION</span></span>
<span data-ttu-id="23ad1-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet crea endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="23ad1-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="23ad1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23ad1-109">EXAMPLES</span></span>

### <span data-ttu-id="23ad1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23ad1-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="23ad1-111">Nome: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Indirizzo: Filter: {"Type": "include", "Items": [{"Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="23ad1-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="23ad1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23ad1-112">PARAMETERS</span></span>

### <span data-ttu-id="23ad1-113">-Address</span><span class="sxs-lookup"><span data-stu-id="23ad1-113">-Address</span></span>
<span data-ttu-id="23ad1-114">Indirizzo dell'endpoint di monitoraggio della connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="23ad1-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ad1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ad1-115">-DefaultProfile</span></span>
<span data-ttu-id="23ad1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23ad1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ad1-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="23ad1-117">-FilterItem</span></span>
<span data-ttu-id="23ad1-118">Elenco di elementi nel filtro.</span><span class="sxs-lookup"><span data-stu-id="23ad1-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ad1-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="23ad1-119">-FilterType</span></span>
<span data-ttu-id="23ad1-120">Comportamento del filtro endpoint.</span><span class="sxs-lookup"><span data-stu-id="23ad1-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="23ad1-121">Attualmente è supportata solo la funzione "Includi".</span><span class="sxs-lookup"><span data-stu-id="23ad1-121">Currently only 'Include' is supported.</span></span>

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

### <span data-ttu-id="23ad1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="23ad1-122">-Name</span></span>
<span data-ttu-id="23ad1-123">Nome dell'endpoint di monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="23ad1-123">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="23ad1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23ad1-124">-ResourceId</span></span>
<span data-ttu-id="23ad1-125">ID risorsa dell'endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="23ad1-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ad1-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23ad1-126">-Confirm</span></span>
<span data-ttu-id="23ad1-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ad1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ad1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ad1-128">-WhatIf</span></span>
<span data-ttu-id="23ad1-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23ad1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23ad1-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23ad1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ad1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ad1-131">CommonParameters</span></span>
<span data-ttu-id="23ad1-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ad1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ad1-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ad1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ad1-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23ad1-134">INPUTS</span></span>

### <span data-ttu-id="23ad1-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="23ad1-135">None</span></span>

## <span data-ttu-id="23ad1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23ad1-136">OUTPUTS</span></span>

### <span data-ttu-id="23ad1-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="23ad1-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="23ad1-138">Note</span><span class="sxs-lookup"><span data-stu-id="23ad1-138">NOTES</span></span>

## <span data-ttu-id="23ad1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23ad1-139">RELATED LINKS</span></span>
