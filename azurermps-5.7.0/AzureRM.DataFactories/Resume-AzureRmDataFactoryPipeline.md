---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 5cf769a02b6a02f0fba9b26df48554d80a406140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509931"
---
# <span data-ttu-id="4bcb9-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="4bcb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcb9-103">Riprende una pipeline sospesa in data factory.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bcb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bcb9-104">SYNTAX</span></span>

### <span data-ttu-id="4bcb9-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bcb9-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bcb9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4bcb9-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcb9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bcb9-107">DESCRIPTION</span></span>
<span data-ttu-id="4bcb9-108">Il cmdlet **Resume-AzureRmDataFactoryPipeline** riprende una pipeline sospesa in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="4bcb9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bcb9-109">EXAMPLES</span></span>

### <span data-ttu-id="4bcb9-110">Esempio 1: riprendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4bcb9-111">Questo comando riprende la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="4bcb9-112">Usa il cmdlet **Suspend-AzureRmDataFactoryPipeline** per sospendere una pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="4bcb9-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="4bcb9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bcb9-114">PARAMETERS</span></span>

### <span data-ttu-id="4bcb9-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bcb9-115">-DataFactory</span></span>
<span data-ttu-id="4bcb9-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4bcb9-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4bcb9-117">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bcb9-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4bcb9-118">-DataFactoryName</span></span>
<span data-ttu-id="4bcb9-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4bcb9-120">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bcb9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb9-121">-DefaultProfile</span></span>
<span data-ttu-id="4bcb9-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4bcb9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bcb9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bcb9-123">-Name</span></span>
<span data-ttu-id="4bcb9-124">Specifica il nome della pipeline da riprendere.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="4bcb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bcb9-126">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4bcb9-127">Questo cmdlet riprende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bcb9-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4bcb9-128">-Confirm</span></span>
<span data-ttu-id="4bcb9-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcb9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcb9-130">-WhatIf</span></span>
<span data-ttu-id="4bcb9-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcb9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcb9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcb9-133">CommonParameters</span></span>
<span data-ttu-id="4bcb9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcb9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcb9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcb9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bcb9-136">INPUTS</span></span>

### <span data-ttu-id="4bcb9-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4bcb9-137">None</span></span>
<span data-ttu-id="4bcb9-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4bcb9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bcb9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bcb9-139">OUTPUTS</span></span>

### <span data-ttu-id="4bcb9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4bcb9-140">System.Boolean</span></span>

## <span data-ttu-id="4bcb9-141">Note</span><span class="sxs-lookup"><span data-stu-id="4bcb9-141">NOTES</span></span>
* <span data-ttu-id="4bcb9-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="4bcb9-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4bcb9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bcb9-143">RELATED LINKS</span></span>

[<span data-ttu-id="4bcb9-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4bcb9-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4bcb9-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="4bcb9-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4bcb9-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="4bcb9-148">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4bcb9-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


