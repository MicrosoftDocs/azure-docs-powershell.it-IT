---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204410"
---
# <span data-ttu-id="a6d1d-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a6d1d-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="a6d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d1d-103">Interrompe l'esecuzione di una pipeline in un data factory.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="a6d1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6d1d-104">SYNTAX</span></span>

### <span data-ttu-id="a6d1d-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a6d1d-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6d1d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6d1d-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6d1d-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a6d1d-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d1d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="a6d1d-109">Il cmdlet **Stop-AzDataFactoryV2PipelineRun** interrompe l'esecuzione di una pipeline in una data factory specificata con l'ID di esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="a6d1d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6d1d-110">EXAMPLES</span></span>

### <span data-ttu-id="a6d1d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6d1d-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="a6d1d-112">Questo comando interrompe l'esecuzione della pipeline con id b9730a13-aa12-4926-a8b3-8e3a974ab0bd nella fabbrica WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="a6d1d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6d1d-113">PARAMETERS</span></span>

### <span data-ttu-id="a6d1d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6d1d-114">-DataFactory</span></span>
<span data-ttu-id="a6d1d-115">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-115">The data factory object.</span></span>

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

### <span data-ttu-id="a6d1d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a6d1d-116">-DataFactoryName</span></span>
<span data-ttu-id="a6d1d-117">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-117">The data factory name.</span></span>

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

### <span data-ttu-id="a6d1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d1d-118">-DefaultProfile</span></span>
<span data-ttu-id="a6d1d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d1d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6d1d-120">-InputObject</span></span>
<span data-ttu-id="a6d1d-121">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d1d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6d1d-122">-PassThru</span></span>
<span data-ttu-id="a6d1d-123">Se è stato specificato il cmdlet write true nel caso l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="a6d1d-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a6d1d-124">-PipelineRunId</span></span>
<span data-ttu-id="a6d1d-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="a6d1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6d1d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-127">The resource group name.</span></span>

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

### <span data-ttu-id="a6d1d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6d1d-128">-Confirm</span></span>
<span data-ttu-id="a6d1d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d1d-130">-WhatIf</span></span>
<span data-ttu-id="a6d1d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d1d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d1d-133">CommonParameters</span></span>
<span data-ttu-id="a6d1d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d1d-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d1d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d1d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6d1d-136">INPUTS</span></span>

### <span data-ttu-id="a6d1d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a6d1d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="a6d1d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a6d1d-138">System.String</span></span>

### <span data-ttu-id="a6d1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6d1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a6d1d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6d1d-140">OUTPUTS</span></span>

### <span data-ttu-id="a6d1d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6d1d-141">System.Boolean</span></span>

## <span data-ttu-id="a6d1d-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6d1d-142">NOTES</span></span>

## <span data-ttu-id="a6d1d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6d1d-143">RELATED LINKS</span></span>
