---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: d4ec2865f0a0efcc4a306d0614df1c27adddc5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520567"
---
# <span data-ttu-id="bb60a-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="bb60a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb60a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb60a-103">Interrompe un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="bb60a-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb60a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb60a-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb60a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb60a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb60a-106">Il cmdlet **Stop-AzureRmStreamAnalyticsJob** arresta in modo asincrono un processo di analisi del flusso da eseguire in Azure e rilascia le risorse che erano in uso.</span><span class="sxs-lookup"><span data-stu-id="bb60a-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="bb60a-107">La definizione del processo e i metadati restano disponibili all'interno dell'abbonamento tramite le API di gestione e portale di Azure, in modo che il processo possa essere modificato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="bb60a-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="bb60a-108">Non verrà addebitato un processo nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="bb60a-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="bb60a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb60a-109">EXAMPLES</span></span>

### <span data-ttu-id="bb60a-110">ESEMPIO 1: arrestare un processo in uso</span><span class="sxs-lookup"><span data-stu-id="bb60a-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="bb60a-111">Questo comando Arresta il processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bb60a-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="bb60a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb60a-112">PARAMETERS</span></span>

### <span data-ttu-id="bb60a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb60a-113">-DefaultProfile</span></span>
<span data-ttu-id="bb60a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb60a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb60a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb60a-115">-Name</span></span>
<span data-ttu-id="bb60a-116">Specifica il nome del processo di analisi di Azure Stream da interrompere.</span><span class="sxs-lookup"><span data-stu-id="bb60a-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="bb60a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb60a-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb60a-118">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="bb60a-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="bb60a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb60a-119">CommonParameters</span></span>
<span data-ttu-id="bb60a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb60a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb60a-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb60a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb60a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb60a-122">INPUTS</span></span>

### <span data-ttu-id="bb60a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bb60a-123">System.String</span></span>

## <span data-ttu-id="bb60a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb60a-124">OUTPUTS</span></span>

### <span data-ttu-id="bb60a-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb60a-125">System.Boolean</span></span>

## <span data-ttu-id="bb60a-126">Note</span><span class="sxs-lookup"><span data-stu-id="bb60a-126">NOTES</span></span>

## <span data-ttu-id="bb60a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb60a-127">RELATED LINKS</span></span>

[<span data-ttu-id="bb60a-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="bb60a-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="bb60a-130">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-130">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="bb60a-131">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-131">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="bb60a-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb60a-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


