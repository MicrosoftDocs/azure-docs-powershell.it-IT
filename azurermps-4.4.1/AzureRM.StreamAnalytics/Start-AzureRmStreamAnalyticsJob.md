---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b012704eebfa9d2c2a868679450cd0231667f585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688599"
---
# <span data-ttu-id="64431-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64431-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="64431-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64431-102">SYNOPSIS</span></span>
<span data-ttu-id="64431-103">Avvia un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="64431-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64431-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64431-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64431-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64431-105">DESCRIPTION</span></span>
<span data-ttu-id="64431-106">Il cmdlet **Start-AzureRmStreamAnalyticsJob** distribuisce in modo asincrono e avvia un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="64431-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="64431-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64431-107">EXAMPLES</span></span>

### <span data-ttu-id="64431-108">ESEMPIO 1: avviare un processo di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="64431-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="64431-109">Questo comando avvia il processo StreamingJob e specifica che il flusso di eventi di output dovrebbe iniziare in timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="64431-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="64431-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64431-110">PARAMETERS</span></span>

### <span data-ttu-id="64431-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="64431-111">-Name</span></span>
<span data-ttu-id="64431-112">Specifica il nome del processo di analisi di Azure Stream da avviare.</span><span class="sxs-lookup"><span data-stu-id="64431-112">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64431-113">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="64431-113">-OutputStartMode</span></span>
<span data-ttu-id="64431-114">Specifica la modalità di avvio per il processo.</span><span class="sxs-lookup"><span data-stu-id="64431-114">Specifies the start mode for the job.</span></span>
<span data-ttu-id="64431-115">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="64431-115">Valid values are:</span></span> 

- <span data-ttu-id="64431-116">JobStartTime: questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare quando il processo viene avviato.</span><span class="sxs-lookup"><span data-stu-id="64431-116">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="64431-117">CustomTime-questo valore indica che il punto di partenza del flusso di eventi di output deve iniziare in corrispondenza di un'ora personalizzata specificata nel parametro *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="64431-117">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="64431-118">--LastOutputEventTime-questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare dall'ultimo tempo di output dell'evento.</span><span class="sxs-lookup"><span data-stu-id="64431-118">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="64431-119">Se la proprietà è assente, il valore predefinito è JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="64431-119">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="64431-120">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="64431-120">-OutputStartTime</span></span>
<span data-ttu-id="64431-121">Specifica l'ora di inizio dell'output.</span><span class="sxs-lookup"><span data-stu-id="64431-121">Specifies the output start time.</span></span>
<span data-ttu-id="64431-122">Questo valore è un indicatore di data e ora formattato ISO-8601 che indica il punto di partenza del flusso di eventi di output oppure $Null per indicare che il flusso di eventi di output verrà avviato ogni volta che si avvia il processo di flusso.</span><span class="sxs-lookup"><span data-stu-id="64431-122">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="64431-123">Questa proprietà deve avere un valore se *OutputStartMode* è impostato su CustomTime.</span><span class="sxs-lookup"><span data-stu-id="64431-123">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64431-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64431-124">-ResourceGroupName</span></span>
<span data-ttu-id="64431-125">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="64431-125">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64431-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64431-126">-DefaultProfile</span></span>
<span data-ttu-id="64431-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64431-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64431-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64431-128">CommonParameters</span></span>
<span data-ttu-id="64431-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64431-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64431-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64431-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64431-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64431-131">INPUTS</span></span>

## <span data-ttu-id="64431-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64431-132">OUTPUTS</span></span>

### <span data-ttu-id="64431-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="64431-133">System.Object</span></span>

## <span data-ttu-id="64431-134">Note</span><span class="sxs-lookup"><span data-stu-id="64431-134">NOTES</span></span>

## <span data-ttu-id="64431-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64431-135">RELATED LINKS</span></span>

[<span data-ttu-id="64431-136">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64431-136">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="64431-137">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64431-137">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="64431-138">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64431-138">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="64431-139">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64431-139">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


