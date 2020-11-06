---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507828"
---
# <span data-ttu-id="f7732-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="f7732-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7732-102">SYNOPSIS</span></span>
<span data-ttu-id="f7732-103">Interrompe un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="f7732-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7732-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7732-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7732-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7732-105">DESCRIPTION</span></span>
<span data-ttu-id="f7732-106">Il cmdlet **Stop-AzureRmStreamAnalyticsJob** arresta in modo asincrono un processo di analisi del flusso da eseguire in Azure e rilascia le risorse che erano in uso.</span><span class="sxs-lookup"><span data-stu-id="f7732-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="f7732-107">La definizione del processo e i metadati restano disponibili all'interno dell'abbonamento tramite le API di gestione e portale di Azure, in modo che il processo possa essere modificato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="f7732-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="f7732-108">Non verrà addebitato un processo nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="f7732-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="f7732-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7732-109">EXAMPLES</span></span>

### <span data-ttu-id="f7732-110">ESEMPIO 1: arrestare un processo in uso</span><span class="sxs-lookup"><span data-stu-id="f7732-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="f7732-111">Questo comando Arresta il processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f7732-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="f7732-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7732-112">PARAMETERS</span></span>

### <span data-ttu-id="f7732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7732-113">-DefaultProfile</span></span>
<span data-ttu-id="f7732-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7732-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7732-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7732-115">-Name</span></span>
<span data-ttu-id="f7732-116">Specifica il nome del processo di analisi di Azure Stream da interrompere.</span><span class="sxs-lookup"><span data-stu-id="f7732-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7732-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7732-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7732-118">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="f7732-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7732-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7732-119">CommonParameters</span></span>
<span data-ttu-id="f7732-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7732-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7732-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7732-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7732-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7732-122">INPUTS</span></span>

### <span data-ttu-id="f7732-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f7732-123">None</span></span>
<span data-ttu-id="f7732-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f7732-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7732-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7732-125">OUTPUTS</span></span>

### <span data-ttu-id="f7732-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7732-126">System.Object</span></span>

## <span data-ttu-id="f7732-127">Note</span><span class="sxs-lookup"><span data-stu-id="f7732-127">NOTES</span></span>

## <span data-ttu-id="f7732-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7732-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7732-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7732-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7732-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7732-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7732-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7732-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


