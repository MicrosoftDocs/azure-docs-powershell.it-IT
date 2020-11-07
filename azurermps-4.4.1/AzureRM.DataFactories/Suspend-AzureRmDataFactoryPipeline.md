---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 52163f9f99a82934ab354f42a49ca77d1c82d7a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686340"
---
# <span data-ttu-id="02f00-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="02f00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02f00-102">SYNOPSIS</span></span>
<span data-ttu-id="02f00-103">Sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="02f00-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02f00-104">SYNTAX</span></span>

### <span data-ttu-id="02f00-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02f00-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="02f00-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f00-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02f00-107">DESCRIPTION</span></span>
<span data-ttu-id="02f00-108">Il cmdlet **Suspend-AzureRmDataFactoryPipeline** sospende una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="02f00-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="02f00-109">Puoi riprendere la pipeline usando il cmdlet Resume-AzureRmDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="02f00-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="02f00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02f00-110">EXAMPLES</span></span>

### <span data-ttu-id="02f00-111">Esempio 1: sospendere una pipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="02f00-112">Questo comando sospende la pipeline denominata DPWikiSample nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="02f00-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="02f00-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="02f00-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="02f00-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02f00-114">PARAMETERS</span></span>

### <span data-ttu-id="02f00-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="02f00-115">-DataFactory</span></span>
<span data-ttu-id="02f00-116">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="02f00-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="02f00-117">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="02f00-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02f00-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="02f00-118">-DataFactoryName</span></span>
<span data-ttu-id="02f00-119">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="02f00-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="02f00-120">Questo cmdlet sospende una pipeline che appartiene alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="02f00-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02f00-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="02f00-121">-Name</span></span>
<span data-ttu-id="02f00-122">Specifica il nome della pipeline da sospendere.</span><span class="sxs-lookup"><span data-stu-id="02f00-122">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="02f00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f00-123">-ResourceGroupName</span></span>
<span data-ttu-id="02f00-124">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="02f00-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="02f00-125">Questo cmdlet sospende una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="02f00-125">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="02f00-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02f00-126">-Confirm</span></span>
<span data-ttu-id="02f00-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f00-128">-WhatIf</span></span>
<span data-ttu-id="02f00-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f00-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f00-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f00-131">-DefaultProfile</span></span>
<span data-ttu-id="02f00-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02f00-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f00-133">CommonParameters</span></span>
<span data-ttu-id="02f00-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f00-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f00-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f00-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02f00-136">INPUTS</span></span>

## <span data-ttu-id="02f00-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02f00-137">OUTPUTS</span></span>

### <span data-ttu-id="02f00-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02f00-138">System.Boolean</span></span>

## <span data-ttu-id="02f00-139">Note</span><span class="sxs-lookup"><span data-stu-id="02f00-139">NOTES</span></span>
* <span data-ttu-id="02f00-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="02f00-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="02f00-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02f00-141">RELATED LINKS</span></span>

[<span data-ttu-id="02f00-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="02f00-143">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="02f00-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="02f00-145">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="02f00-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="02f00-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="02f00-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


