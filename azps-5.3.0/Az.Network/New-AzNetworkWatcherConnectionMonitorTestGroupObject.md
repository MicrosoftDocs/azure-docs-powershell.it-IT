---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379060"
---
# <span data-ttu-id="1452c-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="1452c-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="1452c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1452c-102">SYNOPSIS</span></span>
<span data-ttu-id="1452c-103">Creare un gruppo di test per il monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="1452c-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="1452c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1452c-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1452c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1452c-105">DESCRIPTION</span></span>
<span data-ttu-id="1452c-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorTestGroupObject crea un gruppo di test per il monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="1452c-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="1452c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1452c-107">EXAMPLES</span></span>

### <span data-ttu-id="1452c-108">Esempio 1: creare un gruppo di test con 2 testConfigurations, w source e 2 endpoint di destinazione</span><span class="sxs-lookup"><span data-stu-id="1452c-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="1452c-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1452c-109">PARAMETERS</span></span>

### <span data-ttu-id="1452c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1452c-110">-DefaultProfile</span></span>
<span data-ttu-id="1452c-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1452c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1452c-112">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="1452c-112">-Destination</span></span>
<span data-ttu-id="1452c-113">Elenco di endpoint di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1452c-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="1452c-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="1452c-114">-Disable</span></span>
<span data-ttu-id="1452c-115">Contrassegno che indica se il gruppo di test è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="1452c-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="1452c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1452c-116">-Name</span></span>
<span data-ttu-id="1452c-117">Nome del gruppo di test.</span><span class="sxs-lookup"><span data-stu-id="1452c-117">The test group name.</span></span>

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

### <span data-ttu-id="1452c-118">-Origine</span><span class="sxs-lookup"><span data-stu-id="1452c-118">-Source</span></span>
<span data-ttu-id="1452c-119">Elenco di endpoint di origine.</span><span class="sxs-lookup"><span data-stu-id="1452c-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="1452c-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="1452c-120">-TestConfiguration</span></span>
<span data-ttu-id="1452c-121">Elenco della configurazione di test.</span><span class="sxs-lookup"><span data-stu-id="1452c-121">List of test configuration.</span></span>

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

### <span data-ttu-id="1452c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1452c-122">-Confirm</span></span>
<span data-ttu-id="1452c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1452c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1452c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1452c-124">-WhatIf</span></span>
<span data-ttu-id="1452c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1452c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1452c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1452c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1452c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1452c-127">CommonParameters</span></span>
<span data-ttu-id="1452c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1452c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1452c-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1452c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1452c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1452c-130">INPUTS</span></span>

### <span data-ttu-id="1452c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1452c-131">None</span></span>

## <span data-ttu-id="1452c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1452c-132">OUTPUTS</span></span>

### <span data-ttu-id="1452c-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="1452c-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="1452c-134">Note</span><span class="sxs-lookup"><span data-stu-id="1452c-134">NOTES</span></span>

## <span data-ttu-id="1452c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1452c-135">RELATED LINKS</span></span>
