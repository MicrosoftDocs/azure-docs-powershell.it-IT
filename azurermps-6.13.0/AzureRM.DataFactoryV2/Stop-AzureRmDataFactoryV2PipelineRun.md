---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: d93cd05122d0a2c321ef4ab6d858f975e84bc9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515399"
---
# <span data-ttu-id="0cb2d-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="0cb2d-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="0cb2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb2d-103">Interrompe l'esecuzione di pieline in una data factory.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cb2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cb2d-104">SYNTAX</span></span>

### <span data-ttu-id="0cb2d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0cb2d-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cb2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0cb2d-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb2d-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0cb2d-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb2d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cb2d-108">DESCRIPTION</span></span>
<span data-ttu-id="0cb2d-109">Il cmdlet **Stop-AzureRmDataFactoryV2PipelineRun** interrompe l'esecuzione di una pipeline in una factory di dati specificata con l'ID esecuzione di pieline.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="0cb2d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cb2d-110">EXAMPLES</span></span>

### <span data-ttu-id="0cb2d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0cb2d-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="0cb2d-112">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nella Factory WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="0cb2d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cb2d-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb2d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0cb2d-114">-DataFactory</span></span>
<span data-ttu-id="0cb2d-115">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-115">The data factory object.</span></span>

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

### <span data-ttu-id="0cb2d-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0cb2d-116">-DataFactoryName</span></span>
<span data-ttu-id="0cb2d-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-117">The data factory name.</span></span>

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

### <span data-ttu-id="0cb2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb2d-118">-DefaultProfile</span></span>
<span data-ttu-id="0cb2d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cb2d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cb2d-120">-InputObject</span></span>
<span data-ttu-id="0cb2d-121">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="0cb2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cb2d-122">-PassThru</span></span>
<span data-ttu-id="0cb2d-123">Se specificato, il cmdlet scrive vero in caso di esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="0cb2d-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="0cb2d-124">-PipelineRunId</span></span>
<span data-ttu-id="0cb2d-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="0cb2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0cb2d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-127">The resource group name.</span></span>

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

### <span data-ttu-id="0cb2d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0cb2d-128">-Confirm</span></span>
<span data-ttu-id="0cb2d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb2d-130">-WhatIf</span></span>
<span data-ttu-id="0cb2d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb2d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb2d-133">CommonParameters</span></span>
<span data-ttu-id="0cb2d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb2d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb2d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cb2d-136">INPUTS</span></span>

### <span data-ttu-id="0cb2d-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="0cb2d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="0cb2d-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0cb2d-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0cb2d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0cb2d-139">System.String</span></span>

### <span data-ttu-id="0cb2d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0cb2d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="0cb2d-141">Parametri: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0cb2d-141">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="0cb2d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cb2d-142">OUTPUTS</span></span>

### <span data-ttu-id="0cb2d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0cb2d-143">System.Boolean</span></span>

## <span data-ttu-id="0cb2d-144">Note</span><span class="sxs-lookup"><span data-stu-id="0cb2d-144">NOTES</span></span>

## <span data-ttu-id="0cb2d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cb2d-145">RELATED LINKS</span></span>
