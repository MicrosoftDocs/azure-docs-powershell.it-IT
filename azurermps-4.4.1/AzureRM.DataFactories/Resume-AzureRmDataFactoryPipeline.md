---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510704"
---
# <span data-ttu-id="186d3-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="186d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="186d3-102">SYNOPSIS</span></span>
<span data-ttu-id="186d3-103">Riprende una pipeline sospesa in data factory.</span><span class="sxs-lookup"><span data-stu-id="186d3-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="186d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="186d3-104">SYNTAX</span></span>

### <span data-ttu-id="186d3-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="186d3-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186d3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="186d3-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="186d3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="186d3-107">DESCRIPTION</span></span>
<span data-ttu-id="186d3-108">Il cmdlet **Resume-AzureRmDataFactoryPipeline** riprende una pipeline sospesa in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="186d3-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="186d3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="186d3-109">EXAMPLES</span></span>

### <span data-ttu-id="186d3-110">Esempio 1: riprendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="186d3-111">Questo comando riprende la pipeline denominata DPWikisample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="186d3-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="186d3-112">Usa il cmdlet **Suspend-AzureRmDataFactoryPipeline** per sospendere una pipeline.</span><span class="sxs-lookup"><span data-stu-id="186d3-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="186d3-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="186d3-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="186d3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="186d3-114">PARAMETERS</span></span>

### <span data-ttu-id="186d3-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="186d3-115">-DataFactory</span></span>
<span data-ttu-id="186d3-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="186d3-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="186d3-117">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="186d3-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="186d3-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="186d3-118">-DataFactoryName</span></span>
<span data-ttu-id="186d3-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="186d3-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="186d3-120">Questo cmdlet riprende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="186d3-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="186d3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="186d3-121">-Name</span></span>
<span data-ttu-id="186d3-122">Specifica il nome della pipeline da riprendere.</span><span class="sxs-lookup"><span data-stu-id="186d3-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="186d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="186d3-124">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="186d3-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="186d3-125">Questo cmdlet riprende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="186d3-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="186d3-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="186d3-126">-Confirm</span></span>
<span data-ttu-id="186d3-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="186d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="186d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186d3-128">-WhatIf</span></span>
<span data-ttu-id="186d3-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="186d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186d3-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="186d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="186d3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186d3-131">-DefaultProfile</span></span>
<span data-ttu-id="186d3-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="186d3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="186d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186d3-133">CommonParameters</span></span>
<span data-ttu-id="186d3-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186d3-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="186d3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186d3-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="186d3-136">INPUTS</span></span>

## <span data-ttu-id="186d3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="186d3-137">OUTPUTS</span></span>

### <span data-ttu-id="186d3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="186d3-138">System.Boolean</span></span>

## <span data-ttu-id="186d3-139">Note</span><span class="sxs-lookup"><span data-stu-id="186d3-139">NOTES</span></span>
* <span data-ttu-id="186d3-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="186d3-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="186d3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="186d3-141">RELATED LINKS</span></span>

[<span data-ttu-id="186d3-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="186d3-143">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="186d3-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="186d3-145">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="186d3-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="186d3-146">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="186d3-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


