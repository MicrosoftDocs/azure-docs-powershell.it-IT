---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 7cbd9331802df11bb1fe243265e82fd73d6524f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686436"
---
# <span data-ttu-id="89252-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="89252-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="89252-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89252-102">SYNOPSIS</span></span>
<span data-ttu-id="89252-103">Configura il periodo attivo per le fette di dati.</span><span class="sxs-lookup"><span data-stu-id="89252-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89252-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89252-104">SYNTAX</span></span>

### <span data-ttu-id="89252-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89252-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89252-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="89252-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89252-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89252-107">DESCRIPTION</span></span>
<span data-ttu-id="89252-108">Il cmdlet **set-AzureRmDataFactoryPipelineActivePeriod** configura il periodo attivo per le sezioni di dati elaborate da una pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="89252-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="89252-109">Se si usa il cmdlet Set-AzureRmDataFactorySliceStatus per modificare lo stato delle sezioni per un DataSet, verificare che l'ora di inizio e l'ora di fine per una sezione si trovino nel periodo attivo della pipeline.</span><span class="sxs-lookup"><span data-stu-id="89252-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="89252-110">Dopo aver creato una pipeline, è possibile specificare il periodo in cui si verifica l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="89252-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="89252-111">La specifica del periodo attivo per una pipeline definisce la durata dell'elaborazione delle fette di dati in base alle proprietà di **disponibilità** definite per ogni dataset della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="89252-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="89252-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89252-112">EXAMPLES</span></span>

### <span data-ttu-id="89252-113">Esempio 1: configurare il periodo attivo</span><span class="sxs-lookup"><span data-stu-id="89252-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="89252-114">Questo comando configura il periodo attivo per le fette di dati che la pipeline denominata DPWikisample elabora.</span><span class="sxs-lookup"><span data-stu-id="89252-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="89252-115">Il comando fornisce punti iniziali e finali per le fette di dati come valori.</span><span class="sxs-lookup"><span data-stu-id="89252-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="89252-116">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="89252-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="89252-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89252-117">PARAMETERS</span></span>

### <span data-ttu-id="89252-118">-Risoluzione del problema</span><span class="sxs-lookup"><span data-stu-id="89252-118">-AutoResolve</span></span>
<span data-ttu-id="89252-119">Indica che questo cmdlet usa la risoluzione automatica.</span><span class="sxs-lookup"><span data-stu-id="89252-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="89252-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="89252-120">-DataFactory</span></span>
<span data-ttu-id="89252-121">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="89252-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="89252-122">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="89252-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89252-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="89252-123">-DataFactoryName</span></span>
<span data-ttu-id="89252-124">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="89252-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="89252-125">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="89252-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89252-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89252-126">-DefaultProfile</span></span>
<span data-ttu-id="89252-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89252-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89252-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="89252-128">-EndDateTime</span></span>
<span data-ttu-id="89252-129">Specifica la fine di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="89252-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="89252-130">L'elaborazione dei dati si verifica o le fette di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="89252-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="89252-131">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="89252-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="89252-132">*EndDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) l'identificatore del fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="89252-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="89252-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="89252-133">-ForceRecalculate</span></span>
<span data-ttu-id="89252-134">Indica che questo cmdlet USA Force Ricalcola.</span><span class="sxs-lookup"><span data-stu-id="89252-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="89252-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="89252-135">-PipelineName</span></span>
<span data-ttu-id="89252-136">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="89252-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="89252-137">Questo cmdlet imposta il periodo attivo per la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="89252-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="89252-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89252-138">-ResourceGroupName</span></span>
<span data-ttu-id="89252-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="89252-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="89252-140">Questo cmdlet modifica il periodo attivo per una pipeline che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="89252-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="89252-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="89252-141">-StartDateTime</span></span>
<span data-ttu-id="89252-142">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="89252-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="89252-143">L'elaborazione dei dati si verifica o le fette di dati vengono elaborate entro questo periodo.</span><span class="sxs-lookup"><span data-stu-id="89252-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="89252-144">*StartDateTime* deve essere specificato nel formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="89252-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="89252-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89252-145">-Confirm</span></span>
<span data-ttu-id="89252-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89252-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89252-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89252-147">-WhatIf</span></span>
<span data-ttu-id="89252-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89252-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89252-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89252-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89252-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89252-150">CommonParameters</span></span>
<span data-ttu-id="89252-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89252-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89252-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89252-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89252-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89252-153">INPUTS</span></span>

### <span data-ttu-id="89252-154">System. String</span><span class="sxs-lookup"><span data-stu-id="89252-154">System.String</span></span>

### <span data-ttu-id="89252-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="89252-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="89252-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89252-156">OUTPUTS</span></span>

### <span data-ttu-id="89252-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89252-157">System.Boolean</span></span>

## <span data-ttu-id="89252-158">Note</span><span class="sxs-lookup"><span data-stu-id="89252-158">NOTES</span></span>
* <span data-ttu-id="89252-159">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="89252-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="89252-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89252-160">RELATED LINKS</span></span>

[<span data-ttu-id="89252-161">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="89252-161">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="89252-162">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="89252-162">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)


