---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977949"
---
# <span data-ttu-id="758b9-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="758b9-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="758b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758b9-102">SYNOPSIS</span></span>
<span data-ttu-id="758b9-103">Restituisce informazioni sulle esecuzioni del trigger.</span><span class="sxs-lookup"><span data-stu-id="758b9-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="758b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="758b9-104">SYNTAX</span></span>

### <span data-ttu-id="758b9-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="758b9-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="758b9-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="758b9-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="758b9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="758b9-107">DESCRIPTION</span></span>
<span data-ttu-id="758b9-108">Il **comando Get-AzSynapseTriggerRun** restituisce informazioni dettagliate sull'esecuzione del trigger per il trigger specificato nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="758b9-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="758b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="758b9-109">EXAMPLES</span></span>

### <span data-ttu-id="758b9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="758b9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="758b9-111">Questo comando mostra informazioni sulle esecuzioni di ContosoTrigger nell'area di lavoro ContosoWorkspace iniziate tra "2018-09-01T21:00" e "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="758b9-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="758b9-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="758b9-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="758b9-113">Questo comando mostra informazioni sulle esecuzioni di ContosoTrigger nell'area di lavoro ContosoWorkspace iniziate tra il "2018-09-01T21:00" e "2019-09-01T21:00" alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="758b9-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="758b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="758b9-114">PARAMETERS</span></span>

### <span data-ttu-id="758b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758b9-115">-DefaultProfile</span></span>
<span data-ttu-id="758b9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="758b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="758b9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="758b9-117">-Name</span></span>
<span data-ttu-id="758b9-118">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="758b9-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758b9-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="758b9-119">-RunStartedAfter</span></span>
<span data-ttu-id="758b9-120">L'ora in cui l'evento di esecuzione è stato aggiornato nel formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="758b9-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758b9-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="758b9-121">-RunStartedBefore</span></span>
<span data-ttu-id="758b9-122">L'ora in cui l'evento di esecuzione è stato aggiornato nel formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="758b9-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758b9-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="758b9-123">-WorkspaceName</span></span>
<span data-ttu-id="758b9-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="758b9-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758b9-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="758b9-125">-WorkspaceObject</span></span>
<span data-ttu-id="758b9-126">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="758b9-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="758b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758b9-127">CommonParameters</span></span>
<span data-ttu-id="758b9-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758b9-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="758b9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758b9-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="758b9-130">INPUTS</span></span>

### <span data-ttu-id="758b9-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="758b9-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="758b9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="758b9-132">OUTPUTS</span></span>

### <span data-ttu-id="758b9-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="758b9-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="758b9-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="758b9-134">NOTES</span></span>

## <span data-ttu-id="758b9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="758b9-135">RELATED LINKS</span></span>
