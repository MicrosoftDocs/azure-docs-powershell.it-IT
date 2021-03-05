---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 3c7356768db35ce2c21499db0a94402f040b5162
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003774"
---
# <span data-ttu-id="222e5-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="222e5-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="222e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="222e5-102">SYNOPSIS</span></span>
<span data-ttu-id="222e5-103">Ottieni l'offerta di uno o più archivi privati.</span><span class="sxs-lookup"><span data-stu-id="222e5-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="222e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="222e5-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="222e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="222e5-105">DESCRIPTION</span></span>
<span data-ttu-id="222e5-106">Ottenere l'offerta di uno o più archivi privati con piani pubblici e privati aggiunti nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="222e5-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="222e5-107">Se l'ID dell'abbonamento viene presentato, ottieni un'offerta dell'archivio privato con piani privati solo nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="222e5-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="222e5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="222e5-108">EXAMPLES</span></span>

### <span data-ttu-id="222e5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="222e5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="222e5-110">Ottieni le offerte dell'archivio privato con piani privati e pubblici aggiunti nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="222e5-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="222e5-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="222e5-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="222e5-112">Ottieni le offerte dell'archivio privato solo con piani privati che sono stati aggiunti nell'ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="222e5-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="222e5-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="222e5-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="222e5-114">Ottenere l'offerta dell'archivio privato con piani privati e pubblici aggiunti nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="222e5-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="222e5-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="222e5-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="222e5-116">Ottenere l'offerta dell'archivio privato solo con piani privati aggiunti nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="222e5-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="222e5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="222e5-117">PARAMETERS</span></span>

### <span data-ttu-id="222e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222e5-118">-DefaultProfile</span></span>
<span data-ttu-id="222e5-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="222e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="222e5-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="222e5-120">-OfferId</span></span>
<span data-ttu-id="222e5-121">Offerta di Azure Marketplace privata obbligatoria</span><span class="sxs-lookup"><span data-stu-id="222e5-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222e5-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="222e5-122">-PrivateStoreId</span></span>
<span data-ttu-id="222e5-123">Offerte private di Azure Marketplace richieste</span><span class="sxs-lookup"><span data-stu-id="222e5-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="222e5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="222e5-124">-SubscriptionId</span></span>
<span data-ttu-id="222e5-125">ID sottoscrizione di Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="222e5-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222e5-126">CommonParameters</span></span>
<span data-ttu-id="222e5-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="222e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222e5-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="222e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222e5-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="222e5-129">INPUTS</span></span>

### <span data-ttu-id="222e5-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="222e5-130">None</span></span>

## <span data-ttu-id="222e5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="222e5-131">OUTPUTS</span></span>

### <span data-ttu-id="222e5-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="222e5-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="222e5-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="222e5-133">NOTES</span></span>

## <span data-ttu-id="222e5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="222e5-134">RELATED LINKS</span></span>
