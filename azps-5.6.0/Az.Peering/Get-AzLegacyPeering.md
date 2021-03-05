---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 2f1bdfd317a5578c5ce3a023f1c3cd0151026b80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989615"
---
# <span data-ttu-id="a51c3-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="a51c3-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="a51c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a51c3-103">Consente di convertire le risorse peering legacy in risorse di Gestione ARM Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c3-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="a51c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a51c3-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a51c3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a51c3-105">DESCRIPTION</span></span>
<span data-ttu-id="a51c3-106">Il comando viene usato per visualizzare le risorse peering legacy, che verranno convertite in risorse di Gestione ARM Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c3-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="a51c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a51c3-107">EXAMPLES</span></span>

### <span data-ttu-id="a51c3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a51c3-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="a51c3-109">Ottiene il peering legacy per Seattle</span><span class="sxs-lookup"><span data-stu-id="a51c3-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="a51c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a51c3-110">PARAMETERS</span></span>

### <span data-ttu-id="a51c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51c3-111">-DefaultProfile</span></span>
<span data-ttu-id="a51c3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a51c3-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="a51c3-113">-Kind</span></span>
<span data-ttu-id="a51c3-114">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="a51c3-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51c3-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a51c3-115">-PeeringLocation</span></span>
<span data-ttu-id="a51c3-116">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="a51c3-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="a51c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51c3-117">CommonParameters</span></span>
<span data-ttu-id="a51c3-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51c3-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a51c3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51c3-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a51c3-120">INPUTS</span></span>

### <span data-ttu-id="a51c3-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a51c3-121">None</span></span>

## <span data-ttu-id="a51c3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a51c3-122">OUTPUTS</span></span>

### <span data-ttu-id="a51c3-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="a51c3-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a51c3-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="a51c3-124">NOTES</span></span>

## <span data-ttu-id="a51c3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a51c3-125">RELATED LINKS</span></span>
