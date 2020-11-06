---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 36ee24fea327828247336d7f9c983515ced9deb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518308"
---
# <span data-ttu-id="37dda-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="37dda-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="37dda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37dda-102">SYNOPSIS</span></span>
<span data-ttu-id="37dda-103">Rimuove un DataSet dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="37dda-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37dda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37dda-104">SYNTAX</span></span>

### <span data-ttu-id="37dda-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37dda-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dda-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37dda-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dda-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="37dda-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37dda-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37dda-108">DESCRIPTION</span></span>
<span data-ttu-id="37dda-109">Il cmdlet Remove-AzureRmDataFactoryV2Dataset rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="37dda-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="37dda-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37dda-110">EXAMPLES</span></span>

### <span data-ttu-id="37dda-111">Esempio 1: rimuovere un DataSet</span><span class="sxs-lookup"><span data-stu-id="37dda-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="37dda-112">Questo comando rimuove il DataSet denominato DAWikiAggregatedData dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="37dda-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="37dda-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="37dda-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="37dda-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37dda-114">PARAMETERS</span></span>

### <span data-ttu-id="37dda-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37dda-115">-Confirm</span></span>
<span data-ttu-id="37dda-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dda-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="37dda-117">-DataFactoryName</span></span>
<span data-ttu-id="37dda-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="37dda-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="37dda-119">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37dda-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="37dda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37dda-120">-InputObject</span></span>
<span data-ttu-id="37dda-121">Specifica un oggetto DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="37dda-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-122">-Force</span><span class="sxs-lookup"><span data-stu-id="37dda-122">-Force</span></span>
<span data-ttu-id="37dda-123">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="37dda-123">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="37dda-124">-Name</span></span>
<span data-ttu-id="37dda-125">Specifica il nome del DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="37dda-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dda-126">-ResourceGroupName</span></span>
<span data-ttu-id="37dda-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="37dda-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="37dda-128">Questo cmdlet consente di rimuovere un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37dda-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="37dda-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37dda-129">-ResourceId</span></span>
<span data-ttu-id="37dda-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="37dda-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dda-131">-WhatIf</span></span>
<span data-ttu-id="37dda-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37dda-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dda-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dda-133">-DefaultProfile</span></span>
<span data-ttu-id="37dda-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37dda-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37dda-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dda-135">CommonParameters</span></span>
<span data-ttu-id="37dda-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dda-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dda-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dda-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dda-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37dda-138">INPUTS</span></span>

### <span data-ttu-id="37dda-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="37dda-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="37dda-140">System. String</span><span class="sxs-lookup"><span data-stu-id="37dda-140">System.String</span></span>

## <span data-ttu-id="37dda-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37dda-141">OUTPUTS</span></span>

### <span data-ttu-id="37dda-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="37dda-142">System.Object</span></span>

## <span data-ttu-id="37dda-143">Note</span><span class="sxs-lookup"><span data-stu-id="37dda-143">NOTES</span></span>
<span data-ttu-id="37dda-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="37dda-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37dda-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37dda-145">RELATED LINKS</span></span>

[<span data-ttu-id="37dda-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="37dda-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="37dda-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="37dda-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
