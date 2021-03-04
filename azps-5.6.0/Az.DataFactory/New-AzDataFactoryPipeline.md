---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: ad731dc612290e572ee74a967788e324f764a930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971230"
---
# <span data-ttu-id="72d12-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="72d12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d12-102">SYNOPSIS</span></span>
<span data-ttu-id="72d12-103">Crea una pipeline in Data factory.</span><span class="sxs-lookup"><span data-stu-id="72d12-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="72d12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72d12-104">SYNTAX</span></span>

### <span data-ttu-id="72d12-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="72d12-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72d12-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="72d12-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d12-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72d12-107">DESCRIPTION</span></span>
<span data-ttu-id="72d12-108">Il cmdlet **New-AzDataFactoryPipeline** crea una pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="72d12-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="72d12-109">Se si specifica un nome per una pipeline già esistente, il cmdlet richiede conferma prima che sostituisca la pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="72d12-110">Se si specifica il *parametro Force,* il cmdlet sostituisce la pipeline esistente senza conferma.</span><span class="sxs-lookup"><span data-stu-id="72d12-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="72d12-111">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="72d12-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="72d12-112">Creare un data factory.</span><span class="sxs-lookup"><span data-stu-id="72d12-112">Create a data factory.</span></span> 
- <span data-ttu-id="72d12-113">Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="72d12-113">Create linked services.</span></span> 
- <span data-ttu-id="72d12-114">Creare set di dati.</span><span class="sxs-lookup"><span data-stu-id="72d12-114">Create datasets.</span></span> 
- <span data-ttu-id="72d12-115">Creare una pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-115">Create a pipeline.</span></span>
<span data-ttu-id="72d12-116">Se nel data factory è già presente una pipeline con lo stesso nome, questo cmdlet chiede di confermare se sovrascrivere la pipeline esistente con la nuova pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="72d12-117">Se si conferma di sovrascrivere la pipeline esistente, viene sostituita anche la definizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="72d12-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72d12-118">EXAMPLES</span></span>

### <span data-ttu-id="72d12-119">Esempio 1: Creare una pipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="72d12-120">Questo comando crea una pipeline denominata DPWikisample nel data factory denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="72d12-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="72d12-121">Il comando basa la pipeline sulle informazioni del DPWikisample.jssu file.</span><span class="sxs-lookup"><span data-stu-id="72d12-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="72d12-122">Questo file include informazioni su attività come l'attività di copia e l'attività HDInsight nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="72d12-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72d12-123">PARAMETERS</span></span>

### <span data-ttu-id="72d12-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="72d12-124">-DataFactory</span></span>
<span data-ttu-id="72d12-125">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="72d12-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="72d12-126">Questo cmdlet crea una pipeline per il data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="72d12-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72d12-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="72d12-127">-DataFactoryName</span></span>
<span data-ttu-id="72d12-128">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="72d12-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="72d12-129">Questo cmdlet crea una pipeline per il data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="72d12-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72d12-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d12-130">-DefaultProfile</span></span>
<span data-ttu-id="72d12-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72d12-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72d12-132">-File</span><span class="sxs-lookup"><span data-stu-id="72d12-132">-File</span></span>
<span data-ttu-id="72d12-133">Specifica il percorso completo del file JSON (JavaScript Object Notation) che contiene la descrizione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="72d12-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="72d12-134">-Force</span><span class="sxs-lookup"><span data-stu-id="72d12-134">-Force</span></span>
<span data-ttu-id="72d12-135">Indica che questo cmdlet sostituisce una pipeline esistente senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="72d12-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="72d12-136">-Name</span><span class="sxs-lookup"><span data-stu-id="72d12-136">-Name</span></span>
<span data-ttu-id="72d12-137">Specifica il nome della pipeline da creare.</span><span class="sxs-lookup"><span data-stu-id="72d12-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="72d12-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d12-138">-ResourceGroupName</span></span>
<span data-ttu-id="72d12-139">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="72d12-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="72d12-140">Questo cmdlet crea una pipeline per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="72d12-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="72d12-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72d12-141">-Confirm</span></span>
<span data-ttu-id="72d12-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72d12-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d12-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d12-143">-WhatIf</span></span>
<span data-ttu-id="72d12-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72d12-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d12-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72d12-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d12-146">CommonParameters</span></span>
<span data-ttu-id="72d12-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d12-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d12-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d12-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="72d12-149">INPUTS</span></span>

### <span data-ttu-id="72d12-150">System.String</span><span class="sxs-lookup"><span data-stu-id="72d12-150">System.String</span></span>

### <span data-ttu-id="72d12-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="72d12-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="72d12-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72d12-152">OUTPUTS</span></span>

### <span data-ttu-id="72d12-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="72d12-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="72d12-154">NOTES</span></span>
* <span data-ttu-id="72d12-155">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="72d12-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="72d12-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72d12-156">RELATED LINKS</span></span>

[<span data-ttu-id="72d12-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="72d12-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="72d12-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="72d12-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="72d12-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="72d12-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72d12-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


