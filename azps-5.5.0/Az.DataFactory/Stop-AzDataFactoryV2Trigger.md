---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177135"
---
# <span data-ttu-id="5003a-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5003a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5003a-102">SYNOPSIS</span></span>
<span data-ttu-id="5003a-103">Interrompe un trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="5003a-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="5003a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5003a-104">SYNTAX</span></span>

### <span data-ttu-id="5003a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5003a-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5003a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5003a-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5003a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5003a-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5003a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5003a-108">DESCRIPTION</span></span>
<span data-ttu-id="5003a-109">Il cmdlet **Stop-AzDataFactoryV2Trigger** interrompe un trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="5003a-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="5003a-110">Se il trigger è nello stato "Avviato", il cmdlet interrompe il trigger e non richiama più pipeline.</span><span class="sxs-lookup"><span data-stu-id="5003a-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="5003a-111">Se il trigger è già in stato "Arrestato", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="5003a-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="5003a-112">Se si specifica il parametro Force, il cmdlet non richiede conferma prima di interrompere il trigger.</span><span class="sxs-lookup"><span data-stu-id="5003a-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="5003a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5003a-113">EXAMPLES</span></span>

### <span data-ttu-id="5003a-114">Esempio 1: Interrompere un trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5003a-115">Interrompe un trigger denominato "ScheduledTrigger" nel data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5003a-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5003a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5003a-116">PARAMETERS</span></span>

### <span data-ttu-id="5003a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5003a-117">-DataFactoryName</span></span>
<span data-ttu-id="5003a-118">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="5003a-118">The data factory name.</span></span>

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

### <span data-ttu-id="5003a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5003a-119">-DefaultProfile</span></span>
<span data-ttu-id="5003a-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5003a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5003a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5003a-121">-Force</span></span>
<span data-ttu-id="5003a-122">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5003a-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5003a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5003a-123">-InputObject</span></span>
<span data-ttu-id="5003a-124">Impostare un trigger per avviare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5003a-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="5003a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5003a-125">-Name</span></span>
<span data-ttu-id="5003a-126">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="5003a-126">The trigger name.</span></span>

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

### <span data-ttu-id="5003a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5003a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5003a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5003a-128">The resource group name.</span></span>

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

### <span data-ttu-id="5003a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5003a-129">-ResourceId</span></span>
<span data-ttu-id="5003a-130">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="5003a-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5003a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5003a-131">-Confirm</span></span>
<span data-ttu-id="5003a-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5003a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5003a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5003a-133">-WhatIf</span></span>
<span data-ttu-id="5003a-134">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="5003a-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5003a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5003a-135">CommonParameters</span></span>
<span data-ttu-id="5003a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5003a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5003a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5003a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5003a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="5003a-138">INPUTS</span></span>

### <span data-ttu-id="5003a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5003a-139">System.String</span></span>

### <span data-ttu-id="5003a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5003a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5003a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5003a-141">OUTPUTS</span></span>

### <span data-ttu-id="5003a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5003a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5003a-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5003a-143">NOTES</span></span>

## <span data-ttu-id="5003a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5003a-144">RELATED LINKS</span></span>

[<span data-ttu-id="5003a-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5003a-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5003a-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5003a-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5003a-148">Remove-AzDataFactoryV2Trigger</span></span>]()
