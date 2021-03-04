---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: f735dc3f213069c1ecf5bbae9d1d5cf24dda98a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955950"
---
# <span data-ttu-id="d0b60-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d0b60-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d0b60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b60-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b60-103">Attende il completamento di un processo.</span><span class="sxs-lookup"><span data-stu-id="d0b60-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="d0b60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0b60-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0b60-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0b60-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b60-106">Il cmdlet **Wait-AzDataLakeAnalyticsJob** attende il completamento di un processo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d0b60-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="d0b60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0b60-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b60-108">Esempio 1: Attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="d0b60-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="d0b60-109">Il comando seguente attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="d0b60-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="d0b60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b60-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b60-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d0b60-111">-Account</span></span>
<span data-ttu-id="d0b60-112">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d0b60-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d0b60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b60-113">-DefaultProfile</span></span>
<span data-ttu-id="d0b60-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d0b60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0b60-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="d0b60-115">-JobId</span></span>
<span data-ttu-id="d0b60-116">Specifica l'ID del processo di attesa.</span><span class="sxs-lookup"><span data-stu-id="d0b60-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="d0b60-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d0b60-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="d0b60-118">Specifica il numero di secondi di attesa prima di uscire dall'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="d0b60-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="d0b60-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d0b60-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="d0b60-120">Specificare il numero di secondi trascorsi tra ogni controllo dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="d0b60-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="d0b60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b60-121">CommonParameters</span></span>
<span data-ttu-id="d0b60-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b60-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b60-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b60-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0b60-124">INPUTS</span></span>

### <span data-ttu-id="d0b60-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d0b60-125">System.String</span></span>

### <span data-ttu-id="d0b60-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d0b60-126">System.Guid</span></span>

### <span data-ttu-id="d0b60-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d0b60-127">System.Int32</span></span>

## <span data-ttu-id="d0b60-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0b60-128">OUTPUTS</span></span>

### <span data-ttu-id="d0b60-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="d0b60-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="d0b60-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0b60-130">NOTES</span></span>

## <span data-ttu-id="d0b60-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0b60-131">RELATED LINKS</span></span>

[<span data-ttu-id="d0b60-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d0b60-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d0b60-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d0b60-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d0b60-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d0b60-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


