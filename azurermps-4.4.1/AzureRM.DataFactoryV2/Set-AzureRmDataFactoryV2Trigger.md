---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8bf4a713784b367363e4f1f9167cfb144d06c0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522147"
---
# <span data-ttu-id="6acbb-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6acbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6acbb-102">SYNOPSIS</span></span>
<span data-ttu-id="6acbb-103">Crea un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="6acbb-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6acbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6acbb-104">SYNTAX</span></span>

### <span data-ttu-id="6acbb-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6acbb-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6acbb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6acbb-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6acbb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6acbb-107">DESCRIPTION</span></span>

<span data-ttu-id="6acbb-108">Il cmdlet **set-AzureRmDataFactoryV2Trigger** crea un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="6acbb-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="6acbb-109">Se si specifica un nome per un trigger già esistente, il cmdlet richiede la conferma prima di sostituire il trigger.</span><span class="sxs-lookup"><span data-stu-id="6acbb-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="6acbb-110">Se specifichi il parametro _Force_ , il cmdlet sostituisce il trigger esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6acbb-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="6acbb-111">I trigger vengono creati nello stato "Stopped", quindi non iniziano immediatamente a richiamare pipeline a cui fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="6acbb-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="6acbb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6acbb-112">EXAMPLES</span></span>

### <span data-ttu-id="6acbb-113">Esempio 1: creare un trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

```

<span data-ttu-id="6acbb-114">Creare un nuovo trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6acbb-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="6acbb-115">Il trigger viene creato nello stato "Stopped", quindi non si avvia immediatamente.</span><span class="sxs-lookup"><span data-stu-id="6acbb-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="6acbb-116">È possibile avviare un trigger usando il `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acbb-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="6acbb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6acbb-117">PARAMETERS</span></span>

### <span data-ttu-id="6acbb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6acbb-118">-Confirm</span></span>
<span data-ttu-id="6acbb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acbb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acbb-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6acbb-120">-DataFactoryName</span></span>
<span data-ttu-id="6acbb-121">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6acbb-121">The data factory name.</span></span>

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

### <span data-ttu-id="6acbb-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6acbb-122">-DefinitionFile</span></span>
<span data-ttu-id="6acbb-123">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="6acbb-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6acbb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6acbb-124">-Force</span></span>
<span data-ttu-id="6acbb-125">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6acbb-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6acbb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6acbb-126">-Name</span></span>
<span data-ttu-id="6acbb-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="6acbb-127">The trigger name.</span></span>

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

### <span data-ttu-id="6acbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="6acbb-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6acbb-129">The resource group name.</span></span>

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

### <span data-ttu-id="6acbb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6acbb-130">-ResourceId</span></span>
<span data-ttu-id="6acbb-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="6acbb-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6acbb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acbb-132">-WhatIf</span></span>
<span data-ttu-id="6acbb-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6acbb-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="6acbb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6acbb-134">INPUTS</span></span>

### <span data-ttu-id="6acbb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6acbb-135">System.String</span></span>


## <span data-ttu-id="6acbb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6acbb-136">OUTPUTS</span></span>

### <span data-ttu-id="6acbb-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="6acbb-138">Note</span><span class="sxs-lookup"><span data-stu-id="6acbb-138">NOTES</span></span>

## <span data-ttu-id="6acbb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6acbb-139">RELATED LINKS</span></span>
[<span data-ttu-id="6acbb-140">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-140">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6acbb-141">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-141">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6acbb-142">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-142">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6acbb-143">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6acbb-143">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
