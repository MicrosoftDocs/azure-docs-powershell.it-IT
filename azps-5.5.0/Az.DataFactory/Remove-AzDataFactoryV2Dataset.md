---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180991"
---
# <span data-ttu-id="60e9b-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="60e9b-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="60e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="60e9b-103">Rimuove un set di dati da Data factory.</span><span class="sxs-lookup"><span data-stu-id="60e9b-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="60e9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60e9b-104">SYNTAX</span></span>

### <span data-ttu-id="60e9b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="60e9b-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e9b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60e9b-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e9b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60e9b-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e9b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60e9b-108">DESCRIPTION</span></span>
<span data-ttu-id="60e9b-109">Il cmdlet Remove-AzDataFactoryV2Dataset rimuove un set di dati da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="60e9b-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="60e9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60e9b-110">EXAMPLES</span></span>

### <span data-ttu-id="60e9b-111">Esempio 1: Rimuovere un set di dati</span><span class="sxs-lookup"><span data-stu-id="60e9b-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="60e9b-112">Questo comando rimuove il set di dati denominato DAWikiAggregatedData dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="60e9b-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="60e9b-113">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="60e9b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="60e9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60e9b-114">PARAMETERS</span></span>

### <span data-ttu-id="60e9b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="60e9b-115">-DataFactoryName</span></span>
<span data-ttu-id="60e9b-116">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="60e9b-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="60e9b-117">Questo cmdlet rimuove un set di dati dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="60e9b-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="60e9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e9b-118">-DefaultProfile</span></span>
<span data-ttu-id="60e9b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60e9b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60e9b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="60e9b-120">-Force</span></span>
<span data-ttu-id="60e9b-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="60e9b-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="60e9b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60e9b-122">-InputObject</span></span>
<span data-ttu-id="60e9b-123">Specifica un oggetto Dataset da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="60e9b-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="60e9b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="60e9b-124">-Name</span></span>
<span data-ttu-id="60e9b-125">Specifica il nome del set di dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="60e9b-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="60e9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="60e9b-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="60e9b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="60e9b-128">Questo cmdlet rimuove un set di dati dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="60e9b-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="60e9b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60e9b-129">-ResourceId</span></span>
<span data-ttu-id="60e9b-130">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="60e9b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="60e9b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60e9b-131">-Confirm</span></span>
<span data-ttu-id="60e9b-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e9b-133">-WhatIf</span></span>
<span data-ttu-id="60e9b-134">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="60e9b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="60e9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e9b-135">CommonParameters</span></span>
<span data-ttu-id="60e9b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e9b-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e9b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e9b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="60e9b-138">INPUTS</span></span>

### <span data-ttu-id="60e9b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="60e9b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="60e9b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="60e9b-140">System.String</span></span>

## <span data-ttu-id="60e9b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60e9b-141">OUTPUTS</span></span>

### <span data-ttu-id="60e9b-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="60e9b-142">System.Void</span></span>

## <span data-ttu-id="60e9b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="60e9b-143">NOTES</span></span>
<span data-ttu-id="60e9b-144">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="60e9b-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="60e9b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60e9b-145">RELATED LINKS</span></span>

[<span data-ttu-id="60e9b-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="60e9b-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="60e9b-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="60e9b-147">Set-AzDataFactoryV2Dataset</span></span>]()
