---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202359"
---
# <span data-ttu-id="c0b16-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="c0b16-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="c0b16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0b16-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b16-103">Aggiorna o crea un'offerta per l'archivio privato.</span><span class="sxs-lookup"><span data-stu-id="c0b16-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="c0b16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0b16-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0b16-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b16-106">Aggiorna o crea l'offerta per l'archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="c0b16-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="c0b16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0b16-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0b16-108">Example 1</span></span>
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

<span data-ttu-id="c0b16-109">Crea un'offerta con piani privati + pubblici per l'archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="c0b16-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="c0b16-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c0b16-110">Example 2</span></span>
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

<span data-ttu-id="c0b16-111">Crea un'offerta con piani privati solo per gli archivi privati creati in ambito abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c0b16-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="c0b16-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c0b16-112">Example 3</span></span>
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

<span data-ttu-id="c0b16-113">Offerta aggiornamenti con piani privati + pubblici per l'archivio privato creato in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="c0b16-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="c0b16-114">È necessario un ETag.</span><span class="sxs-lookup"><span data-stu-id="c0b16-114">Etag is needed.</span></span>

### <span data-ttu-id="c0b16-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c0b16-115">Example 4</span></span>
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

<span data-ttu-id="c0b16-116">Offerta aggiornamenti per gli archivi privati con piani privati creati in ambito abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c0b16-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="c0b16-117">È necessario un ETag.</span><span class="sxs-lookup"><span data-stu-id="c0b16-117">Etag is needed.</span></span>


## <span data-ttu-id="c0b16-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0b16-118">PARAMETERS</span></span>

### <span data-ttu-id="c0b16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b16-119">-DefaultProfile</span></span>
<span data-ttu-id="c0b16-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b16-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="c0b16-121">-ETag</span></span>
<span data-ttu-id="c0b16-122">ETag dell'offerta di Azure Marketplace privateStore per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="c0b16-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="c0b16-123">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="c0b16-123">-OfferId</span></span>
<span data-ttu-id="c0b16-124">Offerta privateStore di Azure Marketplace necessaria</span><span class="sxs-lookup"><span data-stu-id="c0b16-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="c0b16-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="c0b16-125">-PrivateStoreId</span></span>
<span data-ttu-id="c0b16-126">Offerte di Azure Marketplace privateStore richieste</span><span class="sxs-lookup"><span data-stu-id="c0b16-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="c0b16-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="c0b16-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="c0b16-128">Limitazione di ID piano specifica dell'offerta di Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="c0b16-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="c0b16-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0b16-129">-Confirm</span></span>
<span data-ttu-id="c0b16-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0b16-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b16-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b16-131">-WhatIf</span></span>
<span data-ttu-id="c0b16-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0b16-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b16-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0b16-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b16-134">CommonParameters</span></span>
<span data-ttu-id="c0b16-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b16-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0b16-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b16-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0b16-137">INPUTS</span></span>

### <span data-ttu-id="c0b16-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c0b16-138">None</span></span>

## <span data-ttu-id="c0b16-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0b16-139">OUTPUTS</span></span>

### <span data-ttu-id="c0b16-140">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="c0b16-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="c0b16-141">Note</span><span class="sxs-lookup"><span data-stu-id="c0b16-141">NOTES</span></span>

## <span data-ttu-id="c0b16-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0b16-142">RELATED LINKS</span></span>
