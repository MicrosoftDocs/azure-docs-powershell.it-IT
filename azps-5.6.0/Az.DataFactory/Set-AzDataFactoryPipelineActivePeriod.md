---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 5cbb353a0a6349842878ef787b75c1ce34b1cfd3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964926"
---
# <span data-ttu-id="78f39-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="78f39-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="78f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f39-102">SYNOPSIS</span></span>
<span data-ttu-id="78f39-103">Configura il periodo attivo per le sezioni di dati.</span><span class="sxs-lookup"><span data-stu-id="78f39-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="78f39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78f39-104">SYNTAX</span></span>

### <span data-ttu-id="78f39-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="78f39-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78f39-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="78f39-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f39-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78f39-107">DESCRIPTION</span></span>
<span data-ttu-id="78f39-108">Il cmdlet **Set-AzDataFactoryPipelineActivePeriod** configura il periodo attivo per le sezioni di dati elaborate da una pipeline in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="78f39-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="78f39-109">Se si usa il cmdlet Set-AzDataFactorySliceStatus per modificare lo stato delle sezioni per un set di dati, verificare che l'ora di inizio e l'ora di fine per una sezione siano nel periodo attivo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="78f39-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="78f39-110">Dopo aver creato una pipeline, è possibile specificare il periodo di elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="78f39-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="78f39-111">Se si specifica il periodo attivo per una pipeline, viene definita la durata dell'elaborazione delle sezioni di dati in base alle proprietà **Di** disponibilità definite per ogni set di dati di Data factory.</span><span class="sxs-lookup"><span data-stu-id="78f39-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="78f39-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78f39-112">EXAMPLES</span></span>

### <span data-ttu-id="78f39-113">Esempio 1: Configurare il periodo attivo</span><span class="sxs-lookup"><span data-stu-id="78f39-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="78f39-114">Questo comando configura il periodo attivo per le sezioni di dati la pipeline denominata DPWikisample.</span><span class="sxs-lookup"><span data-stu-id="78f39-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="78f39-115">Il comando fornisce i punti iniziali e finali per le sezioni di dati come valori.</span><span class="sxs-lookup"><span data-stu-id="78f39-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="78f39-116">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="78f39-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="78f39-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78f39-117">PARAMETERS</span></span>

### <span data-ttu-id="78f39-118">-Risolvere automaticamente</span><span class="sxs-lookup"><span data-stu-id="78f39-118">-AutoResolve</span></span>
<span data-ttu-id="78f39-119">Indica che questo cmdlet usa la risoluzione automatica.</span><span class="sxs-lookup"><span data-stu-id="78f39-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="78f39-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78f39-120">-DataFactory</span></span>
<span data-ttu-id="78f39-121">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="78f39-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="78f39-122">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78f39-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78f39-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78f39-123">-DataFactoryName</span></span>
<span data-ttu-id="78f39-124">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="78f39-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="78f39-125">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78f39-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="78f39-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f39-126">-DefaultProfile</span></span>
<span data-ttu-id="78f39-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="78f39-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78f39-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="78f39-128">-EndDateTime</span></span>
<span data-ttu-id="78f39-129">Specifica la fine di un periodo di tempo come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="78f39-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="78f39-130">Viene eseguita l'elaborazione dei dati o le sezioni di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="78f39-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="78f39-131">Per altre informazioni sugli **oggetti DateTime,** digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="78f39-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="78f39-132">*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (ora standard del Pacifico) Il fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="78f39-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f39-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="78f39-133">-ForceRecalculate</span></span>
<span data-ttu-id="78f39-134">Indica che questo cmdlet usa il ricalcolo forzato.</span><span class="sxs-lookup"><span data-stu-id="78f39-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="78f39-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="78f39-135">-PipelineName</span></span>
<span data-ttu-id="78f39-136">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="78f39-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="78f39-137">Questo cmdlet imposta il periodo attivo per la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78f39-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f39-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f39-138">-ResourceGroupName</span></span>
<span data-ttu-id="78f39-139">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="78f39-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="78f39-140">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78f39-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78f39-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="78f39-141">-StartDateTime</span></span>
<span data-ttu-id="78f39-142">Specifica l'inizio di un periodo di tempo come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="78f39-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="78f39-143">Viene eseguita l'elaborazione dei dati o le sezioni di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="78f39-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="78f39-144">*È necessario specificare StartDateTime* nel formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="78f39-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f39-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78f39-145">-Confirm</span></span>
<span data-ttu-id="78f39-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f39-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f39-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f39-147">-WhatIf</span></span>
<span data-ttu-id="78f39-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f39-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f39-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f39-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f39-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f39-150">CommonParameters</span></span>
<span data-ttu-id="78f39-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f39-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f39-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f39-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f39-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="78f39-153">INPUTS</span></span>

### <span data-ttu-id="78f39-154">System.String</span><span class="sxs-lookup"><span data-stu-id="78f39-154">System.String</span></span>

### <span data-ttu-id="78f39-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78f39-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="78f39-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78f39-156">OUTPUTS</span></span>

### <span data-ttu-id="78f39-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78f39-157">System.Boolean</span></span>

## <span data-ttu-id="78f39-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="78f39-158">NOTES</span></span>
* <span data-ttu-id="78f39-159">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="78f39-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="78f39-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78f39-160">RELATED LINKS</span></span>

[<span data-ttu-id="78f39-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="78f39-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="78f39-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="78f39-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


