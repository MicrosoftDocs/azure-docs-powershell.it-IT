---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475216"
---
# <span data-ttu-id="a7791-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a7791-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="a7791-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7791-102">SYNOPSIS</span></span>
<span data-ttu-id="a7791-103">Ottenere una o più offerte di uno store privato.</span><span class="sxs-lookup"><span data-stu-id="a7791-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="a7791-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7791-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7791-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7791-105">DESCRIPTION</span></span>
<span data-ttu-id="a7791-106">Ottenere una o più offerte di un archivio privato con i piani public + private aggiunti in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="a7791-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="a7791-107">Se l'ID abbonamento è presente, ottenere una o più offerte private Store con piani privati solo in ambito abbonamento</span><span class="sxs-lookup"><span data-stu-id="a7791-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="a7791-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7791-108">EXAMPLES</span></span>

### <span data-ttu-id="a7791-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7791-109">Example 1</span></span>
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

<span data-ttu-id="a7791-110">Ottenere le offerte dell'archivio privato con i piani privati + pubblici aggiunti in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="a7791-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="a7791-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a7791-111">Example 2</span></span>
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

<span data-ttu-id="a7791-112">Ottenere le offerte dell'archivio privato con piani privati aggiunti in ambito abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a7791-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="a7791-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a7791-113">Example 3</span></span>
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

<span data-ttu-id="a7791-114">Ottenere l'offerta dell'archivio privato con i piani privati + pubblici aggiunti in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="a7791-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="a7791-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a7791-115">Example 4</span></span>
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

<span data-ttu-id="a7791-116">Ottenere l'offerta dell'archivio privato con piani privati solo che è stato aggiunto in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="a7791-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="a7791-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7791-117">PARAMETERS</span></span>

### <span data-ttu-id="a7791-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7791-118">-DefaultProfile</span></span>
<span data-ttu-id="a7791-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7791-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7791-120">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="a7791-120">-OfferId</span></span>
<span data-ttu-id="a7791-121">Offerta privateStore di Azure Marketplace necessaria</span><span class="sxs-lookup"><span data-stu-id="a7791-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="a7791-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="a7791-122">-PrivateStoreId</span></span>
<span data-ttu-id="a7791-123">Offerte di Azure Marketplace privateStore richieste</span><span class="sxs-lookup"><span data-stu-id="a7791-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="a7791-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7791-124">-SubscriptionId</span></span>
<span data-ttu-id="a7791-125">ID abbonamento a Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="a7791-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="a7791-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7791-126">CommonParameters</span></span>
<span data-ttu-id="a7791-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7791-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7791-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7791-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7791-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7791-129">INPUTS</span></span>

### <span data-ttu-id="a7791-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7791-130">None</span></span>

## <span data-ttu-id="a7791-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7791-131">OUTPUTS</span></span>

### <span data-ttu-id="a7791-132">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a7791-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="a7791-133">Note</span><span class="sxs-lookup"><span data-stu-id="a7791-133">NOTES</span></span>

## <span data-ttu-id="a7791-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7791-134">RELATED LINKS</span></span>
