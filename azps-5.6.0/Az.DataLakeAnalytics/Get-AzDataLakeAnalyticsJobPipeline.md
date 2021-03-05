---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988272"
---
# <span data-ttu-id="06d85-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="06d85-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="06d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d85-102">SYNOPSIS</span></span>
<span data-ttu-id="06d85-103">Ottiene una pipeline o pipeline di Data Lake Analytics Job.</span><span class="sxs-lookup"><span data-stu-id="06d85-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="06d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06d85-104">SYNTAX</span></span>

### <span data-ttu-id="06d85-105">GetAllInAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06d85-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d85-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="06d85-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d85-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06d85-107">DESCRIPTION</span></span>
<span data-ttu-id="06d85-108">**Get-AzDataLakeAnalyticsJobPipeline** ottiene una pipeline specifica di Azure Data Lake Analytics Job o un elenco di pipeline.</span><span class="sxs-lookup"><span data-stu-id="06d85-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="06d85-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06d85-109">EXAMPLES</span></span>

### <span data-ttu-id="06d85-110">Esempio 1: Ottenere una pipeline specificata</span><span class="sxs-lookup"><span data-stu-id="06d85-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="06d85-111">Questo comando ottiene la pipeline specificata con ID '83cb7ad2-3523-4b82-b909-d478b0d8aea3' nell'account 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="06d85-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="06d85-112">Esempio 2: Ottenere un elenco di tutte le pipeline nell'account</span><span class="sxs-lookup"><span data-stu-id="06d85-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="06d85-113">Questo comando ottiene un elenco di tutte le pipeline nell'account "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="06d85-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="06d85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d85-114">PARAMETERS</span></span>

### <span data-ttu-id="06d85-115">-Account</span><span class="sxs-lookup"><span data-stu-id="06d85-115">-Account</span></span>
<span data-ttu-id="06d85-116">Nome dell'account Data Lake Analytics in cui si vuole recuperare la pipeline di processo.</span><span class="sxs-lookup"><span data-stu-id="06d85-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="06d85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d85-117">-DefaultProfile</span></span>
<span data-ttu-id="06d85-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="06d85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06d85-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="06d85-119">-PipelineId</span></span>
<span data-ttu-id="06d85-120">ID della pipeline di processo specifica per cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="06d85-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="06d85-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="06d85-121">-SubmittedAfter</span></span>
<span data-ttu-id="06d85-122">Filtro facoltativo che restituisce le pipeline di processo inviate solo dopo il periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="06d85-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="06d85-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="06d85-123">-SubmittedBefore</span></span>
<span data-ttu-id="06d85-124">Filtro facoltativo che restituisce le pipeline di processo inviate solo prima del periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="06d85-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="06d85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d85-125">CommonParameters</span></span>
<span data-ttu-id="06d85-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d85-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d85-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d85-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="06d85-128">INPUTS</span></span>

### <span data-ttu-id="06d85-129">System.String</span><span class="sxs-lookup"><span data-stu-id="06d85-129">System.String</span></span>

### <span data-ttu-id="06d85-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="06d85-130">System.Guid</span></span>

### <span data-ttu-id="06d85-131">System.Nullable'1[[System.DateTimeToken, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06d85-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="06d85-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06d85-132">OUTPUTS</span></span>

### <span data-ttu-id="06d85-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="06d85-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="06d85-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="06d85-134">NOTES</span></span>

## <span data-ttu-id="06d85-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06d85-135">RELATED LINKS</span></span>
