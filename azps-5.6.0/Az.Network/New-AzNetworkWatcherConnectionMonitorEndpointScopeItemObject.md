---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958525"
---
# <span data-ttu-id="d4f54-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="d4f54-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="d4f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f54-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f54-103">Crea un elemento dell'ambito endpoint del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="d4f54-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="d4f54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4f54-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4f54-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4f54-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f54-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject crea l'elemento dell'ambito dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d4f54-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="d4f54-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4f54-107">EXAMPLES</span></span>

### <span data-ttu-id="d4f54-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4f54-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="d4f54-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4f54-109">PARAMETERS</span></span>

### <span data-ttu-id="d4f54-110">-Address</span><span class="sxs-lookup"><span data-stu-id="d4f54-110">-Address</span></span>
<span data-ttu-id="d4f54-111">Indirizzo dell'elemento di ambito.</span><span class="sxs-lookup"><span data-stu-id="d4f54-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="d4f54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f54-112">-DefaultProfile</span></span>
<span data-ttu-id="d4f54-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f54-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f54-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4f54-114">-Confirm</span></span>
<span data-ttu-id="d4f54-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4f54-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f54-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f54-116">-WhatIf</span></span>
<span data-ttu-id="d4f54-117">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4f54-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f54-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4f54-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f54-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f54-119">CommonParameters</span></span>
<span data-ttu-id="d4f54-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f54-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f54-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4f54-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f54-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4f54-122">INPUTS</span></span>

### <span data-ttu-id="d4f54-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d4f54-123">None</span></span>

## <span data-ttu-id="d4f54-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4f54-124">OUTPUTS</span></span>

### <span data-ttu-id="d4f54-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="d4f54-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="d4f54-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4f54-126">NOTES</span></span>

## <span data-ttu-id="d4f54-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4f54-127">RELATED LINKS</span></span>
