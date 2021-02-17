---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194599"
---
# <span data-ttu-id="16c31-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="16c31-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="16c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c31-102">SYNOPSIS</span></span>
<span data-ttu-id="16c31-103">Recupera informazioni sui dettagli di sincronizzazione per la condivisione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="16c31-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="16c31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16c31-104">SYNTAX</span></span>

### <span data-ttu-id="16c31-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16c31-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16c31-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16c31-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c31-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16c31-107">DESCRIPTION</span></span>
<span data-ttu-id="16c31-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornisce i dettagli della sincronizzazione avviata per una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="16c31-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="16c31-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16c31-109">EXAMPLES</span></span>

### <span data-ttu-id="16c31-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16c31-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="16c31-111">Questo comando fornisce informazioni sulla sincronizzazione avviata per la condivisione della sottoscrizione AdsShareSubscription nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="16c31-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="16c31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c31-112">PARAMETERS</span></span>

### <span data-ttu-id="16c31-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16c31-113">-AccountName</span></span>
<span data-ttu-id="16c31-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16c31-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c31-115">-DefaultProfile</span></span>
<span data-ttu-id="16c31-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16c31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c31-117">-ResourceGroupName</span></span>
<span data-ttu-id="16c31-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16c31-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c31-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c31-119">-ResourceId</span></span>
<span data-ttu-id="16c31-120">ID risorsa sottoscrizione condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16c31-120">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c31-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="16c31-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="16c31-122">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="16c31-122">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c31-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="16c31-123">-SynchronizationId</span></span>
<span data-ttu-id="16c31-124">ID sincronizzazione della sincronizzazione della sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="16c31-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c31-125">CommonParameters</span></span>
<span data-ttu-id="16c31-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c31-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16c31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c31-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="16c31-128">INPUTS</span></span>

### <span data-ttu-id="16c31-129">System.String</span><span class="sxs-lookup"><span data-stu-id="16c31-129">System.String</span></span>

## <span data-ttu-id="16c31-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16c31-130">OUTPUTS</span></span>

### <span data-ttu-id="16c31-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="16c31-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="16c31-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="16c31-132">NOTES</span></span>

## <span data-ttu-id="16c31-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16c31-133">RELATED LINKS</span></span>
