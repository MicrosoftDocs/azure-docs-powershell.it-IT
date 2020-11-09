---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298188"
---
# <span data-ttu-id="88b24-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="88b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88b24-102">SYNOPSIS</span></span>
<span data-ttu-id="88b24-103">Arresta un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="88b24-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="88b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88b24-104">SYNTAX</span></span>

### <span data-ttu-id="88b24-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88b24-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b24-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="88b24-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b24-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88b24-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88b24-108">DESCRIPTION</span></span>
<span data-ttu-id="88b24-109">Il cmdlet **Stop-AzDataFactoryV2Trigger** arresta un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="88b24-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="88b24-110">Se il trigger si trova nello stato "iniziato", il cmdlet interrompe il trigger e non richiama più le pipeline.</span><span class="sxs-lookup"><span data-stu-id="88b24-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="88b24-111">Se il trigger è già nello stato "Stopped", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="88b24-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="88b24-112">Se il parametro Force viene specificato, il cmdlet non viene richiesto prima di arrestare il trigger.</span><span class="sxs-lookup"><span data-stu-id="88b24-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="88b24-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88b24-113">EXAMPLES</span></span>

### <span data-ttu-id="88b24-114">Esempio 1: arrestare un trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="88b24-115">Interrompe un trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="88b24-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="88b24-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88b24-116">PARAMETERS</span></span>

### <span data-ttu-id="88b24-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="88b24-117">-DataFactoryName</span></span>
<span data-ttu-id="88b24-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="88b24-118">The data factory name.</span></span>

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

### <span data-ttu-id="88b24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b24-119">-DefaultProfile</span></span>
<span data-ttu-id="88b24-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88b24-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88b24-121">-Force</span><span class="sxs-lookup"><span data-stu-id="88b24-121">-Force</span></span>
<span data-ttu-id="88b24-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="88b24-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="88b24-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88b24-123">-InputObject</span></span>
<span data-ttu-id="88b24-124">Oggetto trigger da avviare.</span><span class="sxs-lookup"><span data-stu-id="88b24-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="88b24-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="88b24-125">-Name</span></span>
<span data-ttu-id="88b24-126">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="88b24-126">The trigger name.</span></span>

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

### <span data-ttu-id="88b24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b24-127">-ResourceGroupName</span></span>
<span data-ttu-id="88b24-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88b24-128">The resource group name.</span></span>

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

### <span data-ttu-id="88b24-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88b24-129">-ResourceId</span></span>
<span data-ttu-id="88b24-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="88b24-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="88b24-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88b24-131">-Confirm</span></span>
<span data-ttu-id="88b24-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b24-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b24-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b24-133">-WhatIf</span></span>
<span data-ttu-id="88b24-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b24-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="88b24-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b24-135">CommonParameters</span></span>
<span data-ttu-id="88b24-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b24-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b24-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b24-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b24-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88b24-138">INPUTS</span></span>

### <span data-ttu-id="88b24-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88b24-139">System.String</span></span>

### <span data-ttu-id="88b24-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="88b24-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="88b24-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88b24-141">OUTPUTS</span></span>

### <span data-ttu-id="88b24-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="88b24-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="88b24-143">Note</span><span class="sxs-lookup"><span data-stu-id="88b24-143">NOTES</span></span>

## <span data-ttu-id="88b24-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88b24-144">RELATED LINKS</span></span>

[<span data-ttu-id="88b24-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88b24-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88b24-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="88b24-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="88b24-148">Remove-AzDataFactoryV2Trigger</span></span>]()
