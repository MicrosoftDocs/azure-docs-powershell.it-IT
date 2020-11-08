---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200610"
---
# <span data-ttu-id="6a34e-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="6a34e-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="6a34e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a34e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a34e-103">Restituisce informazioni sulle esecuzioni dei trigger.</span><span class="sxs-lookup"><span data-stu-id="6a34e-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="6a34e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a34e-104">SYNTAX</span></span>

### <span data-ttu-id="6a34e-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a34e-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a34e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="6a34e-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a34e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a34e-107">DESCRIPTION</span></span>
<span data-ttu-id="6a34e-108">Il comando **Get-AzSynapseTriggerRun** restituisce informazioni dettagliate sulle esecuzioni dei trigger per il trigger specificato nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="6a34e-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="6a34e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a34e-109">EXAMPLES</span></span>

### <span data-ttu-id="6a34e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a34e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="6a34e-111">Questo comando Mostra le informazioni sulle esecuzioni per ContosoTrigger nell'area di lavoro ContosoWorkspace iniziata tra "2018-09-01T21:00" e "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="6a34e-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="6a34e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a34e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="6a34e-113">Questo comando Mostra le informazioni sulle esecuzioni per ContosoTrigger nell'area di lavoro ContosoWorkspace iniziata tra "2018-09-01T21:00" e "2019-09-01T21:00" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a34e-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="6a34e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a34e-114">PARAMETERS</span></span>

### <span data-ttu-id="6a34e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a34e-115">-DefaultProfile</span></span>
<span data-ttu-id="6a34e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a34e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a34e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a34e-117">-Name</span></span>
<span data-ttu-id="6a34e-118">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="6a34e-118">The trigger name.</span></span>

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

### <span data-ttu-id="6a34e-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="6a34e-119">-RunStartedAfter</span></span>
<span data-ttu-id="6a34e-120">Intervallo di tempo in cui l'evento di esecuzione è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="6a34e-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="6a34e-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="6a34e-121">-RunStartedBefore</span></span>
<span data-ttu-id="6a34e-122">Il periodo di tempo in cui l'evento Run è stato aggiornato in formato "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="6a34e-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="6a34e-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a34e-123">-WorkspaceName</span></span>
<span data-ttu-id="6a34e-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="6a34e-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6a34e-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a34e-125">-WorkspaceObject</span></span>
<span data-ttu-id="6a34e-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a34e-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6a34e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a34e-127">CommonParameters</span></span>
<span data-ttu-id="6a34e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a34e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a34e-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a34e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a34e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a34e-130">INPUTS</span></span>

### <span data-ttu-id="6a34e-131">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a34e-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6a34e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a34e-132">OUTPUTS</span></span>

### <span data-ttu-id="6a34e-133">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="6a34e-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="6a34e-134">Note</span><span class="sxs-lookup"><span data-stu-id="6a34e-134">NOTES</span></span>

## <span data-ttu-id="6a34e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a34e-135">RELATED LINKS</span></span>