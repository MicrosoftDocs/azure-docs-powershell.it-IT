---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522145"
---
# <span data-ttu-id="235d2-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="235d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="235d2-102">SYNOPSIS</span></span>

<span data-ttu-id="235d2-103">Avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="235d2-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="235d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="235d2-104">SYNTAX</span></span>

### <span data-ttu-id="235d2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="235d2-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="235d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="235d2-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="235d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="235d2-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="235d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="235d2-108">DESCRIPTION</span></span>

<span data-ttu-id="235d2-109">Il cmdlet **Start-AzureRmDataFactoryV2Trigger** avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="235d2-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="235d2-110">Se il trigger si trova nello stato "Stopped", il cmdlet avvia il trigger e infine richiama le pipeline in base alla relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="235d2-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="235d2-111">Se il trigger è già nello stato "Started", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="235d2-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="235d2-112">Se il parametro Force viene specificato, il cmdlet non viene richiesto prima di avviare il trigger.</span><span class="sxs-lookup"><span data-stu-id="235d2-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="235d2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="235d2-113">EXAMPLES</span></span>

### <span data-ttu-id="235d2-114">Esempio 1: avviare un trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="235d2-115">Avvia un trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="235d2-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="235d2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="235d2-116">PARAMETERS</span></span>

### <span data-ttu-id="235d2-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="235d2-117">-Confirm</span></span>
<span data-ttu-id="235d2-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="235d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="235d2-119">-DataFactoryName</span></span>
<span data-ttu-id="235d2-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="235d2-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="235d2-121">-Force</span></span>
<span data-ttu-id="235d2-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="235d2-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="235d2-123">-Name</span></span>
<span data-ttu-id="235d2-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="235d2-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="235d2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="235d2-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="235d2-127">-ResourceId</span></span>
<span data-ttu-id="235d2-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="235d2-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="235d2-129">-InputObject</span></span>
<span data-ttu-id="235d2-130">Oggetto trigger da avviare.</span><span class="sxs-lookup"><span data-stu-id="235d2-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="235d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235d2-131">-WhatIf</span></span>
<span data-ttu-id="235d2-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="235d2-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="235d2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="235d2-133">INPUTS</span></span>

### <span data-ttu-id="235d2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="235d2-134">System.String</span></span>
<span data-ttu-id="235d2-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="235d2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="235d2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="235d2-136">OUTPUTS</span></span>

### <span data-ttu-id="235d2-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="235d2-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="235d2-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="235d2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="235d2-139">Note</span><span class="sxs-lookup"><span data-stu-id="235d2-139">NOTES</span></span>

## <span data-ttu-id="235d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="235d2-140">RELATED LINKS</span></span>
[<span data-ttu-id="235d2-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="235d2-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="235d2-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="235d2-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="235d2-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
