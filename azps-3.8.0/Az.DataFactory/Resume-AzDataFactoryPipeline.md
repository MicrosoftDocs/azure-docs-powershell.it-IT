---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 26b0073cafebbd3e24afae5e8265b4acc9f4b0a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865259"
---
# <span data-ttu-id="0eb03-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="0eb03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0eb03-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb03-103">Riprende una pipeline sospesa in data factory.</span><span class="sxs-lookup"><span data-stu-id="0eb03-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="0eb03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eb03-104">SYNTAX</span></span>

### <span data-ttu-id="0eb03-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0eb03-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb03-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0eb03-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb03-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb03-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb03-108">Il cmdlet **Resume-AzDataFactoryPipeline** riprende una pipeline sospesa in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0eb03-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="0eb03-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eb03-109">EXAMPLES</span></span>

### <span data-ttu-id="0eb03-110">Esempio 1: riprendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="0eb03-111">Questo comando riprende la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0eb03-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="0eb03-112">Usa il cmdlet **Suspend-AzDataFactoryPipeline** per sospendere una pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eb03-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="0eb03-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="0eb03-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="0eb03-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0eb03-114">PARAMETERS</span></span>

### <span data-ttu-id="0eb03-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0eb03-115">-DataFactory</span></span>
<span data-ttu-id="0eb03-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="0eb03-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0eb03-117">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0eb03-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0eb03-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0eb03-118">-DataFactoryName</span></span>
<span data-ttu-id="0eb03-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="0eb03-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0eb03-120">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0eb03-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0eb03-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb03-121">-DefaultProfile</span></span>
<span data-ttu-id="0eb03-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0eb03-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eb03-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0eb03-123">-Name</span></span>
<span data-ttu-id="0eb03-124">Specifica il nome della pipeline da riprendere.</span><span class="sxs-lookup"><span data-stu-id="0eb03-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="0eb03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb03-125">-ResourceGroupName</span></span>
<span data-ttu-id="0eb03-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb03-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0eb03-127">Questo cmdlet riprende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0eb03-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0eb03-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0eb03-128">-Confirm</span></span>
<span data-ttu-id="0eb03-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb03-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb03-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb03-130">-WhatIf</span></span>
<span data-ttu-id="0eb03-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb03-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb03-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0eb03-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb03-133">CommonParameters</span></span>
<span data-ttu-id="0eb03-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb03-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb03-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb03-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0eb03-136">INPUTS</span></span>

### <span data-ttu-id="0eb03-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb03-137">System.String</span></span>

### <span data-ttu-id="0eb03-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0eb03-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0eb03-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eb03-139">OUTPUTS</span></span>

### <span data-ttu-id="0eb03-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0eb03-140">System.Boolean</span></span>

## <span data-ttu-id="0eb03-141">Note</span><span class="sxs-lookup"><span data-stu-id="0eb03-141">NOTES</span></span>
* <span data-ttu-id="0eb03-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="0eb03-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0eb03-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eb03-143">RELATED LINKS</span></span>

[<span data-ttu-id="0eb03-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0eb03-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="0eb03-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="0eb03-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0eb03-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="0eb03-148">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0eb03-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


