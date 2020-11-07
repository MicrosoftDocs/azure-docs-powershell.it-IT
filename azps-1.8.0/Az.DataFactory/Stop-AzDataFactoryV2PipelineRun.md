---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 3d58b378a64eca438340174d6e2085e26ca3868f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684571"
---
# <span data-ttu-id="dbfbe-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="dbfbe-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="dbfbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfbe-103">Interrompe l'esecuzione di pieline in una data factory.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-103">Stops a pieline run in a data factory.</span></span>

## <span data-ttu-id="dbfbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbfbe-104">SYNTAX</span></span>

### <span data-ttu-id="dbfbe-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dbfbe-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbfbe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dbfbe-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfbe-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dbfbe-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbfbe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbfbe-108">DESCRIPTION</span></span>
<span data-ttu-id="dbfbe-109">Il cmdlet **Stop-AzDataFactoryV2PipelineRun** interrompe l'esecuzione di una pipeline in una factory di dati specificata con l'ID esecuzione di pieline.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="dbfbe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbfbe-110">EXAMPLES</span></span>

### <span data-ttu-id="dbfbe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbfbe-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="dbfbe-112">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nella Factory WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="dbfbe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbfbe-113">PARAMETERS</span></span>

### <span data-ttu-id="dbfbe-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dbfbe-114">-DataFactory</span></span>
<span data-ttu-id="dbfbe-115">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-115">The data factory object.</span></span>

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

### <span data-ttu-id="dbfbe-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dbfbe-116">-DataFactoryName</span></span>
<span data-ttu-id="dbfbe-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-117">The data factory name.</span></span>

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

### <span data-ttu-id="dbfbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfbe-118">-DefaultProfile</span></span>
<span data-ttu-id="dbfbe-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfbe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbfbe-120">-InputObject</span></span>
<span data-ttu-id="dbfbe-121">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="dbfbe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbfbe-122">-PassThru</span></span>
<span data-ttu-id="dbfbe-123">Se specificato, il cmdlet scrive vero in caso di esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="dbfbe-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="dbfbe-124">-PipelineRunId</span></span>
<span data-ttu-id="dbfbe-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="dbfbe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbfbe-126">-ResourceGroupName</span></span>
<span data-ttu-id="dbfbe-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-127">The resource group name.</span></span>

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

### <span data-ttu-id="dbfbe-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbfbe-128">-Confirm</span></span>
<span data-ttu-id="dbfbe-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbfbe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbfbe-130">-WhatIf</span></span>
<span data-ttu-id="dbfbe-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbfbe-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbfbe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfbe-133">CommonParameters</span></span>
<span data-ttu-id="dbfbe-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfbe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfbe-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfbe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfbe-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbfbe-136">INPUTS</span></span>

### <span data-ttu-id="dbfbe-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="dbfbe-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="dbfbe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dbfbe-138">System.String</span></span>

### <span data-ttu-id="dbfbe-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dbfbe-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="dbfbe-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbfbe-140">OUTPUTS</span></span>

### <span data-ttu-id="dbfbe-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbfbe-141">System.Boolean</span></span>

## <span data-ttu-id="dbfbe-142">Note</span><span class="sxs-lookup"><span data-stu-id="dbfbe-142">NOTES</span></span>

## <span data-ttu-id="dbfbe-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbfbe-143">RELATED LINKS</span></span>
