---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: ba4fc6a58cd345c149e551263ddf5880f099a54e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864730"
---
# <span data-ttu-id="e2672-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e2672-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="e2672-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2672-102">SYNOPSIS</span></span>
<span data-ttu-id="e2672-103">Ottiene informazioni sull'abbonamento alla condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="e2672-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="e2672-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2672-104">SYNTAX</span></span>

### <span data-ttu-id="e2672-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2672-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2672-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2672-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2672-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2672-107">DESCRIPTION</span></span>
<span data-ttu-id="e2672-108">Il cmdlet **Get-AzDataShareSubscription** fornisce informazioni su come condividere l'abbonamento in un account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="e2672-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="e2672-109">Se viene fornito il nome dell'abbonamento di condivisione, il cmdlet fornisce informazioni sul particolare abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="e2672-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="e2672-110">In caso contrario, il cmdlet fornisce un elenco di abbonamenti di condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="e2672-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="e2672-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2672-111">EXAMPLES</span></span>

### <span data-ttu-id="e2672-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2672-112">Example 1</span></span>
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

<span data-ttu-id="e2672-113">Questo comando fornisce informazioni sulla condivisione dell'abbonamento AdsShareSubscription in WikiAds dell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="e2672-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="e2672-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2672-114">PARAMETERS</span></span>

### <span data-ttu-id="e2672-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2672-115">-AccountName</span></span>
<span data-ttu-id="e2672-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e2672-116">Azure data share account name</span></span>

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

### <span data-ttu-id="e2672-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2672-117">-DefaultProfile</span></span>
<span data-ttu-id="e2672-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2672-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2672-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2672-119">-Name</span></span>
<span data-ttu-id="e2672-120">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e2672-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e2672-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2672-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2672-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e2672-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e2672-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2672-123">-ResourceId</span></span>
<span data-ttu-id="e2672-124">ID risorsa dell'abbonamento a una condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="e2672-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="e2672-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2672-125">CommonParameters</span></span>
<span data-ttu-id="e2672-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2672-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2672-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2672-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2672-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2672-128">INPUTS</span></span>

### <span data-ttu-id="e2672-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e2672-129">System.String</span></span>

## <span data-ttu-id="e2672-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2672-130">OUTPUTS</span></span>

### <span data-ttu-id="e2672-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e2672-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="e2672-132">Note</span><span class="sxs-lookup"><span data-stu-id="e2672-132">NOTES</span></span>

## <span data-ttu-id="e2672-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2672-133">RELATED LINKS</span></span>
