---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186246"
---
# <span data-ttu-id="29f97-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="29f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f97-102">SYNOPSIS</span></span>
<span data-ttu-id="29f97-103">Crea un trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="29f97-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="29f97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29f97-104">SYNTAX</span></span>

### <span data-ttu-id="29f97-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="29f97-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29f97-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29f97-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f97-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29f97-107">DESCRIPTION</span></span>
<span data-ttu-id="29f97-108">Il cmdlet **Set-AzDataFactoryV2Trigger** crea un trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="29f97-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="29f97-109">Se si specifica un nome per un trigger già esistente, il cmdlet richiede conferma prima di sostituirlo.</span><span class="sxs-lookup"><span data-stu-id="29f97-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="29f97-110">Se si specifica il _parametro Force,_ il cmdlet sostituisce il trigger esistente senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="29f97-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="29f97-111">I trigger vengono creati nello stato "Arrestato", ovvero non iniziano immediatamente a richiamare pipeline a cui fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="29f97-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="29f97-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29f97-112">EXAMPLES</span></span>

### <span data-ttu-id="29f97-113">Esempio 1: Creare un trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="29f97-114">Creare un nuovo trigger denominato "ScheduledTrigger" nel data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="29f97-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="29f97-115">Il trigger viene creato nello stato "Arrestato", ovvero non viene avviato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="29f97-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="29f97-116">È possibile avviare un trigger con il `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f97-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="29f97-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29f97-117">PARAMETERS</span></span>

### <span data-ttu-id="29f97-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="29f97-118">-DataFactoryName</span></span>
<span data-ttu-id="29f97-119">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="29f97-119">The data factory name.</span></span>

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

### <span data-ttu-id="29f97-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f97-120">-DefaultProfile</span></span>
<span data-ttu-id="29f97-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29f97-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f97-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="29f97-122">-DefinitionFile</span></span>
<span data-ttu-id="29f97-123">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="29f97-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f97-124">-Force</span><span class="sxs-lookup"><span data-stu-id="29f97-124">-Force</span></span>
<span data-ttu-id="29f97-125">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="29f97-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="29f97-126">-Name</span><span class="sxs-lookup"><span data-stu-id="29f97-126">-Name</span></span>
<span data-ttu-id="29f97-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="29f97-127">The trigger name.</span></span>

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

### <span data-ttu-id="29f97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f97-128">-ResourceGroupName</span></span>
<span data-ttu-id="29f97-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29f97-129">The resource group name.</span></span>

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

### <span data-ttu-id="29f97-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29f97-130">-ResourceId</span></span>
<span data-ttu-id="29f97-131">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="29f97-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="29f97-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29f97-132">-Confirm</span></span>
<span data-ttu-id="29f97-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29f97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f97-134">-WhatIf</span></span>
<span data-ttu-id="29f97-135">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="29f97-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="29f97-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f97-136">CommonParameters</span></span>
<span data-ttu-id="29f97-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f97-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f97-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f97-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f97-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="29f97-139">INPUTS</span></span>

### <span data-ttu-id="29f97-140">System.String</span><span class="sxs-lookup"><span data-stu-id="29f97-140">System.String</span></span>

## <span data-ttu-id="29f97-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29f97-141">OUTPUTS</span></span>

### <span data-ttu-id="29f97-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="29f97-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="29f97-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="29f97-143">NOTES</span></span>

## <span data-ttu-id="29f97-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29f97-144">RELATED LINKS</span></span>

[<span data-ttu-id="29f97-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="29f97-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="29f97-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="29f97-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="29f97-148">Remove-AzDataFactoryV2Trigger</span></span>]()
