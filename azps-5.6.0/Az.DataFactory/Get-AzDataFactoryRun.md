---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: 2dbab7978716d6bb960c1804abf9e86246571e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975326"
---
# <span data-ttu-id="5ccf0-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="5ccf0-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="5ccf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ccf0-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccf0-103">Viene eseguita per una sezione di dati di un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="5ccf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ccf0-104">SYNTAX</span></span>

### <span data-ttu-id="5ccf0-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5ccf0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ccf0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5ccf0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ccf0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ccf0-107">DESCRIPTION</span></span>
<span data-ttu-id="5ccf0-108">Il cmdlet **Get-AzDataFactoryRun** ottiene le esecuzioni per una sezione di dati di un set di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="5ccf0-109">Un set di dati in un data factory è costituito da sezioni sull'asse temporale.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="5ccf0-110">La larghezza di una sezione dipende dalla pianificazione, ogni ora o ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="5ccf0-111">Un'esecuzione è un'unità di elaborazione per una sezione.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="5ccf0-112">Potrebbero essere presenti una o più esecuzioni per una sezione in caso di tentativi o nel caso in cui si esegui di nuovo la sezione a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="5ccf0-113">Una sezione è identificata dall'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="5ccf0-114">Per ottenere l'ora di inizio di una sezione, usare Get-AzDataFactorySlice cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="5ccf0-115">Ad esempio, per ottenere un'esecuzione per la sezione seguente, usare l'ora di inizio 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="5ccf0-116">ResourceGroupName : ADF DataEffectName : SPDataEffect0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 02/05/2014 8:00:00 PM End : 3/5/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span><span class="sxs-lookup"><span data-stu-id="5ccf0-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="5ccf0-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ccf0-117">EXAMPLES</span></span>

### <span data-ttu-id="5ccf0-118">Esempio 1: Ottenere un set di dati</span><span class="sxs-lookup"><span data-stu-id="5ccf0-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="5ccf0-119">Questo comando viene eseguito per sezioni del set di dati denominato DAWikiAggregatedData nel data factory denominato WikiADF che inizia dalle 16:00 del 21/05/2014.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="5ccf0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ccf0-120">PARAMETERS</span></span>

### <span data-ttu-id="5ccf0-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5ccf0-121">-DataFactory</span></span>
<span data-ttu-id="5ccf0-122">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5ccf0-123">Questo cmdlet viene eseguito per le sezioni che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ccf0-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5ccf0-124">-DataFactoryName</span></span>
<span data-ttu-id="5ccf0-125">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5ccf0-126">Questo cmdlet viene eseguito per le sezioni che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ccf0-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="5ccf0-127">-DatasetName</span></span>
<span data-ttu-id="5ccf0-128">Specifica il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="5ccf0-129">Questo cmdlet viene eseguito per le sezioni che appartengono al set di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ccf0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccf0-130">-DefaultProfile</span></span>
<span data-ttu-id="5ccf0-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5ccf0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ccf0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccf0-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ccf0-133">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5ccf0-134">Questo cmdlet esegue il factory per le sezioni appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ccf0-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="5ccf0-135">-StartDateTime</span></span>
<span data-ttu-id="5ccf0-136">Specifica l'inizio di un periodo di tempo come **oggetto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="5ccf0-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="5ccf0-137">Questo cmdlet viene eseguito per le sezioni di dati che corrispondono a questo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="5ccf0-138">*StartDateTime* deve essere specificato nel formato ISO8601, come negli esempi seguenti: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (ora solare Pacifico) Il designatore del fuso orario predefinito è UTC.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="5ccf0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccf0-139">CommonParameters</span></span>
<span data-ttu-id="5ccf0-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccf0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccf0-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccf0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccf0-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ccf0-142">INPUTS</span></span>

### <span data-ttu-id="5ccf0-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ccf0-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5ccf0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5ccf0-144">System.String</span></span>

## <span data-ttu-id="5ccf0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ccf0-145">OUTPUTS</span></span>

### <span data-ttu-id="5ccf0-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="5ccf0-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="5ccf0-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ccf0-147">NOTES</span></span>
* <span data-ttu-id="5ccf0-148">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="5ccf0-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ccf0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ccf0-149">RELATED LINKS</span></span>

[<span data-ttu-id="5ccf0-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="5ccf0-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


