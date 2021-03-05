---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962285"
---
# <span data-ttu-id="e3a7b-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e3a7b-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e3a7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a7b-103">Ottiene informazioni sulla sincronizzazione eseguita nell'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="e3a7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a7b-104">SYNTAX</span></span>

### <span data-ttu-id="e3a7b-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3a7b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3a7b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3a7b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a7b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3a7b-107">DESCRIPTION</span></span>
<span data-ttu-id="e3a7b-108">Il cmdlet **Get-AzDataShareSubscriptionSynchronization** fornisce informazioni su tutta la sincronizzazione eseguita in una sottoscrizione di condivisione in un account di condivisione dati nel consumer.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="e3a7b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a7b-109">EXAMPLES</span></span>

### <span data-ttu-id="e3a7b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3a7b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="e3a7b-111">Questo comando fornisce informazioni su tutta la sincronizzazione eseguita per una sottoscrizione di condivisione AdsShareSubscription nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="e3a7b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a7b-112">PARAMETERS</span></span>

### <span data-ttu-id="e3a7b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3a7b-113">-AccountName</span></span>
<span data-ttu-id="e3a7b-114">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3a7b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="e3a7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a7b-115">-DefaultProfile</span></span>
<span data-ttu-id="e3a7b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3a7b-118">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3a7b-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e3a7b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a7b-119">-ResourceId</span></span>
<span data-ttu-id="e3a7b-120">ID risorsa sottoscrizione condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3a7b-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="e3a7b-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e3a7b-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="e3a7b-122">Nome della sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e3a7b-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e3a7b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a7b-123">CommonParameters</span></span>
<span data-ttu-id="e3a7b-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a7b-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3a7b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a7b-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3a7b-126">INPUTS</span></span>

### <span data-ttu-id="e3a7b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e3a7b-127">System.String</span></span>

## <span data-ttu-id="e3a7b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a7b-128">OUTPUTS</span></span>

### <span data-ttu-id="e3a7b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e3a7b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e3a7b-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3a7b-130">NOTES</span></span>

## <span data-ttu-id="e3a7b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a7b-131">RELATED LINKS</span></span>
