---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685692"
---
# <span data-ttu-id="51a6e-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="51a6e-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="51a6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="51a6e-103">Ottiene informazioni sulle finestre delle attività associate a una data factory.</span><span class="sxs-lookup"><span data-stu-id="51a6e-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a6e-104">SYNTAX</span></span>

### <span data-ttu-id="51a6e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51a6e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51a6e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="51a6e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51a6e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="51a6e-108">Il cmdlet **Get-AzureRmDataFactoryActivityWindow** ottiene informazioni sulle finestre attività associate a una data factory.</span><span class="sxs-lookup"><span data-stu-id="51a6e-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="51a6e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="51a6e-110">Esempio 1: ottenere le finestre attività associate a una data factory</span><span class="sxs-lookup"><span data-stu-id="51a6e-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="51a6e-111">Questo comando consente di ottenere informazioni su tutte le finestre di attività associate alla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="51a6e-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="51a6e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51a6e-112">PARAMETERS</span></span>

### <span data-ttu-id="51a6e-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="51a6e-113">-ActivityName</span></span>
<span data-ttu-id="51a6e-114">Specifica il nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="51a6e-115">Questo cmdlet ottiene le finestre delle attività per l'attività specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="51a6e-116">-DataFactory</span></span>
<span data-ttu-id="51a6e-117">Specifica un oggetto **PSDataFactory** restituito da un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a6e-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="51a6e-118">Questo cmdlet consente di ottenere le finestre delle attività che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="51a6e-119">-DataFactoryName</span></span>
<span data-ttu-id="51a6e-120">Specifica il nome della data factory.</span><span class="sxs-lookup"><span data-stu-id="51a6e-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="51a6e-121">Questo cmdlet consente di ottenere le finestre delle attività che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="51a6e-122">-DatasetName</span></span>
<span data-ttu-id="51a6e-123">Specifica il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="51a6e-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="51a6e-124">Questo cmdlet ottiene le finestre delle attività che appartengono al DataSet specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="51a6e-125">-Filter</span></span>
<span data-ttu-id="51a6e-126">Specifica la finestra attività espressa tramite la grammatica del filtro di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="51a6e-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="51a6e-127">Per informazioni sulla grammatica, vedere Sintassi delle espressioni OData per la ricerca https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx in Azure ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="51a6e-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="51a6e-128">L'elenco di Windows attività viene filtrato dalla stringa di ricerca specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="51a6e-129">-OrderBy</span></span>
<span data-ttu-id="51a6e-130">Specifica di ordinare la risposta tramite uno dei parametri dell'elenco delle finestre attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="51a6e-131">Questo è un elenco di proprietà separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="51a6e-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="51a6e-132">Ad esempio: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="51a6e-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="51a6e-133">Per impostazione predefinita, l'ordine è crescente (ASC).</span><span class="sxs-lookup"><span data-stu-id="51a6e-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="51a6e-134">Specificare DESC se si vuole ordinare l'elenco in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="51a6e-134">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="51a6e-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="51a6e-135">-PipelineName</span></span>
<span data-ttu-id="51a6e-136">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="51a6e-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="51a6e-137">Questo cmdlet ottiene le finestre delle attività che appartengono alla pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a6e-138">-ResourceGroupName</span></span>
<span data-ttu-id="51a6e-139">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51a6e-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="51a6e-140">Questo cmdlet ottiene le finestre delle attività che appartengono al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="51a6e-141">-RunEnd</span></span>
<span data-ttu-id="51a6e-142">Specifica l'ora di fine dell'esecuzione della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="51a6e-143">Questo cmdlet ottiene le finestre delle attività di cui i tempi di esecuzione cadono tra *RunStart* e *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="51a6e-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="51a6e-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="51a6e-144">-RunStart</span></span>
<span data-ttu-id="51a6e-145">Specifica l'ora di inizio dell'esecuzione della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="51a6e-146">Questo cmdlet ottiene le finestre delle attività di cui i tempi di esecuzione cadono tra *RunStart* e *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="51a6e-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="51a6e-147">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="51a6e-147">-Top</span></span>
<span data-ttu-id="51a6e-148">Specifica il numero massimo di finestre di attività restituite dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a6e-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="51a6e-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="51a6e-149">-WindowEnd</span></span>
<span data-ttu-id="51a6e-150">Specifica l'ora di fine della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="51a6e-151">Questo cmdlet ottiene le finestre delle attività di cui i tempi cadono tra *WindowStart* e *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="51a6e-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="51a6e-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="51a6e-152">-WindowStart</span></span>
<span data-ttu-id="51a6e-153">Specifica l'ora di inizio della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="51a6e-154">Questo cmdlet ottiene le finestre delle attività di cui i tempi cadono tra *WindowStart* e *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="51a6e-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="51a6e-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="51a6e-155">-WindowState</span></span>
<span data-ttu-id="51a6e-156">Specifica lo stato della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="51a6e-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="51a6e-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51a6e-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51a6e-158">None</span></span>
- <span data-ttu-id="51a6e-159">In attesa</span><span class="sxs-lookup"><span data-stu-id="51a6e-159">Waiting</span></span>
- <span data-ttu-id="51a6e-160">InProgress</span><span class="sxs-lookup"><span data-stu-id="51a6e-160">InProgress</span></span>
- <span data-ttu-id="51a6e-161">Pronto</span><span class="sxs-lookup"><span data-stu-id="51a6e-161">Ready</span></span>
- <span data-ttu-id="51a6e-162">Fallito</span><span class="sxs-lookup"><span data-stu-id="51a6e-162">Failed</span></span>
- <span data-ttu-id="51a6e-163">Ignorato</span><span class="sxs-lookup"><span data-stu-id="51a6e-163">Skipped</span></span>

<span data-ttu-id="51a6e-164">Questo cmdlet ottiene le finestre delle attività che si trovano nello stato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="51a6e-165">-WindowSubstate</span></span>
<span data-ttu-id="51a6e-166">Specifica il substato della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="51a6e-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="51a6e-167">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="51a6e-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51a6e-168">Annullato</span><span class="sxs-lookup"><span data-stu-id="51a6e-168">Canceled</span></span>
- <span data-ttu-id="51a6e-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="51a6e-169">timedOut</span></span>
- <span data-ttu-id="51a6e-170">Convalida</span><span class="sxs-lookup"><span data-stu-id="51a6e-170">Validating</span></span>

<span data-ttu-id="51a6e-171">Questo cmdlet ottiene le finestre delle attività che si trovano nel sottostato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a6e-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a6e-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a6e-172">-DefaultProfile</span></span>
<span data-ttu-id="51a6e-173">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a6e-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51a6e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a6e-174">CommonParameters</span></span>
<span data-ttu-id="51a6e-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a6e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a6e-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a6e-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a6e-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51a6e-177">INPUTS</span></span>

## <span data-ttu-id="51a6e-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a6e-178">OUTPUTS</span></span>

### <span data-ttu-id="51a6e-179">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSActivyWindow, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="51a6e-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="51a6e-180">Note</span><span class="sxs-lookup"><span data-stu-id="51a6e-180">NOTES</span></span>

## <span data-ttu-id="51a6e-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a6e-181">RELATED LINKS</span></span>

[<span data-ttu-id="51a6e-182">Cmdlet di Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="51a6e-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


