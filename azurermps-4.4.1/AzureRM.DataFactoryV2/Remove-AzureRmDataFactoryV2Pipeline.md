---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522155"
---
# <span data-ttu-id="b4a14-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b4a14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4a14-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a14-103">Rimuove una pipeline dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="b4a14-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4a14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4a14-104">SYNTAX</span></span>

### <span data-ttu-id="b4a14-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4a14-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b4a14-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4a14-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b4a14-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4a14-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b4a14-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4a14-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a14-109">Il cmdlet Remove-AzureRmDataFactoryV2Pipeline consente di rimuovere una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b4a14-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="b4a14-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4a14-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a14-111">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b4a14-112">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b4a14-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="b4a14-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="b4a14-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b4a14-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4a14-114">PARAMETERS</span></span>

### <span data-ttu-id="b4a14-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4a14-115">-Confirm</span></span>
<span data-ttu-id="b4a14-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a14-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a14-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b4a14-117">-DataFactoryName</span></span>
<span data-ttu-id="b4a14-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="b4a14-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b4a14-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b4a14-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4a14-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b4a14-120">-Force</span></span>
<span data-ttu-id="b4a14-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b4a14-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b4a14-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4a14-122">-Name</span></span>
<span data-ttu-id="b4a14-123">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b4a14-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a14-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a14-124">-InputObject</span></span>
<span data-ttu-id="b4a14-125">Specifica un oggetto pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4a14-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="b4a14-126">Questo cmdlet consente di rimuovere la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b4a14-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a14-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a14-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4a14-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a14-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b4a14-129">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b4a14-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4a14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4a14-130">-ResourceId</span></span>
<span data-ttu-id="b4a14-131">ID risorsa Azure della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b4a14-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a14-132">-WhatIf</span></span>
<span data-ttu-id="b4a14-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4a14-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="b4a14-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4a14-134">INPUTS</span></span>

### <span data-ttu-id="b4a14-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="b4a14-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4a14-136">System.String</span></span>


## <span data-ttu-id="b4a14-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4a14-137">OUTPUTS</span></span>

### <span data-ttu-id="b4a14-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="b4a14-138">System.Object</span></span>

## <span data-ttu-id="b4a14-139">Note</span><span class="sxs-lookup"><span data-stu-id="b4a14-139">NOTES</span></span>
<span data-ttu-id="b4a14-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="b4a14-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b4a14-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4a14-141">RELATED LINKS</span></span>
[<span data-ttu-id="b4a14-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b4a14-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b4a14-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b4a14-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

