---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 751fa50a6c29c826fe707852efa661b78d1b9c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004269"
---
# <span data-ttu-id="f2469-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="f2469-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="f2469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2469-102">SYNOPSIS</span></span>
<span data-ttu-id="f2469-103">Ottiene la ricorrenza o le ricorrenze di un processo di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2469-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="f2469-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2469-104">SYNTAX</span></span>

### <span data-ttu-id="f2469-105">GetAllInAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2469-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2469-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="f2469-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2469-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2469-107">DESCRIPTION</span></span>
<span data-ttu-id="f2469-108">**Get-AzDataLakeAnalyticsJobRecurrence** ottiene la ricorrenza specificata del processo di Azure Data Lake Analytics o un elenco di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="f2469-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="f2469-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2469-109">EXAMPLES</span></span>

### <span data-ttu-id="f2469-110">Esempio 1: Ottenere una ricorrenza specificata</span><span class="sxs-lookup"><span data-stu-id="f2469-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="f2469-111">Questo comando recupera la ricorrenza di processo specificata con ID '83cb7ad2-3523-4b82-b909-d478b0d8aea3' nell'account 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="f2469-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="f2469-112">Esempio 2: Ottenere un elenco di tutte le ricorrenze nell'account</span><span class="sxs-lookup"><span data-stu-id="f2469-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="f2469-113">Questo comando ottiene un elenco di tutte le ricorrenze nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="f2469-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="f2469-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2469-114">PARAMETERS</span></span>

### <span data-ttu-id="f2469-115">-Account</span><span class="sxs-lookup"><span data-stu-id="f2469-115">-Account</span></span>
<span data-ttu-id="f2469-116">Nome dell'account Data Lake Analytics in cui si vuole recuperare la ricorrenza del processo.</span><span class="sxs-lookup"><span data-stu-id="f2469-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="f2469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2469-117">-DefaultProfile</span></span>
<span data-ttu-id="f2469-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2469-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2469-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f2469-119">-RecurrenceId</span></span>
<span data-ttu-id="f2469-120">ID della ricorrenza di un processo specifico per cui restituire informazioni.</span><span class="sxs-lookup"><span data-stu-id="f2469-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="f2469-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="f2469-121">-SubmittedAfter</span></span>
<span data-ttu-id="f2469-122">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo dopo il periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f2469-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="f2469-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="f2469-123">-SubmittedBefore</span></span>
<span data-ttu-id="f2469-124">Filtro facoltativo che restituisce le ricorrenze dei processi inviate solo prima del periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f2469-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="f2469-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2469-125">CommonParameters</span></span>
<span data-ttu-id="f2469-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2469-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2469-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2469-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2469-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2469-128">INPUTS</span></span>

### <span data-ttu-id="f2469-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f2469-129">System.String</span></span>

### <span data-ttu-id="f2469-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f2469-130">System.Guid</span></span>

### <span data-ttu-id="f2469-131">System.Nullable'1[[System.DateTimeToken, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f2469-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f2469-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2469-132">OUTPUTS</span></span>

### <span data-ttu-id="f2469-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="f2469-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="f2469-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2469-134">NOTES</span></span>

## <span data-ttu-id="f2469-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2469-135">RELATED LINKS</span></span>
