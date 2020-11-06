---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 838fb221952a97234c31c514aa82fc30be7e2f25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521698"
---
# <span data-ttu-id="faee5-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="faee5-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="faee5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faee5-102">SYNOPSIS</span></span>
<span data-ttu-id="faee5-103">Ottiene una pipeline o pipeline dei processi di analisi del lago dati.</span><span class="sxs-lookup"><span data-stu-id="faee5-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faee5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faee5-104">SYNTAX</span></span>

### <span data-ttu-id="faee5-105">Tutto in account (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="faee5-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faee5-106">Pipeline processi specifica</span><span class="sxs-lookup"><span data-stu-id="faee5-106">Specific Job Pipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faee5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faee5-107">DESCRIPTION</span></span>
<span data-ttu-id="faee5-108">**Get-AzureRmDataLakeAnalyticsJobPipeline** ottiene una pipeline dei processi di analisi di dati di Azure Data Lake specificata o un elenco di pipeline.</span><span class="sxs-lookup"><span data-stu-id="faee5-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="faee5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faee5-109">EXAMPLES</span></span>

### <span data-ttu-id="faee5-110">Esempio 1: ottenere una pipeline specificata</span><span class="sxs-lookup"><span data-stu-id="faee5-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="faee5-111">Questo comando ottiene la pipeline specificata con l'ID ' 83cb7ad2-3523-4b82-B909-d478b0d8aea3' nell'account ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="faee5-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="faee5-112">Esempio 2: ottenere un elenco di tutte le pipeline nell'account</span><span class="sxs-lookup"><span data-stu-id="faee5-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="faee5-113">Questo comando ottiene un elenco di tutte le pipeline nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="faee5-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="faee5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faee5-114">PARAMETERS</span></span>

### <span data-ttu-id="faee5-115">-Account</span><span class="sxs-lookup"><span data-stu-id="faee5-115">-Account</span></span>
<span data-ttu-id="faee5-116">Nome del nome dell'account di data Lake Analytics in cui si vuole recuperare la pipeline dei processi.</span><span class="sxs-lookup"><span data-stu-id="faee5-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="faee5-117">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="faee5-117">-PipelineId</span></span>
<span data-ttu-id="faee5-118">ID della pipeline dei processi specifica in cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="faee5-118">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Pipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faee5-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="faee5-119">-SubmittedAfter</span></span>
<span data-ttu-id="faee5-120">Filtro facoltativo che restituisce le pipeline di lavoro inviate solo dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="faee5-120">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="faee5-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="faee5-121">-SubmittedBefore</span></span>
<span data-ttu-id="faee5-122">Un filtro facoltativo che restituisce pipeline dei processi solo inviato prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="faee5-122">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="faee5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faee5-123">-DefaultProfile</span></span>
<span data-ttu-id="faee5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faee5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faee5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faee5-125">CommonParameters</span></span>
<span data-ttu-id="faee5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faee5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faee5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faee5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faee5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faee5-128">INPUTS</span></span>

### <span data-ttu-id="faee5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="faee5-129">System.String</span></span>

### <span data-ttu-id="faee5-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="faee5-130">System.Guid</span></span>

## <span data-ttu-id="faee5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faee5-131">OUTPUTS</span></span>

### <span data-ttu-id="faee5-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="faee5-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="faee5-133">Note</span><span class="sxs-lookup"><span data-stu-id="faee5-133">NOTES</span></span>

## <span data-ttu-id="faee5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faee5-134">RELATED LINKS</span></span>

