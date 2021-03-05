---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009614"
---
# <span data-ttu-id="3f93d-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="3f93d-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="3f93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f93d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f93d-103">Aggiorna o crea un'offerta per l'archivio privato.</span><span class="sxs-lookup"><span data-stu-id="3f93d-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="3f93d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f93d-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f93d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f93d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f93d-106">Aggiorna o crea un'offerta per l'archivio privato creato nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="3f93d-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="3f93d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f93d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f93d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f93d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3f93d-109">Crea un'offerta con piani privati + pubblici per l'archivio privato creato nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="3f93d-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="3f93d-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3f93d-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3f93d-111">Crea un'offerta con piani privati solo per l'archivio privato creato nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3f93d-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="3f93d-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3f93d-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3f93d-113">Gli aggiornamenti offrono piani + pubblici privati per l'archivio privato creato nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="3f93d-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="3f93d-114">È necessario un Etag.</span><span class="sxs-lookup"><span data-stu-id="3f93d-114">Etag is needed.</span></span>

### <span data-ttu-id="3f93d-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3f93d-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3f93d-116">Aggiornamenti per l'archivio privato con piani privati creati solo nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3f93d-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="3f93d-117">È necessario un Etag.</span><span class="sxs-lookup"><span data-stu-id="3f93d-117">Etag is needed.</span></span>


## <span data-ttu-id="3f93d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f93d-118">PARAMETERS</span></span>

### <span data-ttu-id="3f93d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f93d-119">-DefaultProfile</span></span>
<span data-ttu-id="3f93d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f93d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f93d-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="3f93d-121">-ETag</span></span>
<span data-ttu-id="3f93d-122">ETag per l'aggiornamento dell'offerta di Azure Marketplace privato</span><span class="sxs-lookup"><span data-stu-id="3f93d-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="3f93d-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="3f93d-123">-OfferId</span></span>
<span data-ttu-id="3f93d-124">Offerta di Azure Marketplace privata obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3f93d-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="3f93d-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="3f93d-125">-PrivateStoreId</span></span>
<span data-ttu-id="3f93d-126">Offerte private di Azure Marketplace richieste</span><span class="sxs-lookup"><span data-stu-id="3f93d-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="3f93d-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="3f93d-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="3f93d-128">Limitazione degli ID dei piani specifici dell'offerta di Azure Marketplace privata richiesta</span><span class="sxs-lookup"><span data-stu-id="3f93d-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f93d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f93d-129">-Confirm</span></span>
<span data-ttu-id="3f93d-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f93d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f93d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f93d-131">-WhatIf</span></span>
<span data-ttu-id="3f93d-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f93d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f93d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f93d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f93d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f93d-134">CommonParameters</span></span>
<span data-ttu-id="3f93d-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f93d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f93d-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f93d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f93d-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f93d-137">INPUTS</span></span>

### <span data-ttu-id="3f93d-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3f93d-138">None</span></span>

## <span data-ttu-id="3f93d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f93d-139">OUTPUTS</span></span>

### <span data-ttu-id="3f93d-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="3f93d-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="3f93d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f93d-141">NOTES</span></span>

## <span data-ttu-id="3f93d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f93d-142">RELATED LINKS</span></span>
