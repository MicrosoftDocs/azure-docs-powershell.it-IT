---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 988f63d9f894de95c4206dc05bcda66e68f3c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684572"
---
# <span data-ttu-id="779b3-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="779b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="779b3-102">SYNOPSIS</span></span>
<span data-ttu-id="779b3-103">Avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="779b3-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="779b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="779b3-104">SYNTAX</span></span>

### <span data-ttu-id="779b3-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="779b3-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779b3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="779b3-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="779b3-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="779b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="779b3-108">DESCRIPTION</span></span>
<span data-ttu-id="779b3-109">Il cmdlet **Start-AzDataFactoryV2Trigger** avvia un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="779b3-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="779b3-110">Se il trigger si trova nello stato "Stopped", il cmdlet avvia il trigger e infine richiama le pipeline in base alla relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="779b3-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="779b3-111">Se il trigger è già nello stato "Started", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="779b3-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="779b3-112">Se il parametro Force viene specificato, il cmdlet non viene richiesto prima di avviare il trigger.</span><span class="sxs-lookup"><span data-stu-id="779b3-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="779b3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="779b3-113">EXAMPLES</span></span>

### <span data-ttu-id="779b3-114">Esempio 1: avviare un trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="779b3-115">Avvia un trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="779b3-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="779b3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="779b3-116">PARAMETERS</span></span>

### <span data-ttu-id="779b3-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="779b3-117">-DataFactoryName</span></span>
<span data-ttu-id="779b3-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="779b3-118">The data factory name.</span></span>

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

### <span data-ttu-id="779b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779b3-119">-DefaultProfile</span></span>
<span data-ttu-id="779b3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="779b3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="779b3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="779b3-121">-Force</span></span>
<span data-ttu-id="779b3-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="779b3-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="779b3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="779b3-123">-InputObject</span></span>
<span data-ttu-id="779b3-124">Oggetto trigger da avviare.</span><span class="sxs-lookup"><span data-stu-id="779b3-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="779b3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="779b3-125">-Name</span></span>
<span data-ttu-id="779b3-126">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="779b3-126">The trigger name.</span></span>

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

### <span data-ttu-id="779b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="779b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="779b3-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="779b3-128">The resource group name.</span></span>

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

### <span data-ttu-id="779b3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="779b3-129">-ResourceId</span></span>
<span data-ttu-id="779b3-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="779b3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="779b3-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="779b3-131">-Confirm</span></span>
<span data-ttu-id="779b3-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="779b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="779b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="779b3-133">-WhatIf</span></span>
<span data-ttu-id="779b3-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="779b3-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="779b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779b3-135">CommonParameters</span></span>
<span data-ttu-id="779b3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779b3-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779b3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779b3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="779b3-138">INPUTS</span></span>

### <span data-ttu-id="779b3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="779b3-139">System.String</span></span>

### <span data-ttu-id="779b3-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="779b3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="779b3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="779b3-141">OUTPUTS</span></span>

### <span data-ttu-id="779b3-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="779b3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="779b3-143">Note</span><span class="sxs-lookup"><span data-stu-id="779b3-143">NOTES</span></span>

## <span data-ttu-id="779b3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="779b3-144">RELATED LINKS</span></span>

[<span data-ttu-id="779b3-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="779b3-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="779b3-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="779b3-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="779b3-148">Remove-AzDataFactoryV2Trigger</span></span>]()
