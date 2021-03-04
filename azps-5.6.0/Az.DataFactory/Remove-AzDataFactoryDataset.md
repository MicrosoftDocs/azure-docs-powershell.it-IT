---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 70673fd001078fbeff620f3a6a5ed7dc534ebe2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957405"
---
# <span data-ttu-id="12c29-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="12c29-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="12c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c29-102">SYNOPSIS</span></span>
<span data-ttu-id="12c29-103">Rimuove un set di dati da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="12c29-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="12c29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12c29-104">SYNTAX</span></span>

### <span data-ttu-id="12c29-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="12c29-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12c29-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="12c29-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c29-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12c29-107">DESCRIPTION</span></span>
<span data-ttu-id="12c29-108">Il cmdlet **Remove-AzDataFactoryDataset** rimuove un set di dati da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="12c29-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="12c29-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12c29-109">EXAMPLES</span></span>

### <span data-ttu-id="12c29-110">Esempio 1: Rimuovere un set di dati</span><span class="sxs-lookup"><span data-stu-id="12c29-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="12c29-111">Questo comando rimuove il set di dati denominato DAWikiAggregatedData dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="12c29-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="12c29-112">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="12c29-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="12c29-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c29-113">PARAMETERS</span></span>

### <span data-ttu-id="12c29-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="12c29-114">-DataFactory</span></span>
<span data-ttu-id="12c29-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="12c29-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="12c29-116">Questo cmdlet rimuove un set di dati dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12c29-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="12c29-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12c29-117">-DataFactoryName</span></span>
<span data-ttu-id="12c29-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="12c29-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="12c29-119">Questo cmdlet rimuove un set di dati dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12c29-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="12c29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c29-120">-DefaultProfile</span></span>
<span data-ttu-id="12c29-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="12c29-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12c29-122">-Force</span><span class="sxs-lookup"><span data-stu-id="12c29-122">-Force</span></span>
<span data-ttu-id="12c29-123">Indica che questo cmdlet rimuove un set di dati senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="12c29-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="12c29-124">-Name</span><span class="sxs-lookup"><span data-stu-id="12c29-124">-Name</span></span>
<span data-ttu-id="12c29-125">Specifica il nome del set di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="12c29-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="12c29-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c29-126">-ResourceGroupName</span></span>
<span data-ttu-id="12c29-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="12c29-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="12c29-128">Questo cmdlet rimuove un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12c29-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="12c29-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12c29-129">-Confirm</span></span>
<span data-ttu-id="12c29-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c29-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c29-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c29-131">-WhatIf</span></span>
<span data-ttu-id="12c29-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12c29-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c29-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12c29-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c29-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c29-134">CommonParameters</span></span>
<span data-ttu-id="12c29-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c29-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c29-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c29-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c29-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="12c29-137">INPUTS</span></span>

### <span data-ttu-id="12c29-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="12c29-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="12c29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="12c29-139">System.String</span></span>

## <span data-ttu-id="12c29-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12c29-140">OUTPUTS</span></span>

### <span data-ttu-id="12c29-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="12c29-141">System.Void</span></span>

## <span data-ttu-id="12c29-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="12c29-142">NOTES</span></span>
* <span data-ttu-id="12c29-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="12c29-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="12c29-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12c29-144">RELATED LINKS</span></span>

[<span data-ttu-id="12c29-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="12c29-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="12c29-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="12c29-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


