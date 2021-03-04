---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 009f7033b7ecfe26e314a105d0bf88a7433962c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954749"
---
# <span data-ttu-id="8e1a8-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="8e1a8-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="8e1a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1a8-103">Ottiene informazioni sulle finestre delle attività associate a un data factory.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="8e1a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e1a8-104">SYNTAX</span></span>

### <span data-ttu-id="8e1a8-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="8e1a8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1a8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e1a8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e1a8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e1a8-107">DESCRIPTION</span></span>
<span data-ttu-id="8e1a8-108">Il cmdlet **Get-AzDataActivityActivityWindow** ottiene informazioni sulle finestre di attività associate a un data factory.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="8e1a8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e1a8-109">EXAMPLES</span></span>

### <span data-ttu-id="8e1a8-110">Esempio 1: Ottenere le finestre delle attività associate a un data factory</span><span class="sxs-lookup"><span data-stu-id="8e1a8-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="8e1a8-111">Questo comando recupera informazioni su tutte le finestre di attività associate al data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="8e1a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e1a8-112">PARAMETERS</span></span>

### <span data-ttu-id="8e1a8-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="8e1a8-113">-ActivityName</span></span>
<span data-ttu-id="8e1a8-114">Specifica il nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="8e1a8-115">Questo cmdlet ottiene le finestre delle attività per l'attività specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e1a8-116">-DataFactory</span></span>
<span data-ttu-id="8e1a8-117">Specifica un **oggetto PSDataFactory** restituito da un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="8e1a8-118">Questo cmdlet ottiene le finestre delle attività che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e1a8-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e1a8-119">-DataFactoryName</span></span>
<span data-ttu-id="8e1a8-120">Specifica il nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="8e1a8-121">Questo cmdlet ottiene le finestre delle attività che appartengono al data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e1a8-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="8e1a8-122">-DatasetName</span></span>
<span data-ttu-id="8e1a8-123">Specifica il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="8e1a8-124">Questo cmdlet recupera le finestre delle attività che appartengono al set di dati specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1a8-125">-DefaultProfile</span></span>
<span data-ttu-id="8e1a8-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8e1a8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e1a8-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="8e1a8-127">-Filter</span></span>
<span data-ttu-id="8e1a8-128">Specifica la finestra dell'attività espressa con la grammatica del filtro di Ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="8e1a8-129">Per informazioni sulla grammatica, vedere la sintassi delle espressioni OData per la ricerca di Azure https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="8e1a8-130">L'elenco delle finestre delle attività viene filtrato in base alla stringa di ricerca specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="8e1a8-131">-OrderBy</span></span>
<span data-ttu-id="8e1a8-132">Specifica di ordinare la risposta in base a uno dei parametri dell'elenco della finestra delle attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="8e1a8-133">Si tratta di un elenco di proprietà separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="8e1a8-134">Ad esempio: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="8e1a8-135">Per impostazione predefinita, l'ordine è crescente.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="8e1a8-136">Specificare DESC se si vuole ordinare l'elenco in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8e1a8-137">-PipelineName</span></span>
<span data-ttu-id="8e1a8-138">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="8e1a8-139">Questo cmdlet ottiene le finestre delle attività che appartengono alla pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1a8-140">-ResourceGroupName</span></span>
<span data-ttu-id="8e1a8-141">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="8e1a8-142">Questo cmdlet recupera le finestre delle attività che appartengono al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e1a8-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="8e1a8-143">-RunEnd</span></span>
<span data-ttu-id="8e1a8-144">Specifica l'ora di fine della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="8e1a8-145">Questo cmdlet ottiene le finestre delle attività i cui tempi di esecuzione *rientrano tra RunStart* e *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="8e1a8-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="8e1a8-146">-RunStart</span></span>
<span data-ttu-id="8e1a8-147">Specifica l'ora di inizio della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="8e1a8-148">Questo cmdlet ottiene le finestre delle attività i cui tempi di esecuzione *rientrano tra RunStart* e *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="8e1a8-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-149">-In alto</span><span class="sxs-lookup"><span data-stu-id="8e1a8-149">-Top</span></span>
<span data-ttu-id="8e1a8-150">Specifica il numero massimo di finestre di attività restituite da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="8e1a8-151">-WindowEnd</span></span>
<span data-ttu-id="8e1a8-152">Specifica l'ora di fine della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="8e1a8-153">Questo cmdlet ottiene finestre di attività con orari compresi tra *l'ora WindowStart* *e l'ora WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="8e1a8-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="8e1a8-154">-WindowStart</span></span>
<span data-ttu-id="8e1a8-155">Specifica l'ora di inizio della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="8e1a8-156">Questo cmdlet ottiene finestre di attività con orari compresi tra *l'ora WindowStart* *e l'ora WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="8e1a8-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="8e1a8-157">-WindowState</span></span>
<span data-ttu-id="8e1a8-158">Specifica lo stato della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="8e1a8-159">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="8e1a8-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e1a8-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8e1a8-160">None</span></span>
- <span data-ttu-id="8e1a8-161">In attesa</span><span class="sxs-lookup"><span data-stu-id="8e1a8-161">Waiting</span></span>
- <span data-ttu-id="8e1a8-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="8e1a8-162">InProgress</span></span>
- <span data-ttu-id="8e1a8-163">Pronto</span><span class="sxs-lookup"><span data-stu-id="8e1a8-163">Ready</span></span>
- <span data-ttu-id="8e1a8-164">Operazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="8e1a8-164">Failed</span></span>
- <span data-ttu-id="8e1a8-165">Ignorato Questo cmdlet recupera le finestre delle attività nello stato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="8e1a8-166">-WindowSubstate</span></span>
<span data-ttu-id="8e1a8-167">Specifica la sottostate della finestra dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="8e1a8-168">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="8e1a8-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e1a8-169">Annullato</span><span class="sxs-lookup"><span data-stu-id="8e1a8-169">Canceled</span></span>
- <span data-ttu-id="8e1a8-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="8e1a8-170">timedOut</span></span>
- <span data-ttu-id="8e1a8-171">La convalida di questo cmdlet recupera le finestre delle attività nella sottostate specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1a8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1a8-172">CommonParameters</span></span>
<span data-ttu-id="8e1a8-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1a8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1a8-174">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1a8-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1a8-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e1a8-175">INPUTS</span></span>

### <span data-ttu-id="8e1a8-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8e1a8-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8e1a8-177">System.String</span><span class="sxs-lookup"><span data-stu-id="8e1a8-177">System.String</span></span>

### <span data-ttu-id="8e1a8-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e1a8-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e1a8-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e1a8-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8e1a8-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e1a8-180">OUTPUTS</span></span>

### <span data-ttu-id="8e1a8-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="8e1a8-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="8e1a8-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e1a8-182">NOTES</span></span>

## <span data-ttu-id="8e1a8-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e1a8-183">RELATED LINKS</span></span>

[<span data-ttu-id="8e1a8-184">Cmdlet di Azure Data Factories</span><span class="sxs-lookup"><span data-stu-id="8e1a8-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


