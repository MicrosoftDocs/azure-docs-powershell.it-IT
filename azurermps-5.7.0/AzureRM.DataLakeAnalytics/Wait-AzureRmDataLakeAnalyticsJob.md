---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521055"
---
# <span data-ttu-id="4e931-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e931-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4e931-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e931-102">SYNOPSIS</span></span>
<span data-ttu-id="4e931-103">Attende il completamento di un processo.</span><span class="sxs-lookup"><span data-stu-id="4e931-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e931-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e931-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e931-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e931-105">DESCRIPTION</span></span>
<span data-ttu-id="4e931-106">Il cmdlet **wait-AzureRmDataLakeAnalyticsJob** attende il completamento di un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e931-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="4e931-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e931-107">EXAMPLES</span></span>

### <span data-ttu-id="4e931-108">Esempio 1: attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="4e931-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="4e931-109">Il comando seguente attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="4e931-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="4e931-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e931-110">PARAMETERS</span></span>

### <span data-ttu-id="4e931-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4e931-111">-Account</span></span>
<span data-ttu-id="4e931-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="4e931-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e931-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e931-113">-DefaultProfile</span></span>
<span data-ttu-id="4e931-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4e931-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e931-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="4e931-115">-JobId</span></span>
<span data-ttu-id="4e931-116">Specifica l'ID del processo per cui attendere.</span><span class="sxs-lookup"><span data-stu-id="4e931-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e931-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4e931-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="4e931-118">Specifica il numero di secondi di attesa prima di uscire dall'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="4e931-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e931-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4e931-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="4e931-120">Specificare il numero di secondi che intercorrono tra ogni controllo dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="4e931-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e931-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e931-121">CommonParameters</span></span>
<span data-ttu-id="4e931-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e931-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e931-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e931-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e931-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e931-124">INPUTS</span></span>

### <span data-ttu-id="4e931-125">GUID</span><span class="sxs-lookup"><span data-stu-id="4e931-125">Guid</span></span>
<span data-ttu-id="4e931-126">Il parametro "JobId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4e931-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="4e931-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e931-127">OUTPUTS</span></span>

### <span data-ttu-id="4e931-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="4e931-128">JobInformation</span></span>
<span data-ttu-id="4e931-129">Dettagli del processo finale per il processo completato.</span><span class="sxs-lookup"><span data-stu-id="4e931-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="4e931-130">Note</span><span class="sxs-lookup"><span data-stu-id="4e931-130">NOTES</span></span>

## <span data-ttu-id="4e931-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e931-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e931-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e931-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4e931-133">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e931-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4e931-134">Invia-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e931-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


