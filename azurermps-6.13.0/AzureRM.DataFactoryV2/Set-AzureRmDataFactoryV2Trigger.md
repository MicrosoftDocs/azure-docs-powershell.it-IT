---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515408"
---
# <span data-ttu-id="aa369-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="aa369-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa369-102">SYNOPSIS</span></span>
<span data-ttu-id="aa369-103">Crea un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="aa369-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa369-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa369-104">SYNTAX</span></span>

### <span data-ttu-id="aa369-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa369-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa369-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa369-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa369-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa369-107">DESCRIPTION</span></span>
<span data-ttu-id="aa369-108">Il cmdlet **set-AzureRmDataFactoryV2Trigger** crea un trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="aa369-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="aa369-109">Se si specifica un nome per un trigger già esistente, il cmdlet richiede la conferma prima di sostituire il trigger.</span><span class="sxs-lookup"><span data-stu-id="aa369-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="aa369-110">Se specifichi il parametro _Force_ , il cmdlet sostituisce il trigger esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aa369-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="aa369-111">I trigger vengono creati nello stato "Stopped", quindi non iniziano immediatamente a richiamare pipeline a cui fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="aa369-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="aa369-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa369-112">EXAMPLES</span></span>

### <span data-ttu-id="aa369-113">Esempio 1: creare un trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="aa369-114">Creare un nuovo trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="aa369-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="aa369-115">Il trigger viene creato nello stato "Stopped", quindi non si avvia immediatamente.</span><span class="sxs-lookup"><span data-stu-id="aa369-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="aa369-116">È possibile avviare un trigger usando il `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa369-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="aa369-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa369-117">PARAMETERS</span></span>

### <span data-ttu-id="aa369-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="aa369-118">-DataFactoryName</span></span>
<span data-ttu-id="aa369-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="aa369-119">The data factory name.</span></span>

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

### <span data-ttu-id="aa369-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa369-120">-DefaultProfile</span></span>
<span data-ttu-id="aa369-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa369-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa369-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="aa369-122">-DefinitionFile</span></span>
<span data-ttu-id="aa369-123">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="aa369-123">The JSON file path.</span></span>

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

### <span data-ttu-id="aa369-124">-Force</span><span class="sxs-lookup"><span data-stu-id="aa369-124">-Force</span></span>
<span data-ttu-id="aa369-125">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="aa369-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="aa369-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa369-126">-Name</span></span>
<span data-ttu-id="aa369-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="aa369-127">The trigger name.</span></span>

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

### <span data-ttu-id="aa369-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa369-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa369-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa369-129">The resource group name.</span></span>

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

### <span data-ttu-id="aa369-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa369-130">-ResourceId</span></span>
<span data-ttu-id="aa369-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa369-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="aa369-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa369-132">-Confirm</span></span>
<span data-ttu-id="aa369-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa369-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa369-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa369-134">-WhatIf</span></span>
<span data-ttu-id="aa369-135">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa369-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="aa369-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa369-136">CommonParameters</span></span>
<span data-ttu-id="aa369-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa369-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa369-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa369-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa369-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa369-139">INPUTS</span></span>

### <span data-ttu-id="aa369-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aa369-140">System.String</span></span>

## <span data-ttu-id="aa369-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa369-141">OUTPUTS</span></span>

### <span data-ttu-id="aa369-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="aa369-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="aa369-143">Note</span><span class="sxs-lookup"><span data-stu-id="aa369-143">NOTES</span></span>

## <span data-ttu-id="aa369-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa369-144">RELATED LINKS</span></span>

[<span data-ttu-id="aa369-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="aa369-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="aa369-147">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="aa369-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="aa369-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
