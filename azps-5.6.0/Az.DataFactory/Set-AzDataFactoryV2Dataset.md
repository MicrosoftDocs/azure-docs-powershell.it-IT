---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006957"
---
# <span data-ttu-id="84a80-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="84a80-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="84a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a80-102">SYNOPSIS</span></span>
<span data-ttu-id="84a80-103">Crea un set di dati in Data factory.</span><span class="sxs-lookup"><span data-stu-id="84a80-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="84a80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84a80-104">SYNTAX</span></span>

### <span data-ttu-id="84a80-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="84a80-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84a80-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84a80-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a80-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84a80-107">DESCRIPTION</span></span>
<span data-ttu-id="84a80-108">Il cmdlet Set-AzDataFactoryV2Dataset crea un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="84a80-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="84a80-109">Se si specifica un nome per un set di dati già esistente, questo cmdlet richiede conferma prima che sostituisca il set di dati.</span><span class="sxs-lookup"><span data-stu-id="84a80-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="84a80-110">Se si specifica il parametro Force, il cmdlet sostituisce il set di dati esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="84a80-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="84a80-111">Eseguire queste operazioni nell'ordine seguente: -- Creare un data factory.</span><span class="sxs-lookup"><span data-stu-id="84a80-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="84a80-112">-- Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="84a80-112">-- Create linked services.</span></span>
<span data-ttu-id="84a80-113">-- Creare set di dati.</span><span class="sxs-lookup"><span data-stu-id="84a80-113">-- Create datasets.</span></span>
<span data-ttu-id="84a80-114">-- Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="84a80-114">-- Create a pipeline.</span></span>
<span data-ttu-id="84a80-115">Se esiste già un set di dati con lo stesso nome nel data factory, questo cmdlet chiede di confermare se sovrascrivere il set di dati esistente con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="84a80-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="84a80-116">Se si conferma di sovrascrivere il set di dati esistente, viene sostituita anche la definizione del set di dati.</span><span class="sxs-lookup"><span data-stu-id="84a80-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="84a80-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84a80-117">EXAMPLES</span></span>

### <span data-ttu-id="84a80-118">Esempio 1: Creare un set di dati</span><span class="sxs-lookup"><span data-stu-id="84a80-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="84a80-119">Questo comando crea un set di DA_WikipediaClickEvents dati denominato WikiADF nel data factory.</span><span class="sxs-lookup"><span data-stu-id="84a80-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="84a80-120">Il comando basa il set di dati sulle informazioni DAWikipediaClickEvents.jssu file.</span><span class="sxs-lookup"><span data-stu-id="84a80-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="84a80-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a80-121">PARAMETERS</span></span>

### <span data-ttu-id="84a80-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84a80-122">-DataFactoryName</span></span>
<span data-ttu-id="84a80-123">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="84a80-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="84a80-124">Questo cmdlet crea un set di dati nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84a80-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84a80-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a80-125">-DefaultProfile</span></span>
<span data-ttu-id="84a80-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84a80-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84a80-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="84a80-127">-DefinitionFile</span></span>
<span data-ttu-id="84a80-128">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="84a80-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a80-129">-Force</span><span class="sxs-lookup"><span data-stu-id="84a80-129">-Force</span></span>
<span data-ttu-id="84a80-130">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="84a80-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="84a80-131">-Name</span><span class="sxs-lookup"><span data-stu-id="84a80-131">-Name</span></span>
<span data-ttu-id="84a80-132">Specifica il nome del set di dati da creare.</span><span class="sxs-lookup"><span data-stu-id="84a80-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a80-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a80-133">-ResourceGroupName</span></span>
<span data-ttu-id="84a80-134">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="84a80-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84a80-135">Questo cmdlet crea un set di dati nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84a80-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84a80-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84a80-136">-ResourceId</span></span>
<span data-ttu-id="84a80-137">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="84a80-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84a80-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84a80-138">-Confirm</span></span>
<span data-ttu-id="84a80-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a80-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a80-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a80-140">-WhatIf</span></span>
<span data-ttu-id="84a80-141">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="84a80-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="84a80-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a80-142">CommonParameters</span></span>
<span data-ttu-id="84a80-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a80-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a80-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a80-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a80-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="84a80-145">INPUTS</span></span>

### <span data-ttu-id="84a80-146">System.String</span><span class="sxs-lookup"><span data-stu-id="84a80-146">System.String</span></span>

## <span data-ttu-id="84a80-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84a80-147">OUTPUTS</span></span>

### <span data-ttu-id="84a80-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="84a80-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="84a80-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="84a80-149">NOTES</span></span>
<span data-ttu-id="84a80-150">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="84a80-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84a80-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84a80-151">RELATED LINKS</span></span>

[<span data-ttu-id="84a80-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="84a80-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="84a80-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="84a80-153">Remove-AzDataFactoryV2Dataset</span></span>]()
