---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 50942dfc9b31b96a796b0a77df8b1ffc1a4cbd36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688127"
---
# <span data-ttu-id="12a8d-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="12a8d-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="12a8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="12a8d-103">Ottiene le fette di dati per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="12a8d-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12a8d-104">SYNTAX</span></span>

### <span data-ttu-id="12a8d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12a8d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12a8d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="12a8d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a8d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12a8d-107">DESCRIPTION</span></span>
<span data-ttu-id="12a8d-108">Il cmdlet **Get-AzureRmDataFactorySlice** ottiene le fette di dati per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="12a8d-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="12a8d-109">Specificare l'ora di inizio e l'ora di fine per definire un intervallo di sezioni di dati da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="12a8d-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="12a8d-110">Lo stato di una fetta di dati è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a8d-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="12a8d-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="12a8d-111">PendingExecution.</span></span>
<span data-ttu-id="12a8d-112">L'elaborazione dei dati non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="12a8d-112">Data processing has not started.</span></span> 
- <span data-ttu-id="12a8d-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="12a8d-113">InProgress.</span></span>
<span data-ttu-id="12a8d-114">L'elaborazione dei dati è in corso.</span><span class="sxs-lookup"><span data-stu-id="12a8d-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="12a8d-115">Pronto.</span><span class="sxs-lookup"><span data-stu-id="12a8d-115">Ready.</span></span>
<span data-ttu-id="12a8d-116">L'elaborazione dei dati è completata.</span><span class="sxs-lookup"><span data-stu-id="12a8d-116">Data processing is completed.</span></span>
<span data-ttu-id="12a8d-117">La sezione dati è pronta per l'utilizzo delle sezioni dipendenti.</span><span class="sxs-lookup"><span data-stu-id="12a8d-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="12a8d-118">Fallito.</span><span class="sxs-lookup"><span data-stu-id="12a8d-118">Failed.</span></span>
<span data-ttu-id="12a8d-119">L'esecuzione che produce la sezione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="12a8d-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="12a8d-120">Ignorare.</span><span class="sxs-lookup"><span data-stu-id="12a8d-120">Skip.</span></span>
<span data-ttu-id="12a8d-121">Data Factory ignora l'elaborazione della sezione.</span><span class="sxs-lookup"><span data-stu-id="12a8d-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="12a8d-122">Tentativi.</span><span class="sxs-lookup"><span data-stu-id="12a8d-122">Retry.</span></span>
<span data-ttu-id="12a8d-123">Data Factory ritenta l'esecuzione che produce la sezione.</span><span class="sxs-lookup"><span data-stu-id="12a8d-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="12a8d-124">Scaduta. L'elaborazione dei dati è scaduta.</span><span class="sxs-lookup"><span data-stu-id="12a8d-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="12a8d-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="12a8d-125">PendingValidation.</span></span>
<span data-ttu-id="12a8d-126">La data Slice attende la convalida prima che venga elaborata.</span><span class="sxs-lookup"><span data-stu-id="12a8d-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="12a8d-127">Ripetere la convalida.</span><span class="sxs-lookup"><span data-stu-id="12a8d-127">Retry Validation.</span></span>
<span data-ttu-id="12a8d-128">Data Factory ritenta la convalida della sezione.</span><span class="sxs-lookup"><span data-stu-id="12a8d-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="12a8d-129">Convalida non riuscita.</span><span class="sxs-lookup"><span data-stu-id="12a8d-129">Failed Validation.</span></span>
<span data-ttu-id="12a8d-130">La convalida della sezione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="12a8d-130">Validation of the slice failed.</span></span>
<span data-ttu-id="12a8d-131">Per ognuna delle sezioni, è possibile visualizzare altre informazioni sull'esecuzione che produce la sezione usando il cmdlet Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="12a8d-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="12a8d-132">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12a8d-132">EXAMPLES</span></span>

