---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377408"
---
# <span data-ttu-id="c5812-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c5812-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="c5812-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5812-102">SYNOPSIS</span></span>
<span data-ttu-id="c5812-103">Ottiene informazioni sull'abbonamento alla condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c5812-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="c5812-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5812-104">SYNTAX</span></span>

### <span data-ttu-id="c5812-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5812-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5812-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5812-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5812-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5812-107">DESCRIPTION</span></span>
<span data-ttu-id="c5812-108">Il cmdlet **Get-AzDataShareSubscription** fornisce informazioni su come condividere l'abbonamento in un account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c5812-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="c5812-109">Se viene fornito il nome dell'abbonamento di condivisione, il cmdlet fornisce informazioni sul particolare abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="c5812-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="c5812-110">In caso contrario, il cmdlet fornisce un elenco di abbonamenti di condivisione nell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c5812-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="c5812-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5812-111">EXAMPLES</span></span>

### <span data-ttu-id="c5812-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5812-112">Example 1</span></span>
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

<span data-ttu-id="c5812-113">Questo comando fornisce informazioni sulla condivisione dell'abbonamento AdsShareSubscription in WikiAds dell'account di condivisione dati.</span><span class="sxs-lookup"><span data-stu-id="c5812-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="c5812-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5812-114">PARAMETERS</span></span>

### <span data-ttu-id="c5812-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5812-115">-AccountName</span></span>
<span data-ttu-id="c5812-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c5812-116">Azure data share account name</span></span>

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

### <span data-ttu-id="c5812-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5812-117">-DefaultProfile</span></span>
<span data-ttu-id="c5812-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5812-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5812-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5812-119">-Name</span></span>
<span data-ttu-id="c5812-120">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c5812-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c5812-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5812-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5812-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c5812-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c5812-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5812-123">-ResourceId</span></span>
<span data-ttu-id="c5812-124">ID risorsa dell'abbonamento a una condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="c5812-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="c5812-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5812-125">CommonParameters</span></span>
<span data-ttu-id="c5812-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5812-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5812-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5812-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5812-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5812-128">INPUTS</span></span>

### <span data-ttu-id="c5812-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c5812-129">System.String</span></span>

## <span data-ttu-id="c5812-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5812-130">OUTPUTS</span></span>

### <span data-ttu-id="c5812-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c5812-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="c5812-132">Note</span><span class="sxs-lookup"><span data-stu-id="c5812-132">NOTES</span></span>

## <span data-ttu-id="c5812-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5812-133">RELATED LINKS</span></span>
