---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191611"
---
# <span data-ttu-id="f584d-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="f584d-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="f584d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f584d-102">SYNOPSIS</span></span>
<span data-ttu-id="f584d-103">Ottiene informazioni sui dettagli di portale per l'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="f584d-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="f584d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f584d-104">SYNTAX</span></span>

### <span data-ttu-id="f584d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f584d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f584d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f584d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f584d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f584d-107">DESCRIPTION</span></span>
<span data-ttu-id="f584d-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** fornisce informazioni dettagliate sulla sincronizzazione avviata per un abbonamento a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="f584d-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="f584d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f584d-109">EXAMPLES</span></span>

### <span data-ttu-id="f584d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f584d-110">Example 1</span></span>
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

<span data-ttu-id="f584d-111">Questo comando fornisce informazioni sulla sincronizzazione avviata per la condivisione di abbonamenti AdsShareSubscription in WikiAds account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="f584d-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="f584d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f584d-112">PARAMETERS</span></span>

### <span data-ttu-id="f584d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f584d-113">-AccountName</span></span>
<span data-ttu-id="f584d-114">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f584d-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f584d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f584d-115">-DefaultProfile</span></span>
<span data-ttu-id="f584d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f584d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f584d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f584d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f584d-118">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f584d-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f584d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f584d-119">-ResourceId</span></span>
<span data-ttu-id="f584d-120">ID risorsa di abbonamento a Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="f584d-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="f584d-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f584d-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="f584d-122">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="f584d-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="f584d-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="f584d-123">-SynchronizationId</span></span>
<span data-ttu-id="f584d-124">ID sincronizzazione della sincronizzazione di condivisione sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f584d-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="f584d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f584d-125">CommonParameters</span></span>
<span data-ttu-id="f584d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f584d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f584d-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f584d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f584d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f584d-128">INPUTS</span></span>

### <span data-ttu-id="f584d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f584d-129">System.String</span></span>

## <span data-ttu-id="f584d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f584d-130">OUTPUTS</span></span>

### <span data-ttu-id="f584d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="f584d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="f584d-132">Note</span><span class="sxs-lookup"><span data-stu-id="f584d-132">NOTES</span></span>

## <span data-ttu-id="f584d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f584d-133">RELATED LINKS</span></span>
