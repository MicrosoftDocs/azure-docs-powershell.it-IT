---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508568"
---
# <span data-ttu-id="010a0-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="010a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="010a0-102">SYNOPSIS</span></span>
<span data-ttu-id="010a0-103">Rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="010a0-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="010a0-104">SYNTAX</span></span>

### <span data-ttu-id="010a0-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="010a0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="010a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="010a0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="010a0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="010a0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="010a0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="010a0-108">DESCRIPTION</span></span>
<span data-ttu-id="010a0-109">Il cmdlet **Remove-AzureRmDataFactoryV2Trigger** rimuove un trigger da una data factory.</span><span class="sxs-lookup"><span data-stu-id="010a0-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="010a0-110">Se il parametro _Force_ viene specificato, il cmdlet non viene richiesto prima di rimuovere il trigger.</span><span class="sxs-lookup"><span data-stu-id="010a0-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="010a0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="010a0-111">EXAMPLES</span></span>

### <span data-ttu-id="010a0-112">Esempio 1: rimuovere un trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="010a0-113">Rimuovere un trigger denominato "ScheduledTrigger" dalla data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="010a0-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="010a0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="010a0-114">PARAMETERS</span></span>

### <span data-ttu-id="010a0-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="010a0-115">-Confirm</span></span>
<span data-ttu-id="010a0-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="010a0-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="010a0-117">-DataFactoryName</span></span>
<span data-ttu-id="010a0-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="010a0-118">The data factory name.</span></span>

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

### <span data-ttu-id="010a0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="010a0-119">-Force</span></span>
<span data-ttu-id="010a0-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="010a0-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="010a0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="010a0-121">-Name</span></span>
<span data-ttu-id="010a0-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="010a0-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="010a0-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="010a0-124">The resource group name.</span></span>

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

### <span data-ttu-id="010a0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="010a0-125">-ResourceId</span></span>
<span data-ttu-id="010a0-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="010a0-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="010a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="010a0-127">-InputObject</span></span>
<span data-ttu-id="010a0-128">Oggetto trigger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="010a0-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="010a0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010a0-129">-WhatIf</span></span>
<span data-ttu-id="010a0-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="010a0-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="010a0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010a0-131">-DefaultProfile</span></span>
<span data-ttu-id="010a0-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="010a0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010a0-133">CommonParameters</span></span>
<span data-ttu-id="010a0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010a0-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010a0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010a0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="010a0-136">INPUTS</span></span>

### <span data-ttu-id="010a0-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="010a0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="010a0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="010a0-138">System.String</span></span>

## <span data-ttu-id="010a0-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="010a0-139">OUTPUTS</span></span>

### <span data-ttu-id="010a0-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="010a0-140">System.Object</span></span>

## <span data-ttu-id="010a0-141">Note</span><span class="sxs-lookup"><span data-stu-id="010a0-141">NOTES</span></span>

## <span data-ttu-id="010a0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="010a0-142">RELATED LINKS</span></span>

[<span data-ttu-id="010a0-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="010a0-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="010a0-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="010a0-146">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="010a0-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

