---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520537"
---
# <span data-ttu-id="45683-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="45683-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="45683-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45683-102">SYNOPSIS</span></span>
<span data-ttu-id="45683-103">Rimuove un DataSet dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="45683-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45683-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45683-104">SYNTAX</span></span>

### <span data-ttu-id="45683-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45683-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45683-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="45683-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45683-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45683-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="45683-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45683-108">DESCRIPTION</span></span>
<span data-ttu-id="45683-109">Il cmdlet Remove-AzureRmDataFactoryV2Dataset rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="45683-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="45683-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45683-110">EXAMPLES</span></span>

### <span data-ttu-id="45683-111">Esempio 1: rimuovere un DataSet</span><span class="sxs-lookup"><span data-stu-id="45683-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="45683-112">Questo comando rimuove il DataSet denominato DAWikiAggregatedData dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="45683-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="45683-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="45683-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="45683-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45683-114">PARAMETERS</span></span>

### <span data-ttu-id="45683-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45683-115">-Confirm</span></span>
<span data-ttu-id="45683-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45683-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45683-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="45683-117">-DataFactoryName</span></span>
<span data-ttu-id="45683-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="45683-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="45683-119">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="45683-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="45683-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45683-120">-InputObject</span></span>
<span data-ttu-id="45683-121">Specifica un oggetto DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="45683-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45683-122">-Force</span><span class="sxs-lookup"><span data-stu-id="45683-122">-Force</span></span>
<span data-ttu-id="45683-123">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="45683-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="45683-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="45683-124">-Name</span></span>
<span data-ttu-id="45683-125">Specifica il nome del DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="45683-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45683-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45683-126">-ResourceGroupName</span></span>
<span data-ttu-id="45683-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="45683-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="45683-128">Questo cmdlet consente di rimuovere un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="45683-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="45683-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45683-129">-ResourceId</span></span>
<span data-ttu-id="45683-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="45683-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="45683-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45683-131">-WhatIf</span></span>
<span data-ttu-id="45683-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45683-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="45683-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45683-133">INPUTS</span></span>

### <span data-ttu-id="45683-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="45683-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="45683-135">System. String</span><span class="sxs-lookup"><span data-stu-id="45683-135">System.String</span></span>


## <span data-ttu-id="45683-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45683-136">OUTPUTS</span></span>

### <span data-ttu-id="45683-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="45683-137">System.Object</span></span>

## <span data-ttu-id="45683-138">Note</span><span class="sxs-lookup"><span data-stu-id="45683-138">NOTES</span></span>
<span data-ttu-id="45683-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="45683-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="45683-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45683-140">RELATED LINKS</span></span>
[<span data-ttu-id="45683-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="45683-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="45683-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="45683-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
