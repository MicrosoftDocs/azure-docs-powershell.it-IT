---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190292"
---
# <span data-ttu-id="61443-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="61443-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="61443-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61443-102">SYNOPSIS</span></span>
<span data-ttu-id="61443-103">Ottiene le fette di dati per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="61443-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="61443-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61443-104">SYNTAX</span></span>

### <span data-ttu-id="61443-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61443-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61443-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="61443-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61443-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61443-107">DESCRIPTION</span></span>
<span data-ttu-id="61443-108">Il cmdlet **Get-AzDataFactorySlice** ottiene le fette di dati per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="61443-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="61443-109">Specificare l'ora di inizio e l'ora di fine per definire un intervallo di sezioni di dati da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="61443-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="61443-110">Lo stato di una fetta di dati è uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="61443-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="61443-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="61443-111">PendingExecution.</span></span>
<span data-ttu-id="61443-112">L'elaborazione dei dati non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="61443-112">Data processing has not started.</span></span> 
- <span data-ttu-id="61443-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="61443-113">InProgress.</span></span>
<span data-ttu-id="61443-114">L'elaborazione dei dati è in corso.</span><span class="sxs-lookup"><span data-stu-id="61443-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="61443-115">Pronto.</span><span class="sxs-lookup"><span data-stu-id="61443-115">Ready.</span></span>
<span data-ttu-id="61443-116">L'elaborazione dei dati è completata.</span><span class="sxs-lookup"><span data-stu-id="61443-116">Data processing is completed.</span></span>
<span data-ttu-id="61443-117">La sezione dati è pronta per l'utilizzo delle sezioni dipendenti.</span><span class="sxs-lookup"><span data-stu-id="61443-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="61443-118">Fallito.</span><span class="sxs-lookup"><span data-stu-id="61443-118">Failed.</span></span>
<span data-ttu-id="61443-119">L'esecuzione che produce la sezione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="61443-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="61443-120">Ignorare.</span><span class="sxs-lookup"><span data-stu-id="61443-120">Skip.</span></span>
<span data-ttu-id="61443-121">Data Factory ignora l'elaborazione della sezione.</span><span class="sxs-lookup"><span data-stu-id="61443-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="61443-122">Tentativi.</span><span class="sxs-lookup"><span data-stu-id="61443-122">Retry.</span></span>
<span data-ttu-id="61443-123">Data Factory ritenta l'esecuzione che produce la sezione.</span><span class="sxs-lookup"><span data-stu-id="61443-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="61443-124">Scaduta. L'elaborazione dei dati è scaduta.</span><span class="sxs-lookup"><span data-stu-id="61443-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="61443-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="61443-125">PendingValidation.</span></span>
<span data-ttu-id="61443-126">La data Slice attende la convalida prima che venga elaborata.</span><span class="sxs-lookup"><span data-stu-id="61443-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="61443-127">Ripetere la convalida.</span><span class="sxs-lookup"><span data-stu-id="61443-127">Retry Validation.</span></span>
<span data-ttu-id="61443-128">Data Factory ritenta la convalida della sezione.</span><span class="sxs-lookup"><span data-stu-id="61443-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="61443-129">Convalida non riuscita.</span><span class="sxs-lookup"><span data-stu-id="61443-129">Failed Validation.</span></span>
<span data-ttu-id="61443-130">La convalida della sezione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="61443-130">Validation of the slice failed.</span></span>
<span data-ttu-id="61443-131">Per ognuna delle sezioni, è possibile visualizzare altre informazioni sull'esecuzione che produce la sezione usando il cmdlet Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="61443-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="61443-132">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61443-132">EXAMPLES</span></span>

### <span data-ttu-id="61443-133">Esempio 1: recuperare le fette di dati per un DataSet</span><span class="sxs-lookup"><span data-stu-id="61443-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="61443-134">Questo comando consente di ottenere tutte le fette di dati per il DataSet denominato WikiAggregatedData nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="61443-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="61443-135">Il comando ottiene le sezioni prodotte dopo il tempo specificato dal parametro StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="61443-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="61443-136">Il codice di esempio seguente imposta la disponibilità per questo DataSet ogni ora nel file JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="61443-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="61443-137">disponibilità: {periodo: "hour", periodMultiplier: 1} alcuni dei risultati sono pronti e altri sono PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="61443-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="61443-138">Le sezioni pronte sono già state eseguite.</span><span class="sxs-lookup"><span data-stu-id="61443-138">Ready slices have already run.</span></span>
<span data-ttu-id="61443-139">Le sezioni in sospeso sono in attesa di esecuzione alla fine di ogni ora nell'intervallo specificato dal cmdlet Set-AzDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="61443-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="61443-140">In questo esempio, i periodi di inizio e di fine per la pipeline e la sezione hanno un valore di un giorno (24 ore).</span><span class="sxs-lookup"><span data-stu-id="61443-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="61443-141">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="61443-141">Example 2</span></span>

<span data-ttu-id="61443-142">Ottiene le fette di dati per un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="61443-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="61443-143">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="61443-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="61443-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61443-144">PARAMETERS</span></span>

### <span data-ttu-id="61443-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="61443-145">-DataFactory</span></span>
<span data-ttu-id="61443-146">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="61443-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="61443-147">Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61443-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61443-148">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="61443-148">-DataFactoryName</span></span>
<span data-ttu-id="61443-149">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="61443-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="61443-150">Questo cmdlet consente di ottenere le sezioni che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61443-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61443-151">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="61443-151">-DatasetName</span></span>
<span data-ttu-id="61443-152">Specifica il nome del DataSet per cui questo cmdlet ottiene le sezioni.</span><span class="sxs-lookup"><span data-stu-id="61443-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="61443-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61443-153">-DefaultProfile</span></span>
<span data-ttu-id="61443-154">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61443-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61443-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="61443-155">-EndDateTime</span></span>
<span data-ttu-id="61443-156">Specifica la fine di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="61443-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="61443-157">Questo cmdlet ottiene le sezioni prodotte prima del tempo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61443-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="61443-158">Per altre informazioni sugli oggetti **DateTime** , digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="61443-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="61443-159">*EndDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) l'identificatore del fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="61443-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="61443-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61443-160">-ResourceGroupName</span></span>
<span data-ttu-id="61443-161">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="61443-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61443-162">Questo cmdlet ottiene le sezioni che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61443-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="61443-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="61443-163">-StartDateTime</span></span>
<span data-ttu-id="61443-164">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="61443-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="61443-165">Questo cmdlet ottiene le sezioni prodotte dopo il tempo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61443-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="61443-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61443-166">CommonParameters</span></span>
<span data-ttu-id="61443-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61443-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61443-168">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61443-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61443-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61443-169">INPUTS</span></span>

### <span data-ttu-id="61443-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="61443-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="61443-171">System. String</span><span class="sxs-lookup"><span data-stu-id="61443-171">System.String</span></span>

## <span data-ttu-id="61443-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61443-172">OUTPUTS</span></span>

### <span data-ttu-id="61443-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="61443-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="61443-174">Note</span><span class="sxs-lookup"><span data-stu-id="61443-174">NOTES</span></span>
* <span data-ttu-id="61443-175">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="61443-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61443-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61443-176">RELATED LINKS</span></span>

[<span data-ttu-id="61443-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="61443-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="61443-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="61443-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="61443-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="61443-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


