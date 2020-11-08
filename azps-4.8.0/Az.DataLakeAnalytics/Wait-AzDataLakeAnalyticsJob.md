---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189102"
---
# <span data-ttu-id="dda10-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dda10-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="dda10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dda10-102">SYNOPSIS</span></span>
<span data-ttu-id="dda10-103">Attende il completamento di un processo.</span><span class="sxs-lookup"><span data-stu-id="dda10-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="dda10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dda10-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dda10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dda10-105">DESCRIPTION</span></span>
<span data-ttu-id="dda10-106">Il cmdlet **wait-AzDataLakeAnalyticsJob** attende il completamento di un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="dda10-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="dda10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dda10-107">EXAMPLES</span></span>

### <span data-ttu-id="dda10-108">Esempio 1: attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="dda10-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="dda10-109">Il comando seguente attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="dda10-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="dda10-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dda10-110">PARAMETERS</span></span>

### <span data-ttu-id="dda10-111">-Account</span><span class="sxs-lookup"><span data-stu-id="dda10-111">-Account</span></span>
<span data-ttu-id="dda10-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="dda10-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda10-113">-DefaultProfile</span></span>
<span data-ttu-id="dda10-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dda10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dda10-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="dda10-115">-JobId</span></span>
<span data-ttu-id="dda10-116">Specifica l'ID del processo per cui attendere.</span><span class="sxs-lookup"><span data-stu-id="dda10-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dda10-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="dda10-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="dda10-118">Specifica il numero di secondi di attesa prima di uscire dall'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="dda10-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda10-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="dda10-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="dda10-120">Specificare il numero di secondi che intercorrono tra ogni controllo dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="dda10-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda10-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda10-121">CommonParameters</span></span>
<span data-ttu-id="dda10-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda10-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda10-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda10-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda10-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dda10-124">INPUTS</span></span>

### <span data-ttu-id="dda10-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dda10-125">System.String</span></span>

### <span data-ttu-id="dda10-126">System. Guid</span><span class="sxs-lookup"><span data-stu-id="dda10-126">System.Guid</span></span>

### <span data-ttu-id="dda10-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dda10-127">System.Int32</span></span>

## <span data-ttu-id="dda10-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dda10-128">OUTPUTS</span></span>

### <span data-ttu-id="dda10-129">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="dda10-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="dda10-130">Note</span><span class="sxs-lookup"><span data-stu-id="dda10-130">NOTES</span></span>

## <span data-ttu-id="dda10-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dda10-131">RELATED LINKS</span></span>

[<span data-ttu-id="dda10-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dda10-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="dda10-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dda10-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="dda10-134">Invia-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dda10-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


