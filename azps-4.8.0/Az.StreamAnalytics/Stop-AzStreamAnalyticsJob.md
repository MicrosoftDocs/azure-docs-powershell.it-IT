---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188696"
---
# <span data-ttu-id="44f1e-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="44f1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="44f1e-103">Interrompe un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="44f1e-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="44f1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44f1e-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44f1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="44f1e-106">Il cmdlet **Stop-AzStreamAnalyticsJob** arresta in modo asincrono un processo di analisi del flusso da eseguire in Azure e rilascia le risorse che erano in uso.</span><span class="sxs-lookup"><span data-stu-id="44f1e-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="44f1e-107">La definizione del processo e i metadati restano disponibili all'interno dell'abbonamento tramite le API di gestione e portale di Azure, in modo che il processo possa essere modificato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="44f1e-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="44f1e-108">Non verrà addebitato un processo nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="44f1e-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="44f1e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44f1e-109">EXAMPLES</span></span>

### <span data-ttu-id="44f1e-110">Esempio 1: arrestare un processo in uso</span><span class="sxs-lookup"><span data-stu-id="44f1e-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="44f1e-111">Questo comando Arresta il processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="44f1e-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="44f1e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44f1e-112">PARAMETERS</span></span>

### <span data-ttu-id="44f1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f1e-113">-DefaultProfile</span></span>
<span data-ttu-id="44f1e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44f1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f1e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="44f1e-115">-Name</span></span>
<span data-ttu-id="44f1e-116">Specifica il nome del processo di analisi di Azure Stream da interrompere.</span><span class="sxs-lookup"><span data-stu-id="44f1e-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="44f1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="44f1e-118">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="44f1e-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="44f1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f1e-119">CommonParameters</span></span>
<span data-ttu-id="44f1e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f1e-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f1e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f1e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44f1e-122">INPUTS</span></span>

### <span data-ttu-id="44f1e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="44f1e-123">System.String</span></span>

## <span data-ttu-id="44f1e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44f1e-124">OUTPUTS</span></span>

### <span data-ttu-id="44f1e-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44f1e-125">System.Boolean</span></span>

## <span data-ttu-id="44f1e-126">Note</span><span class="sxs-lookup"><span data-stu-id="44f1e-126">NOTES</span></span>

## <span data-ttu-id="44f1e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44f1e-127">RELATED LINKS</span></span>

[<span data-ttu-id="44f1e-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="44f1e-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="44f1e-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="44f1e-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="44f1e-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="44f1e-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

