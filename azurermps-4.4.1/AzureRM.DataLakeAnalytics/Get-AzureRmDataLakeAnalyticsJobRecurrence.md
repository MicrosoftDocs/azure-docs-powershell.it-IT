---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: cfc5d0999ed9c77e38b83eee99eabbd19dd1e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688326"
---
# <span data-ttu-id="7baec-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="7baec-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="7baec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7baec-102">SYNOPSIS</span></span>
<span data-ttu-id="7baec-103">Ottiene una ricorrenza o ricorrenza dei processi di analisi del lago dati.</span><span class="sxs-lookup"><span data-stu-id="7baec-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7baec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7baec-104">SYNTAX</span></span>

### <span data-ttu-id="7baec-105">Tutto in account (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7baec-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7baec-106">Ricorrenza professionale specifica</span><span class="sxs-lookup"><span data-stu-id="7baec-106">Specific Job Recurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7baec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7baec-107">DESCRIPTION</span></span>
<span data-ttu-id="7baec-108">**Get-AzureRmDataLakeAnalyticsJobRecurrence** ottiene una ricorrenza dei processi di analisi di dati di Azure Data Lake specificata o un elenco di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="7baec-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="7baec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7baec-109">EXAMPLES</span></span>

### <span data-ttu-id="7baec-110">Esempio 1: ottenere una ricorrenza specificata</span><span class="sxs-lookup"><span data-stu-id="7baec-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="7baec-111">Questo comando ottiene la ricorrenza del processo specificata con l'ID ' 83cb7ad2-3523-4b82-B909-d478b0d8aea3' nell'account ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="7baec-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="7baec-112">Esempio 2: ottenere un elenco di tutte le ricorrenze nell'account</span><span class="sxs-lookup"><span data-stu-id="7baec-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="7baec-113">Questo comando ottiene un elenco di tutte le ricorrenze nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="7baec-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="7baec-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7baec-114">PARAMETERS</span></span>

### <span data-ttu-id="7baec-115">-Account</span><span class="sxs-lookup"><span data-stu-id="7baec-115">-Account</span></span>
<span data-ttu-id="7baec-116">Nome del nome dell'account di data Lake Analytics in cui si vuole recuperare la ricorrenza del processo.</span><span class="sxs-lookup"><span data-stu-id="7baec-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="7baec-117">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="7baec-117">-RecurrenceId</span></span>
<span data-ttu-id="7baec-118">ID della ricorrenza del processo specifica a cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7baec-118">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Recurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7baec-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="7baec-119">-SubmittedAfter</span></span>
<span data-ttu-id="7baec-120">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="7baec-120">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="7baec-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="7baec-121">-SubmittedBefore</span></span>
<span data-ttu-id="7baec-122">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="7baec-122">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="7baec-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baec-123">-DefaultProfile</span></span>
<span data-ttu-id="7baec-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7baec-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7baec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baec-125">CommonParameters</span></span>
<span data-ttu-id="7baec-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7baec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baec-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baec-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7baec-128">INPUTS</span></span>

### <span data-ttu-id="7baec-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7baec-129">System.String</span></span>
<span data-ttu-id="7baec-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7baec-130">System.Guid</span></span>

## <span data-ttu-id="7baec-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7baec-131">OUTPUTS</span></span>

### <span data-ttu-id="7baec-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="7baec-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="7baec-133">Note</span><span class="sxs-lookup"><span data-stu-id="7baec-133">NOTES</span></span>

## <span data-ttu-id="7baec-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7baec-134">RELATED LINKS</span></span>

