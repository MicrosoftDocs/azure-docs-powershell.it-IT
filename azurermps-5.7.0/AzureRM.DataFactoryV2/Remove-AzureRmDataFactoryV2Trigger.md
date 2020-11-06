---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 82af1131e2730cf1f78c0c04ff8540e2ef371d2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508196"
---
# <span data-ttu-id="0f48f-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0f48f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f48f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f48f-103">Rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="0f48f-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f48f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f48f-104">SYNTAX</span></span>

### <span data-ttu-id="0f48f-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f48f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f48f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f48f-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f48f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f48f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f48f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f48f-108">DESCRIPTION</span></span>
<span data-ttu-id="0f48f-109">Il cmdlet **Remove-AzureRmDataFactoryV2Trigger** rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="0f48f-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="0f48f-110">Se il parametro _Force_ viene specificato, il cmdlet non viene richiesto prima di rimuovere il trigger.</span><span class="sxs-lookup"><span data-stu-id="0f48f-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="0f48f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f48f-111">EXAMPLES</span></span>

### <span data-ttu-id="0f48f-112">Esempio 1: rimuovere un trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="0f48f-113">Rimuovere un trigger denominato "ScheduledTrigger" dalla data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="0f48f-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="0f48f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f48f-114">PARAMETERS</span></span>

### <span data-ttu-id="0f48f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0f48f-115">-DataFactoryName</span></span>
<span data-ttu-id="0f48f-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0f48f-116">The data factory name.</span></span>

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

### <span data-ttu-id="0f48f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f48f-117">-DefaultProfile</span></span>
<span data-ttu-id="0f48f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f48f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f48f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0f48f-119">-Force</span></span>
<span data-ttu-id="0f48f-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0f48f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0f48f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f48f-121">-InputObject</span></span>
<span data-ttu-id="0f48f-122">Oggetto trigger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0f48f-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="0f48f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f48f-123">-Name</span></span>
<span data-ttu-id="0f48f-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="0f48f-124">The trigger name.</span></span>

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

### <span data-ttu-id="0f48f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f48f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f48f-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f48f-126">The resource group name.</span></span>

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

### <span data-ttu-id="0f48f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f48f-127">-ResourceId</span></span>
<span data-ttu-id="0f48f-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f48f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0f48f-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f48f-129">-Confirm</span></span>
<span data-ttu-id="0f48f-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f48f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f48f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f48f-131">-WhatIf</span></span>
<span data-ttu-id="0f48f-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f48f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0f48f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f48f-133">CommonParameters</span></span>
<span data-ttu-id="0f48f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f48f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f48f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f48f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f48f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f48f-136">INPUTS</span></span>

### <span data-ttu-id="0f48f-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="0f48f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0f48f-138">System.String</span></span>

## <span data-ttu-id="0f48f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f48f-139">OUTPUTS</span></span>

### <span data-ttu-id="0f48f-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="0f48f-140">System.Object</span></span>

## <span data-ttu-id="0f48f-141">Note</span><span class="sxs-lookup"><span data-stu-id="0f48f-141">NOTES</span></span>

## <span data-ttu-id="0f48f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f48f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f48f-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f48f-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f48f-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f48f-146">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f48f-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

