---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298410"
---
# <span data-ttu-id="d1150-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="d1150-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1150-102">SYNOPSIS</span></span>
<span data-ttu-id="d1150-103">Crea una pipeline in data factory.</span><span class="sxs-lookup"><span data-stu-id="d1150-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="d1150-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1150-104">SYNTAX</span></span>

### <span data-ttu-id="d1150-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1150-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1150-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d1150-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1150-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1150-107">DESCRIPTION</span></span>
<span data-ttu-id="d1150-108">Il cmdlet **New-AzDataFactoryPipeline** crea una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d1150-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="d1150-109">Se specifichi un nome per una pipeline già esistente, il cmdlet richiede conferma prima di sostituire la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="d1150-110">Se specifichi il parametro *Force* , il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d1150-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="d1150-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="d1150-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="d1150-112">Creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="d1150-112">Create a data factory.</span></span> 
- <span data-ttu-id="d1150-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="d1150-113">Create linked services.</span></span> 
- <span data-ttu-id="d1150-114">Creare set di DataSet.</span><span class="sxs-lookup"><span data-stu-id="d1150-114">Create datasets.</span></span> 
- <span data-ttu-id="d1150-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-115">Create a pipeline.</span></span>
<span data-ttu-id="d1150-116">Se nella data factory esiste già una pipeline con lo stesso nome, questo cmdlet richiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="d1150-117">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="d1150-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1150-118">EXAMPLES</span></span>

### <span data-ttu-id="d1150-119">Esempio 1: creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="d1150-120">Questo comando crea una pipeline denominata DPWikisample nella Factory di dati denominata ADF.</span><span class="sxs-lookup"><span data-stu-id="d1150-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="d1150-121">Il comando basa la pipeline sulle informazioni nella DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="d1150-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="d1150-122">Questo file include informazioni sulle attività, ad esempio attività di copia e attività di HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="d1150-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1150-123">PARAMETERS</span></span>

### <span data-ttu-id="d1150-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1150-124">-DataFactory</span></span>
<span data-ttu-id="d1150-125">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d1150-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d1150-126">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d1150-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1150-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d1150-127">-DataFactoryName</span></span>
<span data-ttu-id="d1150-128">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="d1150-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d1150-129">Questo cmdlet crea una pipeline per la factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d1150-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1150-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1150-130">-DefaultProfile</span></span>
<span data-ttu-id="d1150-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1150-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1150-132">-File</span><span class="sxs-lookup"><span data-stu-id="d1150-132">-File</span></span>
<span data-ttu-id="d1150-133">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1150-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1150-134">-Force</span><span class="sxs-lookup"><span data-stu-id="d1150-134">-Force</span></span>
<span data-ttu-id="d1150-135">Indica che questo cmdlet sostituisce una pipeline esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d1150-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d1150-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1150-136">-Name</span></span>
<span data-ttu-id="d1150-137">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="d1150-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1150-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1150-138">-ResourceGroupName</span></span>
<span data-ttu-id="d1150-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d1150-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d1150-140">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d1150-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1150-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1150-141">-Confirm</span></span>
<span data-ttu-id="d1150-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1150-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1150-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1150-143">-WhatIf</span></span>
<span data-ttu-id="d1150-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1150-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1150-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1150-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1150-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1150-146">CommonParameters</span></span>
<span data-ttu-id="d1150-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1150-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1150-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1150-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1150-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1150-149">INPUTS</span></span>

### <span data-ttu-id="d1150-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d1150-150">System.String</span></span>

### <span data-ttu-id="d1150-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1150-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d1150-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1150-152">OUTPUTS</span></span>

### <span data-ttu-id="d1150-153">Microsoft. Azure. Commands. datafactories. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="d1150-154">Note</span><span class="sxs-lookup"><span data-stu-id="d1150-154">NOTES</span></span>
* <span data-ttu-id="d1150-155">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="d1150-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d1150-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1150-156">RELATED LINKS</span></span>

[<span data-ttu-id="d1150-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="d1150-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="d1150-159">Curriculum vitae-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="d1150-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d1150-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d1150-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d1150-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


