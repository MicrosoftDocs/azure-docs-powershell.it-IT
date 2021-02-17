---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198831"
---
# <span data-ttu-id="5021d-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5021d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5021d-102">SYNOPSIS</span></span>
<span data-ttu-id="5021d-103">Rimuove un trigger da un data factory.</span><span class="sxs-lookup"><span data-stu-id="5021d-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="5021d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5021d-104">SYNTAX</span></span>

### <span data-ttu-id="5021d-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5021d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5021d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5021d-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5021d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5021d-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5021d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5021d-108">DESCRIPTION</span></span>
<span data-ttu-id="5021d-109">Il cmdlet **Remove-AzDataFactoryV2Trigger** rimuove un trigger da un data factory.</span><span class="sxs-lookup"><span data-stu-id="5021d-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="5021d-110">Se si _specifica il_ parametro Force, il cmdlet non richiede conferma prima di rimuovere il trigger.</span><span class="sxs-lookup"><span data-stu-id="5021d-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="5021d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5021d-111">EXAMPLES</span></span>

### <span data-ttu-id="5021d-112">Esempio 1: Rimuovere un trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5021d-113">Rimuovere un trigger denominato "ScheduledTrigger" dal data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5021d-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="5021d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5021d-114">PARAMETERS</span></span>

### <span data-ttu-id="5021d-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5021d-115">-DataFactoryName</span></span>
<span data-ttu-id="5021d-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="5021d-116">The data factory name.</span></span>

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

### <span data-ttu-id="5021d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5021d-117">-DefaultProfile</span></span>
<span data-ttu-id="5021d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5021d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5021d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5021d-119">-Force</span></span>
<span data-ttu-id="5021d-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5021d-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5021d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5021d-121">-InputObject</span></span>
<span data-ttu-id="5021d-122">Oggetto Trigger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5021d-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="5021d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5021d-123">-Name</span></span>
<span data-ttu-id="5021d-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="5021d-124">The trigger name.</span></span>

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

### <span data-ttu-id="5021d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5021d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5021d-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5021d-126">The resource group name.</span></span>

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

### <span data-ttu-id="5021d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5021d-127">-ResourceId</span></span>
<span data-ttu-id="5021d-128">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="5021d-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5021d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5021d-129">-Confirm</span></span>
<span data-ttu-id="5021d-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5021d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5021d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5021d-131">-WhatIf</span></span>
<span data-ttu-id="5021d-132">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="5021d-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5021d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5021d-133">CommonParameters</span></span>
<span data-ttu-id="5021d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5021d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5021d-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5021d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5021d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="5021d-136">INPUTS</span></span>

### <span data-ttu-id="5021d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5021d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="5021d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5021d-138">System.String</span></span>

## <span data-ttu-id="5021d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5021d-139">OUTPUTS</span></span>

### <span data-ttu-id="5021d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5021d-140">System.Boolean</span></span>

## <span data-ttu-id="5021d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="5021d-141">NOTES</span></span>

## <span data-ttu-id="5021d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5021d-142">RELATED LINKS</span></span>

[<span data-ttu-id="5021d-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5021d-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5021d-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5021d-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5021d-146">Stop-AzDataFactoryV2Trigger</span></span>]()

