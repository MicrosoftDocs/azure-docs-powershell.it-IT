---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200615"
---
# <span data-ttu-id="bb688-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb688-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="bb688-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb688-102">SYNOPSIS</span></span>
<span data-ttu-id="bb688-103">Avvia un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="bb688-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="bb688-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb688-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb688-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb688-105">DESCRIPTION</span></span>
<span data-ttu-id="bb688-106">Il cmdlet **Start-AzStreamAnalyticsJob** distribuisce in modo asincrono e avvia un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="bb688-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="bb688-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb688-107">EXAMPLES</span></span>

### <span data-ttu-id="bb688-108">Esempio 1: avviare un processo di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="bb688-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="bb688-109">Questo comando avvia il processo StreamingJob e specifica che il flusso di eventi di output dovrebbe iniziare in timestamp 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="bb688-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="bb688-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb688-110">PARAMETERS</span></span>

### <span data-ttu-id="bb688-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb688-111">-DefaultProfile</span></span>
<span data-ttu-id="bb688-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb688-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb688-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb688-113">-Name</span></span>
<span data-ttu-id="bb688-114">Specifica il nome del processo di analisi di Azure Stream da avviare.</span><span class="sxs-lookup"><span data-stu-id="bb688-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="bb688-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="bb688-115">-OutputStartMode</span></span>
<span data-ttu-id="bb688-116">Specifica la modalità di avvio per il processo.</span><span class="sxs-lookup"><span data-stu-id="bb688-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="bb688-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bb688-117">Valid values are:</span></span> 
- <span data-ttu-id="bb688-118">JobStartTime: questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare quando il processo viene avviato.</span><span class="sxs-lookup"><span data-stu-id="bb688-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="bb688-119">CustomTime-questo valore indica che il punto di partenza del flusso di eventi di output deve iniziare in corrispondenza di un'ora personalizzata specificata nel parametro *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="bb688-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="bb688-120">LastOutputEventTime: questo valore indica che il punto di partenza del flusso di eventi di output dovrebbe iniziare dall'ultimo tempo di output dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bb688-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="bb688-121">Se la proprietà è assente, il valore predefinito è JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="bb688-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="bb688-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="bb688-122">-OutputStartTime</span></span>
<span data-ttu-id="bb688-123">Specifica l'ora di inizio dell'output.</span><span class="sxs-lookup"><span data-stu-id="bb688-123">Specifies the output start time.</span></span>
<span data-ttu-id="bb688-124">Questo valore è un indicatore di data e ora formattato ISO-8601 che indica il punto di partenza del flusso di eventi di output oppure $Null per indicare che il flusso di eventi di output verrà avviato ogni volta che si avvia il processo di flusso.</span><span class="sxs-lookup"><span data-stu-id="bb688-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="bb688-125">Questa proprietà deve avere un valore se *OutputStartMode* è impostato su CustomTime.</span><span class="sxs-lookup"><span data-stu-id="bb688-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="bb688-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb688-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb688-127">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="bb688-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="bb688-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb688-128">CommonParameters</span></span>
<span data-ttu-id="bb688-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb688-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb688-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb688-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb688-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb688-131">INPUTS</span></span>

### <span data-ttu-id="bb688-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bb688-132">System.String</span></span>

### <span data-ttu-id="bb688-133">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb688-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bb688-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb688-134">OUTPUTS</span></span>

### <span data-ttu-id="bb688-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb688-135">System.Boolean</span></span>

## <span data-ttu-id="bb688-136">Note</span><span class="sxs-lookup"><span data-stu-id="bb688-136">NOTES</span></span>

## <span data-ttu-id="bb688-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb688-137">RELATED LINKS</span></span>

[<span data-ttu-id="bb688-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb688-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb688-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb688-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb688-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb688-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb688-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb688-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

