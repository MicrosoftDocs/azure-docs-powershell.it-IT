---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298189"
---
# <span data-ttu-id="48020-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="48020-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="48020-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48020-102">SYNOPSIS</span></span>
<span data-ttu-id="48020-103">Interrompe l'esecuzione di una pipeline in una data factory.</span><span class="sxs-lookup"><span data-stu-id="48020-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="48020-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48020-104">SYNTAX</span></span>

### <span data-ttu-id="48020-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48020-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48020-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48020-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48020-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="48020-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48020-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48020-108">DESCRIPTION</span></span>
<span data-ttu-id="48020-109">Il cmdlet **Stop-AzDataFactoryV2PipelineRun** interrompe l'esecuzione di una pipeline in una factory di dati specificata con l'ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="48020-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="48020-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48020-110">EXAMPLES</span></span>

### <span data-ttu-id="48020-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48020-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="48020-112">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nella Factory WikiADF.</span><span class="sxs-lookup"><span data-stu-id="48020-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="48020-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48020-113">PARAMETERS</span></span>

### <span data-ttu-id="48020-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="48020-114">-DataFactory</span></span>
<span data-ttu-id="48020-115">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="48020-115">The data factory object.</span></span>

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

### <span data-ttu-id="48020-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="48020-116">-DataFactoryName</span></span>
<span data-ttu-id="48020-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="48020-117">The data factory name.</span></span>

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

### <span data-ttu-id="48020-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48020-118">-DefaultProfile</span></span>
<span data-ttu-id="48020-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48020-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48020-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48020-120">-InputObject</span></span>
<span data-ttu-id="48020-121">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="48020-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="48020-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48020-122">-PassThru</span></span>
<span data-ttu-id="48020-123">Se specificato, il cmdlet scrive vero in caso di esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="48020-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="48020-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="48020-124">-PipelineRunId</span></span>
<span data-ttu-id="48020-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="48020-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="48020-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48020-126">-ResourceGroupName</span></span>
<span data-ttu-id="48020-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48020-127">The resource group name.</span></span>

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

### <span data-ttu-id="48020-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48020-128">-Confirm</span></span>
<span data-ttu-id="48020-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48020-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48020-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48020-130">-WhatIf</span></span>
<span data-ttu-id="48020-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48020-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48020-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48020-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48020-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48020-133">CommonParameters</span></span>
<span data-ttu-id="48020-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48020-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48020-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48020-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48020-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48020-136">INPUTS</span></span>

### <span data-ttu-id="48020-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="48020-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="48020-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48020-138">System.String</span></span>

### <span data-ttu-id="48020-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="48020-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="48020-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48020-140">OUTPUTS</span></span>

### <span data-ttu-id="48020-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48020-141">System.Boolean</span></span>

## <span data-ttu-id="48020-142">Note</span><span class="sxs-lookup"><span data-stu-id="48020-142">NOTES</span></span>

## <span data-ttu-id="48020-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48020-143">RELATED LINKS</span></span>
