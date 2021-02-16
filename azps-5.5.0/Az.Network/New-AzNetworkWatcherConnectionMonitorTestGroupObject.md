---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206675"
---
# <span data-ttu-id="e6e3c-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e6e3c-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e6e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e3c-103">Creare un gruppo di test del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="e6e3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e3c-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e3c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e3c-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorTestGroupObject crea un gruppo di test del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="e6e3c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e3c-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e3c-108">Esempio 1: Creare un gruppo di test con 2 testConfigurations, w endpoint di origine e 2 di destinazione</span><span class="sxs-lookup"><span data-stu-id="e6e3c-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="e6e3c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e3c-109">PARAMETERS</span></span>

### <span data-ttu-id="e6e3c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e3c-110">-DefaultProfile</span></span>
<span data-ttu-id="e6e3c-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e3c-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="e6e3c-112">-Destination</span></span>
<span data-ttu-id="e6e3c-113">Elenco degli endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e3c-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="e6e3c-114">-Disable</span></span>
<span data-ttu-id="e6e3c-115">Contrassegno che indica se il gruppo di test è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="e6e3c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e6e3c-116">-Name</span></span>
<span data-ttu-id="e6e3c-117">Nome del gruppo di test.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-117">The test group name.</span></span>

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

### <span data-ttu-id="e6e3c-118">-Source</span><span class="sxs-lookup"><span data-stu-id="e6e3c-118">-Source</span></span>
<span data-ttu-id="e6e3c-119">Elenco degli endpoint di origine.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e3c-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6e3c-120">-TestConfiguration</span></span>
<span data-ttu-id="e6e3c-121">Elenco della configurazione di test.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e3c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6e3c-122">-Confirm</span></span>
<span data-ttu-id="e6e3c-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e3c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e3c-124">-WhatIf</span></span>
<span data-ttu-id="e6e3c-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e3c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e3c-127">CommonParameters</span></span>
<span data-ttu-id="e6e3c-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e3c-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e3c-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6e3c-130">INPUTS</span></span>

### <span data-ttu-id="e6e3c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6e3c-131">None</span></span>

## <span data-ttu-id="e6e3c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e3c-132">OUTPUTS</span></span>

### <span data-ttu-id="e6e3c-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e6e3c-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e6e3c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6e3c-134">NOTES</span></span>

## <span data-ttu-id="e6e3c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e3c-135">RELATED LINKS</span></span>
