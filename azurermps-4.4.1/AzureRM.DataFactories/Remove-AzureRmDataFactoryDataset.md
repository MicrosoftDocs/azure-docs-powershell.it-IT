---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510708"
---
# <span data-ttu-id="2a35e-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="2a35e-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="2a35e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a35e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a35e-103">Rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2a35e-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a35e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a35e-104">SYNTAX</span></span>

### <span data-ttu-id="2a35e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a35e-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a35e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2a35e-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a35e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a35e-107">DESCRIPTION</span></span>
<span data-ttu-id="2a35e-108">Il cmdlet **Remove-AzureRmDataFactoryDataset** rimuove un DataSet da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2a35e-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="2a35e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a35e-109">EXAMPLES</span></span>

### <span data-ttu-id="2a35e-110">Esempio 1: rimuovere un DataSet</span><span class="sxs-lookup"><span data-stu-id="2a35e-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2a35e-111">Questo comando rimuove il DataSet denominato DAWikiAggregatedData dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2a35e-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="2a35e-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="2a35e-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="2a35e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a35e-113">PARAMETERS</span></span>

### <span data-ttu-id="2a35e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2a35e-114">-DataFactory</span></span>
<span data-ttu-id="2a35e-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="2a35e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2a35e-116">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2a35e-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a35e-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2a35e-117">-DataFactoryName</span></span>
<span data-ttu-id="2a35e-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="2a35e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2a35e-119">Questo cmdlet consente di rimuovere un DataSet dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2a35e-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a35e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2a35e-120">-Force</span></span>
<span data-ttu-id="2a35e-121">Indica che questo cmdlet rimuove un DataSet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2a35e-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2a35e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a35e-122">-Name</span></span>
<span data-ttu-id="2a35e-123">Specifica il nome del DataSet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2a35e-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="2a35e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a35e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a35e-125">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="2a35e-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2a35e-126">Questo cmdlet consente di rimuovere un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2a35e-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a35e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a35e-127">-Confirm</span></span>
<span data-ttu-id="2a35e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a35e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a35e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a35e-129">-WhatIf</span></span>
<span data-ttu-id="2a35e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a35e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a35e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a35e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a35e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a35e-132">-DefaultProfile</span></span>
<span data-ttu-id="2a35e-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a35e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a35e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a35e-134">CommonParameters</span></span>
<span data-ttu-id="2a35e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a35e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a35e-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a35e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a35e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a35e-137">INPUTS</span></span>

## <span data-ttu-id="2a35e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a35e-138">OUTPUTS</span></span>

### <span data-ttu-id="2a35e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a35e-139">System.Boolean</span></span>

## <span data-ttu-id="2a35e-140">Note</span><span class="sxs-lookup"><span data-stu-id="2a35e-140">NOTES</span></span>
* <span data-ttu-id="2a35e-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="2a35e-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2a35e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a35e-142">RELATED LINKS</span></span>

[<span data-ttu-id="2a35e-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="2a35e-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="2a35e-144">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="2a35e-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


