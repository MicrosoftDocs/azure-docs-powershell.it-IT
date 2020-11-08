---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191629"
---
# <span data-ttu-id="647d2-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="647d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="647d2-102">SYNOPSIS</span></span>
<span data-ttu-id="647d2-103">Sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="647d2-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="647d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="647d2-104">SYNTAX</span></span>

### <span data-ttu-id="647d2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="647d2-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="647d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="647d2-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="647d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="647d2-107">DESCRIPTION</span></span>
<span data-ttu-id="647d2-108">Il cmdlet **Suspend-AzDataFactoryPipeline** sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="647d2-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="647d2-109">Puoi riprendere la pipeline usando il cmdlet Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="647d2-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="647d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="647d2-110">EXAMPLES</span></span>

### <span data-ttu-id="647d2-111">Esempio 1: sospendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="647d2-112">Questo comando sospende la pipeline denominata DPWikiSample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="647d2-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="647d2-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="647d2-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="647d2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="647d2-114">PARAMETERS</span></span>

### <span data-ttu-id="647d2-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="647d2-115">-DataFactory</span></span>
<span data-ttu-id="647d2-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="647d2-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="647d2-117">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="647d2-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647d2-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="647d2-118">-DataFactoryName</span></span>
<span data-ttu-id="647d2-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="647d2-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="647d2-120">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="647d2-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="647d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647d2-121">-DefaultProfile</span></span>
<span data-ttu-id="647d2-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="647d2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="647d2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="647d2-123">-Name</span></span>
<span data-ttu-id="647d2-124">Specifica il nome della pipeline da sospendere.</span><span class="sxs-lookup"><span data-stu-id="647d2-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="647d2-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="647d2-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="647d2-127">Questo cmdlet sospende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="647d2-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="647d2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="647d2-128">-Confirm</span></span>
<span data-ttu-id="647d2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="647d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647d2-130">-WhatIf</span></span>
<span data-ttu-id="647d2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="647d2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="647d2-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647d2-133">CommonParameters</span></span>
<span data-ttu-id="647d2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647d2-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647d2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647d2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="647d2-136">INPUTS</span></span>

### <span data-ttu-id="647d2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="647d2-137">System.String</span></span>

### <span data-ttu-id="647d2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="647d2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="647d2-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="647d2-139">OUTPUTS</span></span>

### <span data-ttu-id="647d2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="647d2-140">System.Boolean</span></span>

## <span data-ttu-id="647d2-141">Note</span><span class="sxs-lookup"><span data-stu-id="647d2-141">NOTES</span></span>
* <span data-ttu-id="647d2-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="647d2-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="647d2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="647d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="647d2-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="647d2-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="647d2-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="647d2-147">Curriculum vitae-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="647d2-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="647d2-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="647d2-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