### <span data-ttu-id="12a8d-133">Esempio 1: recuperare le fette di dati per un DataSet</span><span class="sxs-lookup"><span data-stu-id="12a8d-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="12a8d-134">Questo comando consente di ottenere tutte le fette di dati per il DataSet denominato WikiAggregatedData nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="12a8d-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="12a8d-135">Il comando ottiene le sezioni prodotte dopo il tempo specificato dal parametro StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="12a8d-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="12a8d-136">Il codice di esempio seguente imposta la disponibilità per questo DataSet ogni ora nel file JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="12a8d-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="12a8d-137">disponibilità: {periodo: "hour", periodMultiplier: 1} alcuni dei risultati sono pronti e altri sono PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="12a8d-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="12a8d-138">Le sezioni pronte sono già state eseguite.</span><span class="sxs-lookup"><span data-stu-id="12a8d-138">Ready slices have already run.</span></span>
<span data-ttu-id="12a8d-139">Le sezioni in sospeso sono in attesa di esecuzione alla fine di ogni ora nell'intervallo specificato dal cmdlet Set-AzureRmDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="12a8d-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="12a8d-140">In questo esempio, i periodi di inizio e di fine per la pipeline e la sezione hanno un valore di un giorno (24 ore).</span><span class="sxs-lookup"><span data-stu-id="12a8d-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="12a8d-141">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12a8d-141">PARAMETERS</span></span>

### <span data-ttu-id="12a8d-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="12a8d-142">-DataFactory</span></span>
<span data-ttu-id="12a8d-143">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="12a8d-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="12a8d-144">Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a8d-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a8d-145">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="12a8d-145">-DataFactoryName</span></span>
<span data-ttu-id="12a8d-146">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="12a8d-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="12a8d-147">Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a8d-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a8d-148">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="12a8d-148">-DatasetName</span></span>
<span data-ttu-id="12a8d-149">Specifica il nome del DataSet per cui questo cmdlet ottiene le sezioni.</span><span class="sxs-lookup"><span data-stu-id="12a8d-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a8d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a8d-150">-DefaultProfile</span></span>
<span data-ttu-id="12a8d-151">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="12a8d-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a8d-152">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="12a8d-152">-EndDateTime</span></span>
<span data-ttu-id="12a8d-153">Specifica la fine di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="12a8d-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="12a8d-154">Questo cmdlet ottiene le sezioni prodotte prima del tempo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a8d-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="12a8d-155">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="12a8d-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="12a8d-156">*EndDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) l'identificatore del fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="12a8d-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="12a8d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a8d-157">-ResourceGroupName</span></span>
<span data-ttu-id="12a8d-158">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="12a8d-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="12a8d-159">Questo cmdlet ottiene le sezioni che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a8d-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a8d-160">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="12a8d-160">-StartDateTime</span></span>
<span data-ttu-id="12a8d-161">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="12a8d-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="12a8d-162">Questo cmdlet ottiene le sezioni prodotte dopo il tempo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a8d-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="12a8d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a8d-163">CommonParameters</span></span>
<span data-ttu-id="12a8d-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a8d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a8d-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a8d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a8d-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12a8d-166">INPUTS</span></span>

### <span data-ttu-id="12a8d-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="12a8d-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="12a8d-168">System. String</span><span class="sxs-lookup"><span data-stu-id="12a8d-168">System.String</span></span>

## <span data-ttu-id="12a8d-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12a8d-169">OUTPUTS</span></span>

### <span data-ttu-id="12a8d-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="12a8d-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="12a8d-171">Note</span><span class="sxs-lookup"><span data-stu-id="12a8d-171">NOTES</span></span>
* <span data-ttu-id="12a8d-172">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="12a8d-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="12a8d-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12a8d-173">RELATED LINKS</span></span>

[<span data-ttu-id="12a8d-174">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="12a8d-174">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="12a8d-175">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="12a8d-175">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="12a8d-176">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="12a8d-176">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

