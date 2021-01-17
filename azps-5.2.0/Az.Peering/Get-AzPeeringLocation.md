---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345484"
---
# <span data-ttu-id="ebae5-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="ebae5-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="ebae5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ebae5-102">SYNOPSIS</span></span>
<span data-ttu-id="ebae5-103">Ottiene i percorsi di peering offerti da Microsoft</span><span class="sxs-lookup"><span data-stu-id="ebae5-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="ebae5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebae5-104">SYNTAX</span></span>

### <span data-ttu-id="ebae5-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebae5-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebae5-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="ebae5-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebae5-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="ebae5-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebae5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebae5-108">DESCRIPTION</span></span>
<span data-ttu-id="ebae5-109">Ottiene le strutture di peering in cui gli utenti possono connettersi con ARM.</span><span class="sxs-lookup"><span data-stu-id="ebae5-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="ebae5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebae5-110">EXAMPLES</span></span>

### <span data-ttu-id="ebae5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ebae5-111">Example 1</span></span>
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

<span data-ttu-id="ebae5-112">È un lungo elenco di posizioni.</span><span class="sxs-lookup"><span data-stu-id="ebae5-112">Its a long list of locations.</span></span> <span data-ttu-id="ebae5-113">Ottiene tutte le funzionalità di peering dirette.</span><span class="sxs-lookup"><span data-stu-id="ebae5-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="ebae5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ebae5-114">Example 2</span></span>
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

<span data-ttu-id="ebae5-115">Ottiene la posizione di peering di Exchange per Honolulu.</span><span class="sxs-lookup"><span data-stu-id="ebae5-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="ebae5-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ebae5-116">Example 3</span></span>
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

<span data-ttu-id="ebae5-117">Ottiene la posizione di peering di Exchange per l'ID della funzionalità peering 71.</span><span class="sxs-lookup"><span data-stu-id="ebae5-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="ebae5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ebae5-118">PARAMETERS</span></span>

### <span data-ttu-id="ebae5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebae5-119">-DefaultProfile</span></span>
<span data-ttu-id="ebae5-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebae5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebae5-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="ebae5-121">-DirectPeeringType</span></span>
<span data-ttu-id="ebae5-122">Selezionare "Edge", "CDN" e "Transit".</span><span class="sxs-lookup"><span data-stu-id="ebae5-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

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

### <span data-ttu-id="ebae5-123">-Tipo</span><span class="sxs-lookup"><span data-stu-id="ebae5-123">-Kind</span></span>
<span data-ttu-id="ebae5-124">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="ebae5-124">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="ebae5-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="ebae5-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="ebae5-126">ID della struttura PeeringDB.com</span><span class="sxs-lookup"><span data-stu-id="ebae5-126">The PeeringDB.com Facility ID</span></span>

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

### <span data-ttu-id="ebae5-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="ebae5-127">-PeeringLocation</span></span>
<span data-ttu-id="ebae5-128">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ebae5-128">The location of the resource.</span></span>

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

### <span data-ttu-id="ebae5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebae5-129">CommonParameters</span></span>
<span data-ttu-id="ebae5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebae5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebae5-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebae5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebae5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ebae5-132">INPUTS</span></span>

### <span data-ttu-id="ebae5-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ebae5-133">None</span></span>

## <span data-ttu-id="ebae5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebae5-134">OUTPUTS</span></span>

### <span data-ttu-id="ebae5-135">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="ebae5-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="ebae5-136">Note</span><span class="sxs-lookup"><span data-stu-id="ebae5-136">NOTES</span></span>

## <span data-ttu-id="ebae5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebae5-137">RELATED LINKS</span></span>
