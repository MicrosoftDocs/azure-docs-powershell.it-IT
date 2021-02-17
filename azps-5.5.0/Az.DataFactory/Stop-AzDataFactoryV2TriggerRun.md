---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194815"
---
# <span data-ttu-id="25a94-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="25a94-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="25a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a94-102">SYNOPSIS</span></span>
<span data-ttu-id="25a94-103">Interrompe l'esecuzione di un trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="25a94-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="25a94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25a94-104">SYNTAX</span></span>

### <span data-ttu-id="25a94-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="25a94-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a94-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25a94-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a94-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="25a94-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25a94-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25a94-108">DESCRIPTION</span></span>
<span data-ttu-id="25a94-109">Il cmdlet **Stop-AzDataFactoryV2TriggerRun** interrompe l'esecuzione di un trigger in un data factory specificato con il nome del trigger e l'ID di esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="25a94-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="25a94-110">Attualmente supportato solo per TumblingWindowTriggers in WaitingOnUsingy State.</span><span class="sxs-lookup"><span data-stu-id="25a94-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="25a94-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25a94-111">EXAMPLES</span></span>

### <span data-ttu-id="25a94-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25a94-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="25a94-113">Questo comando interrompe l'esecuzione del trigger con ID '0858600246800588497807248799CU16' nel produttore WikiADF.</span><span class="sxs-lookup"><span data-stu-id="25a94-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="25a94-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25a94-114">PARAMETERS</span></span>

### <span data-ttu-id="25a94-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="25a94-115">-DataFactory</span></span>
<span data-ttu-id="25a94-116">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="25a94-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a94-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="25a94-117">-DataFactoryName</span></span>
<span data-ttu-id="25a94-118">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="25a94-118">The data factory name.</span></span>

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

### <span data-ttu-id="25a94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a94-119">-DefaultProfile</span></span>
<span data-ttu-id="25a94-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25a94-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a94-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25a94-121">-InputObject</span></span>
<span data-ttu-id="25a94-122">Informazioni sul trigger eseguito.</span><span class="sxs-lookup"><span data-stu-id="25a94-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a94-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25a94-123">-PassThru</span></span>
<span data-ttu-id="25a94-124">Se è stato specificato il cmdlet write true nel caso l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="25a94-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="25a94-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a94-125">-ResourceGroupName</span></span>
<span data-ttu-id="25a94-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25a94-126">The resource group name.</span></span>

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

### <span data-ttu-id="25a94-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="25a94-127">-TriggerName</span></span>
<span data-ttu-id="25a94-128">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="25a94-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a94-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="25a94-129">-TriggerRunId</span></span>
<span data-ttu-id="25a94-130">ID esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="25a94-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a94-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25a94-131">-Confirm</span></span>
<span data-ttu-id="25a94-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25a94-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a94-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a94-133">-WhatIf</span></span>
<span data-ttu-id="25a94-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25a94-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25a94-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25a94-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a94-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a94-136">CommonParameters</span></span>
<span data-ttu-id="25a94-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a94-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a94-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25a94-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a94-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="25a94-139">INPUTS</span></span>

### <span data-ttu-id="25a94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="25a94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="25a94-141">System.String</span><span class="sxs-lookup"><span data-stu-id="25a94-141">System.String</span></span>

### <span data-ttu-id="25a94-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="25a94-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="25a94-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25a94-143">OUTPUTS</span></span>

### <span data-ttu-id="25a94-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25a94-144">System.Boolean</span></span>

## <span data-ttu-id="25a94-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="25a94-145">NOTES</span></span>

## <span data-ttu-id="25a94-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25a94-146">RELATED LINKS</span></span>
