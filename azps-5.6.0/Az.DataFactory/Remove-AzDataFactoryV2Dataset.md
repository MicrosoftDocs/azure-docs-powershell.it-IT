---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: a5c7ca7a651510d8b417beedc28cbd5ba26e6fe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954734"
---
# <span data-ttu-id="3ca8f-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3ca8f-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3ca8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca8f-103">Rimuove un set di dati da Data factory.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="3ca8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ca8f-104">SYNTAX</span></span>

### <span data-ttu-id="3ca8f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="3ca8f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca8f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ca8f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca8f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca8f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca8f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ca8f-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca8f-109">Il cmdlet Remove-AzDataFactoryV2Dataset rimuove un set di dati da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="3ca8f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ca8f-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca8f-111">Esempio 1: Rimuovere un set di dati</span><span class="sxs-lookup"><span data-stu-id="3ca8f-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="3ca8f-112">Questo comando rimuove il set di dati denominato DAWikiAggregatedData dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="3ca8f-113">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3ca8f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ca8f-114">PARAMETERS</span></span>

### <span data-ttu-id="3ca8f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3ca8f-115">-DataFactoryName</span></span>
<span data-ttu-id="3ca8f-116">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3ca8f-117">Questo cmdlet rimuove un set di dati dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ca8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca8f-118">-DefaultProfile</span></span>
<span data-ttu-id="3ca8f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ca8f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca8f-120">-Force</span></span>
<span data-ttu-id="3ca8f-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3ca8f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca8f-122">-InputObject</span></span>
<span data-ttu-id="3ca8f-123">Specifica un oggetto Dataset da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="3ca8f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3ca8f-124">-Name</span></span>
<span data-ttu-id="3ca8f-125">Specifica il nome del set di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="3ca8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ca8f-127">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3ca8f-128">Questo cmdlet rimuove un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ca8f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca8f-129">-ResourceId</span></span>
<span data-ttu-id="3ca8f-130">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3ca8f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca8f-131">-Confirm</span></span>
<span data-ttu-id="3ca8f-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca8f-133">-WhatIf</span></span>
<span data-ttu-id="3ca8f-134">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3ca8f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca8f-135">CommonParameters</span></span>
<span data-ttu-id="3ca8f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca8f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca8f-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca8f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca8f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ca8f-138">INPUTS</span></span>

### <span data-ttu-id="3ca8f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3ca8f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="3ca8f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca8f-140">System.String</span></span>

## <span data-ttu-id="3ca8f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ca8f-141">OUTPUTS</span></span>

### <span data-ttu-id="3ca8f-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="3ca8f-142">System.Void</span></span>

## <span data-ttu-id="3ca8f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ca8f-143">NOTES</span></span>
<span data-ttu-id="3ca8f-144">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="3ca8f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3ca8f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ca8f-145">RELATED LINKS</span></span>

[<span data-ttu-id="3ca8f-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3ca8f-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3ca8f-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3ca8f-147">Set-AzDataFactoryV2Dataset</span></span>]()
