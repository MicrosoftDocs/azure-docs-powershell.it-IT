---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 8e4f547d615a88957ffbf133dd725e2453ef7a11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686847"
---
# <span data-ttu-id="8c462-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8c462-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c462-102">SYNOPSIS</span></span>
<span data-ttu-id="8c462-103">Arresta un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="8c462-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c462-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c462-104">SYNTAX</span></span>

### <span data-ttu-id="8c462-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c462-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c462-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c462-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c462-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c462-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c462-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c462-108">DESCRIPTION</span></span>
<span data-ttu-id="8c462-109">Il cmdlet **Stop-AzureRmDataFactoryV2Trigger** arresta un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="8c462-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="8c462-110">Se il trigger si trova nello stato "iniziato", il cmdlet interrompe il trigger e non richiama più le pipeline.</span><span class="sxs-lookup"><span data-stu-id="8c462-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="8c462-111">Se il trigger è già nello stato "Stopped", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="8c462-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="8c462-112">Se il parametro Force viene specificato, il cmdlet non viene richiesto prima di arrestare il trigger.</span><span class="sxs-lookup"><span data-stu-id="8c462-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="8c462-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c462-113">EXAMPLES</span></span>

### <span data-ttu-id="8c462-114">Esempio 1: arrestare un trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="8c462-115">Interrompe un trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8c462-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="8c462-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c462-116">PARAMETERS</span></span>

### <span data-ttu-id="8c462-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c462-117">-Confirm</span></span>
<span data-ttu-id="8c462-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c462-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c462-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8c462-119">-DataFactoryName</span></span>
<span data-ttu-id="8c462-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8c462-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8c462-121">-Force</span></span>
<span data-ttu-id="8c462-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8c462-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8c462-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c462-123">-Name</span></span>
<span data-ttu-id="8c462-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="8c462-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c462-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c462-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c462-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c462-127">-ResourceId</span></span>
<span data-ttu-id="8c462-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c462-128">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c462-129">-InputObject</span></span>
<span data-ttu-id="8c462-130">Oggetto trigger da avviare.</span><span class="sxs-lookup"><span data-stu-id="8c462-130">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c462-131">-WhatIf</span></span>
<span data-ttu-id="8c462-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c462-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8c462-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c462-133">-DefaultProfile</span></span>
<span data-ttu-id="8c462-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c462-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c462-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c462-135">CommonParameters</span></span>
<span data-ttu-id="8c462-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c462-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c462-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c462-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c462-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c462-138">INPUTS</span></span>

### <span data-ttu-id="8c462-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8c462-139">System.String</span></span>
<span data-ttu-id="8c462-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8c462-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8c462-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c462-141">OUTPUTS</span></span>

### <span data-ttu-id="8c462-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8c462-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8c462-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8c462-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8c462-144">Note</span><span class="sxs-lookup"><span data-stu-id="8c462-144">NOTES</span></span>

## <span data-ttu-id="8c462-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c462-145">RELATED LINKS</span></span>

[<span data-ttu-id="8c462-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c462-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c462-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c462-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c462-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()