---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: ba6cff5c2618754caa35efbaa7345c24b1f25a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674877"
---
# <span data-ttu-id="58bd0-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="58bd0-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="58bd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="58bd0-103">Ottiene una ricorrenza o ricorrenza dei processi di analisi del lago dati.</span><span class="sxs-lookup"><span data-stu-id="58bd0-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="58bd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58bd0-104">SYNTAX</span></span>

### <span data-ttu-id="58bd0-105">GetAllInAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58bd0-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58bd0-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="58bd0-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58bd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58bd0-107">DESCRIPTION</span></span>
<span data-ttu-id="58bd0-108">**Get-AzDataLakeAnalyticsJobRecurrence** ottiene una ricorrenza dei processi di analisi di dati di Azure Data Lake specificata o un elenco di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="58bd0-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="58bd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58bd0-109">EXAMPLES</span></span>

### <span data-ttu-id="58bd0-110">Esempio 1: ottenere una ricorrenza specificata</span><span class="sxs-lookup"><span data-stu-id="58bd0-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="58bd0-111">Questo comando ottiene la ricorrenza del processo specificata con l'ID ' 83cb7ad2-3523-4b82-B909-d478b0d8aea3' nell'account ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="58bd0-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="58bd0-112">Esempio 2: ottenere un elenco di tutte le ricorrenze nell'account</span><span class="sxs-lookup"><span data-stu-id="58bd0-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="58bd0-113">Questo comando ottiene un elenco di tutte le ricorrenze nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="58bd0-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="58bd0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58bd0-114">PARAMETERS</span></span>

### <span data-ttu-id="58bd0-115">-Account</span><span class="sxs-lookup"><span data-stu-id="58bd0-115">-Account</span></span>
<span data-ttu-id="58bd0-116">Nome del nome dell'account di data Lake Analytics in cui si vuole recuperare la ricorrenza del processo.</span><span class="sxs-lookup"><span data-stu-id="58bd0-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="58bd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bd0-117">-DefaultProfile</span></span>
<span data-ttu-id="58bd0-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="58bd0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58bd0-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="58bd0-119">-RecurrenceId</span></span>
<span data-ttu-id="58bd0-120">ID della ricorrenza del processo specifica a cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="58bd0-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58bd0-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="58bd0-121">-SubmittedAfter</span></span>
<span data-ttu-id="58bd0-122">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="58bd0-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="58bd0-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="58bd0-123">-SubmittedBefore</span></span>
<span data-ttu-id="58bd0-124">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="58bd0-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="58bd0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bd0-125">CommonParameters</span></span>
<span data-ttu-id="58bd0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58bd0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bd0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bd0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bd0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58bd0-128">INPUTS</span></span>

### <span data-ttu-id="58bd0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="58bd0-129">System.String</span></span>

### <span data-ttu-id="58bd0-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="58bd0-130">System.Guid</span></span>

### <span data-ttu-id="58bd0-131">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58bd0-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58bd0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58bd0-132">OUTPUTS</span></span>

### <span data-ttu-id="58bd0-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="58bd0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="58bd0-134">Note</span><span class="sxs-lookup"><span data-stu-id="58bd0-134">NOTES</span></span>

## <span data-ttu-id="58bd0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58bd0-135">RELATED LINKS</span></span>
