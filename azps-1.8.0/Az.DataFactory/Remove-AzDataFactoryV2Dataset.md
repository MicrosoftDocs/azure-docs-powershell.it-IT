---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 8d1a4dfcaaa101a87fc687e78b8086823be7caab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684590"
---
# <span data-ttu-id="b88f8-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b88f8-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="b88f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b88f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b88f8-103">Rimuove un DataSet dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="b88f8-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="b88f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b88f8-104">SYNTAX</span></span>

### <span data-ttu-id="b88f8-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b88f8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b88f8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b88f8-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b88f8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b88f8-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b88f8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b88f8-108">DESCRIPTION</span></span>
<span data-ttu-id="b88f8-109">Il cmdlet Remove-AzDataFactoryV2Dataset rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b88f8-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="b88f8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b88f8-110">EXAMPLES</span></span>

### <span data-ttu-id="b88f8-111">Esempio 1: rimuovere un DataSet</span><span class="sxs-lookup"><span data-stu-id="b88f8-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="b88f8-112">Questo comando rimuove il DataSet denominato DAWikiAggregatedData dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b88f8-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="b88f8-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="b88f8-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b88f8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b88f8-114">PARAMETERS</span></span>

### <span data-ttu-id="b88f8-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b88f8-115">-DataFactoryName</span></span>
<span data-ttu-id="b88f8-116">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="b88f8-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b88f8-117">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b88f8-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b88f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88f8-118">-DefaultProfile</span></span>
<span data-ttu-id="b88f8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b88f8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b88f8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b88f8-120">-Force</span></span>
<span data-ttu-id="b88f8-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b88f8-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b88f8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b88f8-122">-InputObject</span></span>
<span data-ttu-id="b88f8-123">Specifica un oggetto DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b88f8-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="b88f8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b88f8-124">-Name</span></span>
<span data-ttu-id="b88f8-125">Specifica il nome del DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b88f8-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="b88f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="b88f8-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b88f8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b88f8-128">Questo cmdlet consente di rimuovere un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b88f8-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b88f8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b88f8-129">-ResourceId</span></span>
<span data-ttu-id="b88f8-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="b88f8-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b88f8-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b88f8-131">-Confirm</span></span>
<span data-ttu-id="b88f8-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b88f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b88f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b88f8-133">-WhatIf</span></span>
<span data-ttu-id="b88f8-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b88f8-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b88f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88f8-135">CommonParameters</span></span>
<span data-ttu-id="b88f8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88f8-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b88f8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88f8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b88f8-138">INPUTS</span></span>

### <span data-ttu-id="b88f8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="b88f8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="b88f8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b88f8-140">System.String</span></span>

## <span data-ttu-id="b88f8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b88f8-141">OUTPUTS</span></span>

### <span data-ttu-id="b88f8-142">System. void</span><span class="sxs-lookup"><span data-stu-id="b88f8-142">System.Void</span></span>

## <span data-ttu-id="b88f8-143">Note</span><span class="sxs-lookup"><span data-stu-id="b88f8-143">NOTES</span></span>
<span data-ttu-id="b88f8-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="b88f8-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b88f8-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b88f8-145">RELATED LINKS</span></span>

[<span data-ttu-id="b88f8-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b88f8-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="b88f8-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b88f8-147">Set-AzDataFactoryV2Dataset</span></span>]()
