---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298615"
---
# <span data-ttu-id="44eb2-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="44eb2-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="44eb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="44eb2-103">Ottiene informazioni sulle finestre delle attività associate a una data factory.</span><span class="sxs-lookup"><span data-stu-id="44eb2-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="44eb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44eb2-104">SYNTAX</span></span>

### <span data-ttu-id="44eb2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44eb2-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44eb2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="44eb2-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44eb2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44eb2-107">DESCRIPTION</span></span>
<span data-ttu-id="44eb2-108">Il cmdlet **Get-AzDataFactoryActivityWindow** ottiene informazioni sulle finestre attività associate a una data factory.</span><span class="sxs-lookup"><span data-stu-id="44eb2-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="44eb2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44eb2-109">EXAMPLES</span></span>

### <span data-ttu-id="44eb2-110">Esempio 1: ottenere le finestre attività associate a una data factory</span><span class="sxs-lookup"><span data-stu-id="44eb2-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="44eb2-111">Questo comando consente di ottenere informazioni su tutte le finestre di attività associate alla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="44eb2-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="44eb2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44eb2-112">PARAMETERS</span></span>

### <span data-ttu-id="44eb2-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="44eb2-113">-ActivityName</span></span>
<span data-ttu-id="44eb2-114">Specifica il nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="44eb2-115">Questo cmdlet ottiene le finestre delle attività per l'attività specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="44eb2-116">-DataFactory</span></span>
<span data-ttu-id="44eb2-117">Specifica un oggetto **PSDataFactory** restituito da un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44eb2-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="44eb2-118">Questo cmdlet consente di ottenere le finestre delle attività che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="44eb2-119">-DataFactoryName</span></span>
<span data-ttu-id="44eb2-120">Specifica il nome della data factory.</span><span class="sxs-lookup"><span data-stu-id="44eb2-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="44eb2-121">Questo cmdlet consente di ottenere le finestre delle attività che appartengono alla Factory di dati specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="44eb2-122">-DatasetName</span></span>
<span data-ttu-id="44eb2-123">Specifica il nome del set di dati.</span><span class="sxs-lookup"><span data-stu-id="44eb2-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="44eb2-124">Questo cmdlet ottiene le finestre delle attività che appartengono al DataSet specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44eb2-125">-DefaultProfile</span></span>
<span data-ttu-id="44eb2-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="44eb2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44eb2-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="44eb2-127">-Filter</span></span>
<span data-ttu-id="44eb2-128">Specifica la finestra attività espressa tramite la grammatica del filtro di ricerca di Azure.</span><span class="sxs-lookup"><span data-stu-id="44eb2-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="44eb2-129">Per informazioni sulla grammatica, vedere Sintassi delle espressioni OData per la ricerca https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx in Azure ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="44eb2-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="44eb2-130">L'elenco di Windows attività viene filtrato dalla stringa di ricerca specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="44eb2-131">-OrderBy</span></span>
<span data-ttu-id="44eb2-132">Specifica di ordinare la risposta tramite uno dei parametri dell'elenco delle finestre attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="44eb2-133">Questo è un elenco di proprietà separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="44eb2-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="44eb2-134">Ad esempio: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="44eb2-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="44eb2-135">Per impostazione predefinita, l'ordine è crescente (ASC).</span><span class="sxs-lookup"><span data-stu-id="44eb2-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="44eb2-136">Specificare DESC se si vuole ordinare l'elenco in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="44eb2-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="44eb2-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="44eb2-137">-PipelineName</span></span>
<span data-ttu-id="44eb2-138">Specifica il nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="44eb2-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="44eb2-139">Questo cmdlet ottiene le finestre delle attività che appartengono alla pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44eb2-140">-ResourceGroupName</span></span>
<span data-ttu-id="44eb2-141">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44eb2-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="44eb2-142">Questo cmdlet ottiene le finestre delle attività che appartengono al gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="44eb2-143">-RunEnd</span></span>
<span data-ttu-id="44eb2-144">Specifica l'ora di fine dell'esecuzione della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="44eb2-145">Questo cmdlet ottiene le finestre delle attività di cui i tempi di esecuzione cadono tra *RunStart* e *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="44eb2-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="44eb2-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="44eb2-146">-RunStart</span></span>
<span data-ttu-id="44eb2-147">Specifica l'ora di inizio dell'esecuzione della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="44eb2-148">Questo cmdlet ottiene le finestre delle attività di cui i tempi di esecuzione cadono tra *RunStart* e *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="44eb2-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="44eb2-149">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="44eb2-149">-Top</span></span>
<span data-ttu-id="44eb2-150">Specifica il numero massimo di finestre di attività restituite dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44eb2-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="44eb2-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="44eb2-151">-WindowEnd</span></span>
<span data-ttu-id="44eb2-152">Specifica l'ora di fine della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="44eb2-153">Questo cmdlet ottiene le finestre delle attività di cui i tempi cadono tra *WindowStart* e *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="44eb2-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="44eb2-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="44eb2-154">-WindowStart</span></span>
<span data-ttu-id="44eb2-155">Specifica l'ora di inizio della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="44eb2-156">Questo cmdlet ottiene le finestre delle attività di cui i tempi cadono tra *WindowStart* e *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="44eb2-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="44eb2-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="44eb2-157">-WindowState</span></span>
<span data-ttu-id="44eb2-158">Specifica lo stato della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="44eb2-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="44eb2-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44eb2-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44eb2-160">None</span></span>
- <span data-ttu-id="44eb2-161">In attesa</span><span class="sxs-lookup"><span data-stu-id="44eb2-161">Waiting</span></span>
- <span data-ttu-id="44eb2-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="44eb2-162">InProgress</span></span>
- <span data-ttu-id="44eb2-163">Pronto</span><span class="sxs-lookup"><span data-stu-id="44eb2-163">Ready</span></span>
- <span data-ttu-id="44eb2-164">Fallito</span><span class="sxs-lookup"><span data-stu-id="44eb2-164">Failed</span></span>
- <span data-ttu-id="44eb2-165">Ignorato questo cmdlet ottiene le finestre delle attività che si trovano nello stato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="44eb2-166">-WindowSubstate</span></span>
<span data-ttu-id="44eb2-167">Specifica il substato della finestra attività.</span><span class="sxs-lookup"><span data-stu-id="44eb2-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="44eb2-168">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="44eb2-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44eb2-169">Annullato</span><span class="sxs-lookup"><span data-stu-id="44eb2-169">Canceled</span></span>
- <span data-ttu-id="44eb2-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="44eb2-170">timedOut</span></span>
- <span data-ttu-id="44eb2-171">La convalida di questo cmdlet consente di ottenere le finestre delle attività che si trovano nel sottostato specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44eb2-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="44eb2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44eb2-172">CommonParameters</span></span>
<span data-ttu-id="44eb2-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44eb2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44eb2-174">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44eb2-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44eb2-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44eb2-175">INPUTS</span></span>

### <span data-ttu-id="44eb2-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="44eb2-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="44eb2-177">System. String</span><span class="sxs-lookup"><span data-stu-id="44eb2-177">System.String</span></span>

### <span data-ttu-id="44eb2-178">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44eb2-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="44eb2-179">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44eb2-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="44eb2-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44eb2-180">OUTPUTS</span></span>

### <span data-ttu-id="44eb2-181">Microsoft. Azure. Commands. datafactories. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="44eb2-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="44eb2-182">Note</span><span class="sxs-lookup"><span data-stu-id="44eb2-182">NOTES</span></span>

## <span data-ttu-id="44eb2-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44eb2-183">RELATED LINKS</span></span>

[<span data-ttu-id="44eb2-184">Cmdlet di Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="44eb2-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


