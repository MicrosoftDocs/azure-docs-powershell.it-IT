---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032363"
---
# <span data-ttu-id="09d9c-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="09d9c-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="09d9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="09d9c-103">Crea un elemento filtro endpoint di monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="09d9c-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="09d9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09d9c-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09d9c-105">DESCRIPTION</span></span>
<span data-ttu-id="09d9c-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject crea l'elemento filtro endpoint.</span><span class="sxs-lookup"><span data-stu-id="09d9c-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="09d9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09d9c-107">EXAMPLES</span></span>

### <span data-ttu-id="09d9c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09d9c-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="09d9c-109">Digitare: AgentAddress Indirizzo: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="09d9c-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="09d9c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09d9c-110">PARAMETERS</span></span>

### <span data-ttu-id="09d9c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="09d9c-111">-Address</span></span>
<span data-ttu-id="09d9c-112">Indirizzo dell'elemento filter.</span><span class="sxs-lookup"><span data-stu-id="09d9c-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="09d9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d9c-113">-DefaultProfile</span></span>
<span data-ttu-id="09d9c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09d9c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09d9c-115">-Digitare</span><span class="sxs-lookup"><span data-stu-id="09d9c-115">-Type</span></span>
<span data-ttu-id="09d9c-116">Tipo di elemento incluso nel filtro.</span><span class="sxs-lookup"><span data-stu-id="09d9c-116">The type of item included in the filter.</span></span> <span data-ttu-id="09d9c-117">Attualmente è supportato solo "AgentAddress".</span><span class="sxs-lookup"><span data-stu-id="09d9c-117">Currently only 'AgentAddress' is supported.</span></span>

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

### <span data-ttu-id="09d9c-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09d9c-118">-Confirm</span></span>
<span data-ttu-id="09d9c-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d9c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09d9c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d9c-120">-WhatIf</span></span>
<span data-ttu-id="09d9c-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09d9c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09d9c-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09d9c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09d9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d9c-123">CommonParameters</span></span>
<span data-ttu-id="09d9c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d9c-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09d9c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d9c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09d9c-126">INPUTS</span></span>

### <span data-ttu-id="09d9c-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09d9c-127">None</span></span>

## <span data-ttu-id="09d9c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09d9c-128">OUTPUTS</span></span>

### <span data-ttu-id="09d9c-129">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="09d9c-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="09d9c-130">Note</span><span class="sxs-lookup"><span data-stu-id="09d9c-130">NOTES</span></span>

## <span data-ttu-id="09d9c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09d9c-131">RELATED LINKS</span></span>
