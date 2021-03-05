---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: a4367087bd248589f3345c14f6c7681be5eae9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989587"
---
# <span data-ttu-id="4268c-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="4268c-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="4268c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4268c-102">SYNOPSIS</span></span>
<span data-ttu-id="4268c-103">Ottiene le posizioni di peering offerte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="4268c-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="4268c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4268c-104">SYNTAX</span></span>

### <span data-ttu-id="4268c-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4268c-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4268c-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="4268c-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4268c-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="4268c-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4268c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4268c-108">DESCRIPTION</span></span>
<span data-ttu-id="4268c-109">Ottiene le strutture di peering in cui gli utenti possono connettersi con ARM.</span><span class="sxs-lookup"><span data-stu-id="4268c-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="4268c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4268c-110">EXAMPLES</span></span>

### <span data-ttu-id="4268c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4268c-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="4268c-112">Il suo lungo elenco di posizioni.</span><span class="sxs-lookup"><span data-stu-id="4268c-112">Its a long list of locations.</span></span> <span data-ttu-id="4268c-113">Ottiene tutte le strutture di peering diretto.</span><span class="sxs-lookup"><span data-stu-id="4268c-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="4268c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4268c-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="4268c-115">Ottiene la posizione di peering di Exchange per Honolulu.</span><span class="sxs-lookup"><span data-stu-id="4268c-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="4268c-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4268c-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="4268c-117">Ottiene la posizione di peering di Exchange per l'ID della struttura di peering 71.</span><span class="sxs-lookup"><span data-stu-id="4268c-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="4268c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4268c-118">PARAMETERS</span></span>

### <span data-ttu-id="4268c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4268c-119">-DefaultProfile</span></span>
<span data-ttu-id="4268c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4268c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4268c-121">-DirectCollectioningType</span><span class="sxs-lookup"><span data-stu-id="4268c-121">-DirectPeeringType</span></span>
<span data-ttu-id="4268c-122">Selezionare "Edge", "CDN" e "Transit".</span><span class="sxs-lookup"><span data-stu-id="4268c-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4268c-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="4268c-123">-Kind</span></span>
<span data-ttu-id="4268c-124">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="4268c-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4268c-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="4268c-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="4268c-126">ID PeeringDB.com struttura</span><span class="sxs-lookup"><span data-stu-id="4268c-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4268c-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="4268c-127">-PeeringLocation</span></span>
<span data-ttu-id="4268c-128">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4268c-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4268c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4268c-129">CommonParameters</span></span>
<span data-ttu-id="4268c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4268c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4268c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4268c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4268c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4268c-132">INPUTS</span></span>

### <span data-ttu-id="4268c-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4268c-133">None</span></span>

## <span data-ttu-id="4268c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4268c-134">OUTPUTS</span></span>

### <span data-ttu-id="4268c-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSLocationingLocation</span><span class="sxs-lookup"><span data-stu-id="4268c-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="4268c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="4268c-136">NOTES</span></span>

## <span data-ttu-id="4268c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4268c-137">RELATED LINKS</span></span>
