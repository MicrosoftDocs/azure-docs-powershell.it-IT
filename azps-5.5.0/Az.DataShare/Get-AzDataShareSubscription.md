---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198063"
---
# <span data-ttu-id="a9dc7-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a9dc7-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="a9dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dc7-103">Ottiene informazioni sulla sottoscrizione di condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="a9dc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9dc7-104">SYNTAX</span></span>

### <span data-ttu-id="a9dc7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9dc7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9dc7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9dc7-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9dc7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="a9dc7-108">Il cmdlet **Get-AzDataShareSubscription** fornisce informazioni sulla sottoscrizione della condivisione in un account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="a9dc7-109">Se si specifica il nome della sottoscrizione di condivisione, il cmdlet fornisce informazioni sulla sottoscrizione di condivisione specifica.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="a9dc7-110">In caso contrario, il cmdlet fornisce un elenco delle sottoscrizioni di condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="a9dc7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9dc7-111">EXAMPLES</span></span>

### <span data-ttu-id="a9dc7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9dc7-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="a9dc7-113">Questo comando fornisce informazioni sulla condivisione dell'abbonamento AdsShareSubscription nell'account di condivisione dati WikiAds.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="a9dc7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9dc7-114">PARAMETERS</span></span>

### <span data-ttu-id="a9dc7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9dc7-115">-AccountName</span></span>
<span data-ttu-id="a9dc7-116">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a9dc7-116">Azure data share account name</span></span>

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

### <span data-ttu-id="a9dc7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dc7-117">-DefaultProfile</span></span>
<span data-ttu-id="a9dc7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9dc7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9dc7-119">-Name</span></span>
<span data-ttu-id="a9dc7-120">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a9dc7-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9dc7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9dc7-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9dc7-122">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a9dc7-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a9dc7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9dc7-123">-ResourceId</span></span>
<span data-ttu-id="a9dc7-124">ID risorsa della sottoscrizione della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a9dc7-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="a9dc7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dc7-125">CommonParameters</span></span>
<span data-ttu-id="a9dc7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dc7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9dc7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dc7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9dc7-128">INPUTS</span></span>

### <span data-ttu-id="a9dc7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a9dc7-129">System.String</span></span>

## <span data-ttu-id="a9dc7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9dc7-130">OUTPUTS</span></span>

### <span data-ttu-id="a9dc7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a9dc7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="a9dc7-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9dc7-132">NOTES</span></span>

## <span data-ttu-id="a9dc7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9dc7-133">RELATED LINKS</span></span>
