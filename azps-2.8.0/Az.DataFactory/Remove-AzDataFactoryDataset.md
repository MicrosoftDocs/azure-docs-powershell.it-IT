---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674970"
---
# <span data-ttu-id="dd80d-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="dd80d-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="dd80d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd80d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd80d-103">Rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd80d-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="dd80d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd80d-104">SYNTAX</span></span>

### <span data-ttu-id="dd80d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd80d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd80d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dd80d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd80d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd80d-107">DESCRIPTION</span></span>
<span data-ttu-id="dd80d-108">Il cmdlet **Remove-AzDataFactoryDataset** rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd80d-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="dd80d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd80d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd80d-110">Esempio 1: rimuovere un DataSet</span><span class="sxs-lookup"><span data-stu-id="dd80d-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="dd80d-111">Questo comando rimuove il DataSet denominato DAWikiAggregatedData dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dd80d-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="dd80d-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="dd80d-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="dd80d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd80d-113">PARAMETERS</span></span>

### <span data-ttu-id="dd80d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd80d-114">-DataFactory</span></span>
<span data-ttu-id="dd80d-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="dd80d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dd80d-116">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd80d-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd80d-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dd80d-117">-DataFactoryName</span></span>
<span data-ttu-id="dd80d-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="dd80d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dd80d-119">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd80d-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd80d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd80d-120">-DefaultProfile</span></span>
<span data-ttu-id="dd80d-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dd80d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd80d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dd80d-122">-Force</span></span>
<span data-ttu-id="dd80d-123">Indica che questo cmdlet rimuove un DataSet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dd80d-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dd80d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd80d-124">-Name</span></span>
<span data-ttu-id="dd80d-125">Specifica il nome del DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd80d-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd80d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd80d-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd80d-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="dd80d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dd80d-128">Questo cmdlet consente di rimuovere un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd80d-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd80d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd80d-129">-Confirm</span></span>
<span data-ttu-id="dd80d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd80d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd80d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd80d-131">-WhatIf</span></span>
<span data-ttu-id="dd80d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd80d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd80d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd80d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd80d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd80d-134">CommonParameters</span></span>
<span data-ttu-id="dd80d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd80d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd80d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd80d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd80d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd80d-137">INPUTS</span></span>

### <span data-ttu-id="dd80d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd80d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="dd80d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd80d-139">System.String</span></span>

## <span data-ttu-id="dd80d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd80d-140">OUTPUTS</span></span>

### <span data-ttu-id="dd80d-141">System. void</span><span class="sxs-lookup"><span data-stu-id="dd80d-141">System.Void</span></span>

## <span data-ttu-id="dd80d-142">Note</span><span class="sxs-lookup"><span data-stu-id="dd80d-142">NOTES</span></span>
* <span data-ttu-id="dd80d-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="dd80d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dd80d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd80d-144">RELATED LINKS</span></span>

[<span data-ttu-id="dd80d-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="dd80d-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="dd80d-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="dd80d-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

