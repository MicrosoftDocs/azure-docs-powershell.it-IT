---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: 77ca77322cec186878b327bcafa9fce626a99c02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515435"
---
# <span data-ttu-id="274c5-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="274c5-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="274c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="274c5-102">SYNOPSIS</span></span>
<span data-ttu-id="274c5-103">Viene eseguita per una sezione di dati di un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="274c5-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="274c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="274c5-104">SYNTAX</span></span>

### <span data-ttu-id="274c5-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="274c5-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="274c5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="274c5-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="274c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="274c5-107">DESCRIPTION</span></span>
<span data-ttu-id="274c5-108">Il cmdlet **Get-AzureRmDataFactoryRun** Ottiene l'esecuzione di una sezione di dati di un DataSet in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="274c5-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="274c5-109">Un DataSet in una data factory è costituito da sezioni nell'asse temporale.</span><span class="sxs-lookup"><span data-stu-id="274c5-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="274c5-110">La larghezza di una sezione viene determinata dalla pianificazione, ogni ora o ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="274c5-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="274c5-111">Un'esecuzione è un'unità di elaborazione per una sezione.</span><span class="sxs-lookup"><span data-stu-id="274c5-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="274c5-112">Potrebbero essere presenti una o più esecuzioni per una sezione in caso di tentativi o in caso di rieseguire la sezione a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="274c5-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="274c5-113">Una fetta viene identificata dall'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="274c5-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="274c5-114">Per ottenere l'ora di inizio di una sezione, usare il cmdlet Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="274c5-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="274c5-115">Ad esempio, per ottenere una corsa per la sezione seguente, usare l'ora di inizio 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="274c5-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="274c5-116">ResourceGroupName: ADF datafactoryname: SPDataFactory0924 DataSetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM end: 5/3/2014 8:00:00 PM RetryCount: 0 status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="274c5-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="274c5-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="274c5-117">EXAMPLES</span></span>

### <span data-ttu-id="274c5-118">Esempio 1: ottenere un DataSet</span><span class="sxs-lookup"><span data-stu-id="274c5-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="274c5-119">Questo comando consente di ottenere tutte le esecuzioni per le sezioni del DataSet denominato DAWikiAggregatedData nella data factory denominata WikiADF che iniziano dalle 4 PM GMT in 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="274c5-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="274c5-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="274c5-120">PARAMETERS</span></span>

### <span data-ttu-id="274c5-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="274c5-121">-DataFactory</span></span>
<span data-ttu-id="274c5-122">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="274c5-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="274c5-123">Questo cmdlet viene eseguito per le sezioni che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="274c5-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="274c5-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="274c5-124">-DataFactoryName</span></span>
<span data-ttu-id="274c5-125">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="274c5-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="274c5-126">Questo cmdlet viene eseguito per le sezioni che appartengono alla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="274c5-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="274c5-127">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="274c5-127">-DatasetName</span></span>
<span data-ttu-id="274c5-128">Specifica il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="274c5-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="274c5-129">Questo cmdlet viene eseguito per le sezioni che appartengono al set di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="274c5-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="274c5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274c5-130">-DefaultProfile</span></span>
<span data-ttu-id="274c5-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="274c5-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="274c5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274c5-132">-ResourceGroupName</span></span>
<span data-ttu-id="274c5-133">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="274c5-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="274c5-134">Questo cmdlet ottiene l'esecuzione di Factory per le sezioni che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="274c5-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="274c5-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="274c5-135">-StartDateTime</span></span>
<span data-ttu-id="274c5-136">Specifica l'inizio di un periodo di tempo come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="274c5-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="274c5-137">Questo cmdlet viene eseguito per le fette di dati che corrispondono a questo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="274c5-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="274c5-138">*StartDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) l'identificatore del fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="274c5-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="274c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274c5-139">CommonParameters</span></span>
<span data-ttu-id="274c5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274c5-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274c5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274c5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="274c5-142">INPUTS</span></span>

### <span data-ttu-id="274c5-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="274c5-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="274c5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="274c5-144">System.String</span></span>

## <span data-ttu-id="274c5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="274c5-145">OUTPUTS</span></span>

### <span data-ttu-id="274c5-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="274c5-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="274c5-147">Note</span><span class="sxs-lookup"><span data-stu-id="274c5-147">NOTES</span></span>
* <span data-ttu-id="274c5-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="274c5-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="274c5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="274c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="274c5-150">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="274c5-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)

