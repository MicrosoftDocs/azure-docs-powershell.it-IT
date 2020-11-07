---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: ed4769c26363c60aace191d439d4a450a894eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686004"
---
# <span data-ttu-id="0647b-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0647b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0647b-102">SYNOPSIS</span></span>
<span data-ttu-id="0647b-103">Avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="0647b-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0647b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0647b-104">SYNTAX</span></span>

### <span data-ttu-id="0647b-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0647b-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0647b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0647b-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0647b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0647b-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0647b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0647b-108">DESCRIPTION</span></span>
<span data-ttu-id="0647b-109">Il cmdlet **Start-AzureRmDataFactoryV2Trigger** avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="0647b-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="0647b-110">Se il trigger si trova nello stato "Stopped", il cmdlet avvia il trigger e infine richiama le pipeline in base alla relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="0647b-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="0647b-111">Se il trigger è già nello stato "Started", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0647b-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="0647b-112">Se il parametro Force viene specificato, il cmdlet non viene richiesto prima di avviare il trigger.</span><span class="sxs-lookup"><span data-stu-id="0647b-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="0647b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0647b-113">EXAMPLES</span></span>

### <span data-ttu-id="0647b-114">Esempio 1: avviare un trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="0647b-115">Avvia un trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="0647b-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="0647b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0647b-116">PARAMETERS</span></span>

### <span data-ttu-id="0647b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0647b-117">-DataFactoryName</span></span>
<span data-ttu-id="0647b-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0647b-118">The data factory name.</span></span>

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

### <span data-ttu-id="0647b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0647b-119">-DefaultProfile</span></span>
<span data-ttu-id="0647b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0647b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0647b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0647b-121">-Force</span></span>
<span data-ttu-id="0647b-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0647b-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0647b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0647b-123">-InputObject</span></span>
<span data-ttu-id="0647b-124">Oggetto trigger da avviare.</span><span class="sxs-lookup"><span data-stu-id="0647b-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="0647b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0647b-125">-Name</span></span>
<span data-ttu-id="0647b-126">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="0647b-126">The trigger name.</span></span>

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

### <span data-ttu-id="0647b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0647b-127">-ResourceGroupName</span></span>
<span data-ttu-id="0647b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0647b-128">The resource group name.</span></span>

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

### <span data-ttu-id="0647b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0647b-129">-ResourceId</span></span>
<span data-ttu-id="0647b-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="0647b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0647b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0647b-131">-Confirm</span></span>
<span data-ttu-id="0647b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0647b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0647b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0647b-133">-WhatIf</span></span>
<span data-ttu-id="0647b-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0647b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0647b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0647b-135">CommonParameters</span></span>
<span data-ttu-id="0647b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0647b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0647b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0647b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0647b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0647b-138">INPUTS</span></span>

### <span data-ttu-id="0647b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0647b-139">System.String</span></span>
<span data-ttu-id="0647b-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0647b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0647b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0647b-141">OUTPUTS</span></span>

### <span data-ttu-id="0647b-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0647b-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0647b-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0647b-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0647b-144">Note</span><span class="sxs-lookup"><span data-stu-id="0647b-144">NOTES</span></span>

## <span data-ttu-id="0647b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0647b-145">RELATED LINKS</span></span>

[<span data-ttu-id="0647b-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0647b-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0647b-148">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0647b-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0647b-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
