---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522154"
---
# <span data-ttu-id="499cb-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="499cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="499cb-102">SYNOPSIS</span></span>
<span data-ttu-id="499cb-103">Rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="499cb-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="499cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="499cb-104">SYNTAX</span></span>

### <span data-ttu-id="499cb-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="499cb-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="499cb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="499cb-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="499cb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="499cb-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="499cb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="499cb-108">DESCRIPTION</span></span>
<span data-ttu-id="499cb-109">Il cmdlet **Remove-AzureRmDataFactoryV2Trigger** rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="499cb-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="499cb-110">Se il parametro _Force_ viene specificato, il cmdlet non viene richiesto prima di rimuovere il trigger.</span><span class="sxs-lookup"><span data-stu-id="499cb-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="499cb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="499cb-111">EXAMPLES</span></span>

### <span data-ttu-id="499cb-112">Esempio 1: rimuovere un trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="499cb-113">Rimuovere un trigger denominato "ScheduledTrigger" dalla data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="499cb-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="499cb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="499cb-114">PARAMETERS</span></span>

### <span data-ttu-id="499cb-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="499cb-115">-Confirm</span></span>
<span data-ttu-id="499cb-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="499cb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="499cb-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="499cb-117">-DataFactoryName</span></span>
<span data-ttu-id="499cb-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="499cb-118">The data factory name.</span></span>

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

### <span data-ttu-id="499cb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="499cb-119">-Force</span></span>
<span data-ttu-id="499cb-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="499cb-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="499cb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="499cb-121">-Name</span></span>
<span data-ttu-id="499cb-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="499cb-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="499cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="499cb-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="499cb-124">The resource group name.</span></span>

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

### <span data-ttu-id="499cb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="499cb-125">-ResourceId</span></span>
<span data-ttu-id="499cb-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="499cb-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="499cb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="499cb-127">-InputObject</span></span>
<span data-ttu-id="499cb-128">Oggetto trigger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="499cb-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="499cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499cb-129">-WhatIf</span></span>
<span data-ttu-id="499cb-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="499cb-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="499cb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="499cb-131">INPUTS</span></span>

### <span data-ttu-id="499cb-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="499cb-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="499cb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="499cb-133">System.String</span></span>


## <span data-ttu-id="499cb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="499cb-134">OUTPUTS</span></span>

### <span data-ttu-id="499cb-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="499cb-135">System.Object</span></span>

## <span data-ttu-id="499cb-136">Note</span><span class="sxs-lookup"><span data-stu-id="499cb-136">NOTES</span></span>

## <span data-ttu-id="499cb-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="499cb-137">RELATED LINKS</span></span>
[<span data-ttu-id="499cb-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="499cb-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="499cb-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="499cb-141">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="499cb-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

