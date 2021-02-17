---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208683"
---
# <span data-ttu-id="5cc4b-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="5cc4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc4b-103">Sospende una pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="5cc4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-104">SYNTAX</span></span>

### <span data-ttu-id="5cc4b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5cc4b-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5cc4b-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc4b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5cc4b-107">DESCRIPTION</span></span>
<span data-ttu-id="5cc4b-108">Il cmdlet **Suspend-AzDataFactoryPipeline** sospende una pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="5cc4b-109">È possibile riprendere la pipeline usando il cmdlet Resume-AzDataFactoryPipeline pipeline.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="5cc4b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-110">EXAMPLES</span></span>

### <span data-ttu-id="5cc4b-111">Esempio 1: Sospendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="5cc4b-112">Questo comando sospende la pipeline denominata DPWikiSample nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="5cc4b-113">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="5cc4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cc4b-114">PARAMETERS</span></span>

### <span data-ttu-id="5cc4b-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5cc4b-115">-DataFactory</span></span>
<span data-ttu-id="5cc4b-116">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="5cc4b-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5cc4b-117">Questo cmdlet sospende una pipeline che appartiene al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cc4b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5cc4b-118">-DataFactoryName</span></span>
<span data-ttu-id="5cc4b-119">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5cc4b-120">Questo cmdlet sospende una pipeline che appartiene al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cc4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc4b-121">-DefaultProfile</span></span>
<span data-ttu-id="5cc4b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5cc4b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cc4b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5cc4b-123">-Name</span></span>
<span data-ttu-id="5cc4b-124">Specifica il nome della pipeline da sospendere.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="5cc4b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc4b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5cc4b-126">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5cc4b-127">Questo cmdlet sospende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cc4b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cc4b-128">-Confirm</span></span>
<span data-ttu-id="5cc4b-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc4b-130">-WhatIf</span></span>
<span data-ttu-id="5cc4b-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc4b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc4b-133">CommonParameters</span></span>
<span data-ttu-id="5cc4b-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc4b-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc4b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc4b-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="5cc4b-136">INPUTS</span></span>

### <span data-ttu-id="5cc4b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5cc4b-137">System.String</span></span>

### <span data-ttu-id="5cc4b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5cc4b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5cc4b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cc4b-139">OUTPUTS</span></span>

### <span data-ttu-id="5cc4b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cc4b-140">System.Boolean</span></span>

## <span data-ttu-id="5cc4b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="5cc4b-141">NOTES</span></span>
* <span data-ttu-id="5cc4b-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="5cc4b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5cc4b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-143">RELATED LINKS</span></span>

[<span data-ttu-id="5cc4b-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cc4b-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cc4b-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cc4b-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cc4b-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cc4b-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="5cc4b-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


