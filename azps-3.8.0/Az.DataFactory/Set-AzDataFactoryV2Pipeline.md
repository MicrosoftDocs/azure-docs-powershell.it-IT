---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865242"
---
# <span data-ttu-id="63f2e-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="63f2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="63f2e-103">Crea una pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="63f2e-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="63f2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63f2e-104">SYNTAX</span></span>

### <span data-ttu-id="63f2e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63f2e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f2e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63f2e-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f2e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="63f2e-108">Il cmdlet Set-AzDataFactoryV2Pipeline crea una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="63f2e-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="63f2e-109">Se specifichi un nome per una pipeline già esistente, il cmdlet richiede conferma prima di sostituire la pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f2e-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="63f2e-110">Se specifichi il parametro Force, il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="63f2e-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="63f2e-111">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="63f2e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="63f2e-112">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="63f2e-112">-- Create linked services.</span></span>
<span data-ttu-id="63f2e-113">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="63f2e-113">-- Create datasets.</span></span>
<span data-ttu-id="63f2e-114">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f2e-114">-- Create a pipeline.</span></span>
<span data-ttu-id="63f2e-115">Se nella data factory esiste già una pipeline con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f2e-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="63f2e-116">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f2e-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="63f2e-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63f2e-117">EXAMPLES</span></span>

### <span data-ttu-id="63f2e-118">Esempio 1: creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="63f2e-119">Questo comando crea una pipeline denominata DPWikisample nella Factory di dati denominata ADF.</span><span class="sxs-lookup"><span data-stu-id="63f2e-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="63f2e-120">Il comando basa la pipeline sulle informazioni nella DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="63f2e-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="63f2e-121">Questo file include informazioni sulle attività, ad esempio attività di copia e attività di HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="63f2e-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="63f2e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63f2e-122">PARAMETERS</span></span>

### <span data-ttu-id="63f2e-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="63f2e-123">-DataFactoryName</span></span>
<span data-ttu-id="63f2e-124">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="63f2e-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="63f2e-125">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="63f2e-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="63f2e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f2e-126">-DefaultProfile</span></span>
<span data-ttu-id="63f2e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63f2e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f2e-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="63f2e-128">-DefinitionFile</span></span>
<span data-ttu-id="63f2e-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="63f2e-129">The JSON file path.</span></span>

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

### <span data-ttu-id="63f2e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="63f2e-130">-Force</span></span>
<span data-ttu-id="63f2e-131">Indica che questo cmdlet sostituisce una pipeline esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="63f2e-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="63f2e-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="63f2e-132">-Name</span></span>
<span data-ttu-id="63f2e-133">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="63f2e-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="63f2e-135">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="63f2e-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="63f2e-136">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="63f2e-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="63f2e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f2e-137">-ResourceId</span></span>
<span data-ttu-id="63f2e-138">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="63f2e-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="63f2e-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63f2e-139">-Confirm</span></span>
<span data-ttu-id="63f2e-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f2e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f2e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f2e-141">-WhatIf</span></span>
<span data-ttu-id="63f2e-142">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63f2e-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="63f2e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f2e-143">CommonParameters</span></span>
<span data-ttu-id="63f2e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f2e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f2e-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f2e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f2e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63f2e-146">INPUTS</span></span>

### <span data-ttu-id="63f2e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="63f2e-147">System.String</span></span>

## <span data-ttu-id="63f2e-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63f2e-148">OUTPUTS</span></span>

### <span data-ttu-id="63f2e-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="63f2e-150">Note</span><span class="sxs-lookup"><span data-stu-id="63f2e-150">NOTES</span></span>
<span data-ttu-id="63f2e-151">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="63f2e-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="63f2e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63f2e-152">RELATED LINKS</span></span>

[<span data-ttu-id="63f2e-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="63f2e-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="63f2e-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63f2e-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
