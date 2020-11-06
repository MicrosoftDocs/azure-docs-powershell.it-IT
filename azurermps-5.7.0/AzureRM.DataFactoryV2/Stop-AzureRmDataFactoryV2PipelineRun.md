---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514436"
---
# <span data-ttu-id="743bf-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="743bf-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="743bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="743bf-102">SYNOPSIS</span></span>
<span data-ttu-id="743bf-103">Interrompe l'esecuzione di pieline in una data factory.</span><span class="sxs-lookup"><span data-stu-id="743bf-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="743bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="743bf-104">SYNTAX</span></span>

### <span data-ttu-id="743bf-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="743bf-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="743bf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="743bf-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="743bf-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="743bf-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="743bf-108">DESCRIPTION</span></span>
<span data-ttu-id="743bf-109">Il cmdlet **Stop-AzureRmDataFactoryV2PipelineRun** interrompe l'esecuzione di una pipeline in una factory di dati specificata con l'ID esecuzione di pieline.</span><span class="sxs-lookup"><span data-stu-id="743bf-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="743bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="743bf-110">EXAMPLES</span></span>

### <span data-ttu-id="743bf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="743bf-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="743bf-112">Questo comando interrompe l'esecuzione della pipeline con ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd nella Factory WikiADF.</span><span class="sxs-lookup"><span data-stu-id="743bf-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="743bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="743bf-113">PARAMETERS</span></span>

### <span data-ttu-id="743bf-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="743bf-114">-DataFactory</span></span>
<span data-ttu-id="743bf-115">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="743bf-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="743bf-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="743bf-116">-DataFactoryName</span></span>
<span data-ttu-id="743bf-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="743bf-117">The data factory name.</span></span>

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

### <span data-ttu-id="743bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743bf-118">-DefaultProfile</span></span>
<span data-ttu-id="743bf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="743bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="743bf-120">-InputObject</span></span>
<span data-ttu-id="743bf-121">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="743bf-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="743bf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="743bf-122">-PassThru</span></span>
<span data-ttu-id="743bf-123">Se specificato, il cmdlet scrive vero in caso di esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="743bf-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="743bf-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="743bf-124">-PipelineRunId</span></span>
<span data-ttu-id="743bf-125">ID esecuzione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="743bf-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="743bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="743bf-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="743bf-127">The resource group name.</span></span>

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

### <span data-ttu-id="743bf-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="743bf-128">-Confirm</span></span>
<span data-ttu-id="743bf-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="743bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743bf-130">-WhatIf</span></span>
<span data-ttu-id="743bf-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="743bf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743bf-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="743bf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743bf-133">CommonParameters</span></span>
<span data-ttu-id="743bf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743bf-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743bf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="743bf-136">INPUTS</span></span>

### <span data-ttu-id="743bf-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="743bf-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="743bf-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="743bf-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="743bf-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="743bf-139">OUTPUTS</span></span>

### <span data-ttu-id="743bf-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="743bf-140">System.Boolean</span></span>

## <span data-ttu-id="743bf-141">Note</span><span class="sxs-lookup"><span data-stu-id="743bf-141">NOTES</span></span>

## <span data-ttu-id="743bf-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="743bf-142">RELATED LINKS</span></span>

