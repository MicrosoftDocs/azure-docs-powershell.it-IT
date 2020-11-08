---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190477"
---
# <span data-ttu-id="5b3a7-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="5b3a7-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="5b3a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3a7-103">Ottiene una pipeline o pipeline dei processi di analisi del lago dati.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="5b3a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b3a7-104">SYNTAX</span></span>

### <span data-ttu-id="5b3a7-105">GetAllInAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b3a7-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b3a7-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="5b3a7-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b3a7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b3a7-107">DESCRIPTION</span></span>
<span data-ttu-id="5b3a7-108">**Get-AzDataLakeAnalyticsJobPipeline** ottiene una pipeline dei processi di analisi di dati di Azure Data Lake specificata o un elenco di pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="5b3a7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b3a7-109">EXAMPLES</span></span>

### <span data-ttu-id="5b3a7-110">Esempio 1: ottenere una pipeline specificata</span><span class="sxs-lookup"><span data-stu-id="5b3a7-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="5b3a7-111">Questo comando ottiene la pipeline specificata con l'ID ' 83cb7ad2-3523-4b82-B909-d478b0d8aea3' nell'account ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="5b3a7-112">Esempio 2: ottenere un elenco di tutte le pipeline nell'account</span><span class="sxs-lookup"><span data-stu-id="5b3a7-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="5b3a7-113">Questo comando ottiene un elenco di tutte le pipeline nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="5b3a7-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="5b3a7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b3a7-114">PARAMETERS</span></span>

### <span data-ttu-id="5b3a7-115">-Account</span><span class="sxs-lookup"><span data-stu-id="5b3a7-115">-Account</span></span>
<span data-ttu-id="5b3a7-116">Nome del nome dell'account di data Lake Analytics in cui si vuole recuperare la pipeline dei processi.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="5b3a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3a7-117">-DefaultProfile</span></span>
<span data-ttu-id="5b3a7-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b3a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b3a7-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="5b3a7-119">-PipelineId</span></span>
<span data-ttu-id="5b3a7-120">ID della pipeline dei processi specifica in cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3a7-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="5b3a7-121">-SubmittedAfter</span></span>
<span data-ttu-id="5b3a7-122">Filtro facoltativo che restituisce le pipeline di lavoro inviate solo dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3a7-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="5b3a7-123">-SubmittedBefore</span></span>
<span data-ttu-id="5b3a7-124">Un filtro facoltativo che restituisce pipeline dei processi solo inviato prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3a7-125">CommonParameters</span></span>
<span data-ttu-id="5b3a7-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3a7-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b3a7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3a7-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b3a7-128">INPUTS</span></span>

### <span data-ttu-id="5b3a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5b3a7-129">System.String</span></span>

### <span data-ttu-id="5b3a7-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="5b3a7-130">System.Guid</span></span>

### <span data-ttu-id="5b3a7-131">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b3a7-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5b3a7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b3a7-132">OUTPUTS</span></span>

### <span data-ttu-id="5b3a7-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="5b3a7-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="5b3a7-134">Note</span><span class="sxs-lookup"><span data-stu-id="5b3a7-134">NOTES</span></span>

## <span data-ttu-id="5b3a7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b3a7-135">RELATED LINKS</span></span>
