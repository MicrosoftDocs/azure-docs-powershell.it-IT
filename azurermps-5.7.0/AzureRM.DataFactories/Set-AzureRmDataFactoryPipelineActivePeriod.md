---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 1c6290f21693f599925f34f950256005df8be670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509915"
---
# <span data-ttu-id="540fe-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="540fe-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="540fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="540fe-102">SYNOPSIS</span></span>
<span data-ttu-id="540fe-103">Configura il periodo attivo per le fette di dati.</span><span class="sxs-lookup"><span data-stu-id="540fe-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="540fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="540fe-104">SYNTAX</span></span>

### <span data-ttu-id="540fe-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="540fe-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="540fe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="540fe-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="540fe-107">DESCRIPTION</span></span>
<span data-ttu-id="540fe-108">Il cmdlet **set-AzureRmDataFactoryPipelineActivePeriod** configura il periodo attivo per le sezioni di dati elaborate da una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="540fe-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="540fe-109">Se si usa il cmdlet Set-AzureRmDataFactorySliceStatus per modificare lo stato delle sezioni per un DataSet, verificare che l'ora di inizio e l'ora di fine per una sezione si trovino nel periodo attivo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="540fe-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>

<span data-ttu-id="540fe-110">Dopo aver creato una pipeline, è possibile specificare il periodo in cui si verifica l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="540fe-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="540fe-111">La specifica del periodo attivo per una pipeline definisce la durata dell'elaborazione delle fette di dati in base alle proprietà di **disponibilità** definite per ogni dataset della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="540fe-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="540fe-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="540fe-112">EXAMPLES</span></span>

### <span data-ttu-id="540fe-113">Esempio 1: configurare il periodo attivo</span><span class="sxs-lookup"><span data-stu-id="540fe-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="540fe-114">Questo comando configura il periodo attivo per le fette di dati che la pipeline denominata DPWikisample elabora.</span><span class="sxs-lookup"><span data-stu-id="540fe-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="540fe-115">Il comando fornisce punti iniziali e finali per le fette di dati come valori.</span><span class="sxs-lookup"><span data-stu-id="540fe-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="540fe-116">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="540fe-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="540fe-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="540fe-117">PARAMETERS</span></span>

### <span data-ttu-id="540fe-118">-Risoluzione del problema</span><span class="sxs-lookup"><span data-stu-id="540fe-118">-AutoResolve</span></span>
<span data-ttu-id="540fe-119">Indica che questo cmdlet usa la risoluzione automatica.</span><span class="sxs-lookup"><span data-stu-id="540fe-119">Indicates that this cmdlet uses auto resolve.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="540fe-120">-DataFactory</span></span>
<span data-ttu-id="540fe-121">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="540fe-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="540fe-122">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="540fe-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="540fe-123">-DataFactoryName</span></span>
<span data-ttu-id="540fe-124">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="540fe-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="540fe-125">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="540fe-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540fe-126">-DefaultProfile</span></span>
<span data-ttu-id="540fe-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="540fe-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="540fe-128">-EndDateTime</span></span>
<span data-ttu-id="540fe-129">Specifica la fine di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="540fe-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="540fe-130">L'elaborazione dei dati si verifica o le fette di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="540fe-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="540fe-131">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="540fe-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="540fe-132">*EndDateTime* deve essere specificato nel formato ISO8601 come negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="540fe-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="540fe-133">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico)</span><span class="sxs-lookup"><span data-stu-id="540fe-133">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="540fe-134">L'indicatore di fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="540fe-134">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-135">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="540fe-135">-ForceRecalculate</span></span>
<span data-ttu-id="540fe-136">Indica che questo cmdlet USA Force Ricalcola.</span><span class="sxs-lookup"><span data-stu-id="540fe-136">Indicates that this cmdlet uses force recalculate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="540fe-137">-PipelineName</span></span>
<span data-ttu-id="540fe-138">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="540fe-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="540fe-139">Questo cmdlet imposta il periodo attivo per la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="540fe-139">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540fe-140">-ResourceGroupName</span></span>
<span data-ttu-id="540fe-141">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="540fe-141">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="540fe-142">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="540fe-142">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-143">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="540fe-143">-StartDateTime</span></span>
<span data-ttu-id="540fe-144">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="540fe-144">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="540fe-145">L'elaborazione dei dati si verifica o le fette di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="540fe-145">Data processing occurs or data slices are processed within this period.</span></span>

<span data-ttu-id="540fe-146">*StartDateTime* deve essere specificato nel formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="540fe-146">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="540fe-147">-Confirm</span></span>
<span data-ttu-id="540fe-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="540fe-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540fe-149">-WhatIf</span></span>
<span data-ttu-id="540fe-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="540fe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540fe-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="540fe-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540fe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540fe-152">CommonParameters</span></span>
<span data-ttu-id="540fe-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540fe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540fe-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540fe-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540fe-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="540fe-155">INPUTS</span></span>

### <span data-ttu-id="540fe-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="540fe-156">None</span></span>
<span data-ttu-id="540fe-157">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="540fe-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="540fe-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="540fe-158">OUTPUTS</span></span>

### <span data-ttu-id="540fe-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="540fe-159">System.Boolean</span></span>

## <span data-ttu-id="540fe-160">Note</span><span class="sxs-lookup"><span data-stu-id="540fe-160">NOTES</span></span>
* <span data-ttu-id="540fe-161">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="540fe-161">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="540fe-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="540fe-162">RELATED LINKS</span></span>

[<span data-ttu-id="540fe-163">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="540fe-163">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="540fe-164">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="540fe-164">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)


