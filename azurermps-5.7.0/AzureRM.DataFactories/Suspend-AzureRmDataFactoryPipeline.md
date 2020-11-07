---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 98c8d5778e827b251c5d0c9b919bde9f86e2c41e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685617"
---
# <span data-ttu-id="9c3b1-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="9c3b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3b1-103">Sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c3b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c3b1-104">SYNTAX</span></span>

### <span data-ttu-id="9c3b1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c3b1-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c3b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9c3b1-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c3b1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c3b1-107">DESCRIPTION</span></span>
<span data-ttu-id="9c3b1-108">Il cmdlet **Suspend-AzureRmDataFactoryPipeline** sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="9c3b1-109">Puoi riprendere la pipeline usando il cmdlet Resume-AzureRmDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="9c3b1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c3b1-110">EXAMPLES</span></span>

### <span data-ttu-id="9c3b1-111">Esempio 1: sospendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9c3b1-112">Questo comando sospende la pipeline denominata DPWikiSample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="9c3b1-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="9c3b1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c3b1-114">PARAMETERS</span></span>

### <span data-ttu-id="9c3b1-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9c3b1-115">-DataFactory</span></span>
<span data-ttu-id="9c3b1-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9c3b1-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9c3b1-117">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3b1-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9c3b1-118">-DataFactoryName</span></span>
<span data-ttu-id="9c3b1-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9c3b1-120">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c3b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3b1-121">-DefaultProfile</span></span>
<span data-ttu-id="9c3b1-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9c3b1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3b1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c3b1-123">-Name</span></span>
<span data-ttu-id="9c3b1-124">Specifica il nome della pipeline da sospendere.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c3b1-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9c3b1-127">Questo cmdlet sospende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c3b1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c3b1-128">-Confirm</span></span>
<span data-ttu-id="9c3b1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c3b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c3b1-130">-WhatIf</span></span>
<span data-ttu-id="9c3b1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c3b1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c3b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3b1-133">CommonParameters</span></span>
<span data-ttu-id="9c3b1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3b1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3b1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3b1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c3b1-136">INPUTS</span></span>

### <span data-ttu-id="9c3b1-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9c3b1-137">None</span></span>
<span data-ttu-id="9c3b1-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9c3b1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c3b1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c3b1-139">OUTPUTS</span></span>

### <span data-ttu-id="9c3b1-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c3b1-140">System.Boolean</span></span>

## <span data-ttu-id="9c3b1-141">Note</span><span class="sxs-lookup"><span data-stu-id="9c3b1-141">NOTES</span></span>
* <span data-ttu-id="9c3b1-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="9c3b1-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9c3b1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c3b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="9c3b1-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9c3b1-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9c3b1-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9c3b1-147">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9c3b1-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9c3b1-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9c3b1-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


