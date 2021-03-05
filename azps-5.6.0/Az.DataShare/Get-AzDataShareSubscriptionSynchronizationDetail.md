---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: c2f7dc41bc84594d1c9d7e64dc52f27a162b8be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006813"
---
# <span data-ttu-id="6b1dc-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="6b1dc-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="6b1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1dc-103">Recupera informazioni sui dettagli di sincronizzazione per la condivisione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="6b1dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b1dc-104">SYNTAX</span></span>

### <span data-ttu-id="6b1dc-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b1dc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1dc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b1dc-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b1dc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b1dc-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1dc-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornisce i dettagli della sincronizzazione avviata per una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="6b1dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b1dc-109">EXAMPLES</span></span>

### <span data-ttu-id="6b1dc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b1dc-110">Example 1</span></span>
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

<span data-ttu-id="6b1dc-111">Questo comando fornisce informazioni sulla sincronizzazione avviata per la condivisione della sottoscrizione AdsShareSubscription nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="6b1dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b1dc-112">PARAMETERS</span></span>

### <span data-ttu-id="6b1dc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6b1dc-113">-AccountName</span></span>
<span data-ttu-id="6b1dc-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="6b1dc-114">Azure data share account name</span></span>

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

### <span data-ttu-id="6b1dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1dc-115">-DefaultProfile</span></span>
<span data-ttu-id="6b1dc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b1dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b1dc-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="6b1dc-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6b1dc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b1dc-119">-ResourceId</span></span>
<span data-ttu-id="6b1dc-120">ID risorsa sottoscrizione condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="6b1dc-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="6b1dc-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6b1dc-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="6b1dc-122">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="6b1dc-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6b1dc-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="6b1dc-123">-SynchronizationId</span></span>
<span data-ttu-id="6b1dc-124">ID sincronizzazione della sincronizzazione della sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="6b1dc-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="6b1dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1dc-125">CommonParameters</span></span>
<span data-ttu-id="6b1dc-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1dc-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b1dc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1dc-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b1dc-128">INPUTS</span></span>

### <span data-ttu-id="6b1dc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6b1dc-129">System.String</span></span>

## <span data-ttu-id="6b1dc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b1dc-130">OUTPUTS</span></span>

### <span data-ttu-id="6b1dc-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="6b1dc-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="6b1dc-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b1dc-132">NOTES</span></span>

## <span data-ttu-id="6b1dc-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b1dc-133">RELATED LINKS</span></span>
