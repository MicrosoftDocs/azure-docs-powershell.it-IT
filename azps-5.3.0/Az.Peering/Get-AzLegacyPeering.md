---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475038"
---
# <span data-ttu-id="8fe82-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="8fe82-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="8fe82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fe82-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe82-103">Usato per convertire le risorse peer legacy in risorse di gestione delle risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="8fe82-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="8fe82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fe82-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fe82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe82-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe82-106">Il comando viene usato per visualizzare le risorse peer legacy che vengono convertite in risorse di gestione delle risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="8fe82-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="8fe82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fe82-107">EXAMPLES</span></span>

### <span data-ttu-id="8fe82-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8fe82-108">Example 1</span></span>
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

<span data-ttu-id="8fe82-109">Ottiene il peering legacy per Seattle</span><span class="sxs-lookup"><span data-stu-id="8fe82-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="8fe82-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fe82-110">PARAMETERS</span></span>

### <span data-ttu-id="8fe82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe82-111">-DefaultProfile</span></span>
<span data-ttu-id="8fe82-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fe82-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="8fe82-113">-Kind</span></span>
<span data-ttu-id="8fe82-114">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="8fe82-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="8fe82-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8fe82-115">-PeeringLocation</span></span>
<span data-ttu-id="8fe82-116">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="8fe82-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="8fe82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe82-117">CommonParameters</span></span>
<span data-ttu-id="8fe82-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe82-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fe82-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe82-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fe82-120">INPUTS</span></span>

### <span data-ttu-id="8fe82-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8fe82-121">None</span></span>

## <span data-ttu-id="8fe82-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fe82-122">OUTPUTS</span></span>

### <span data-ttu-id="8fe82-123">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="8fe82-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="8fe82-124">Note</span><span class="sxs-lookup"><span data-stu-id="8fe82-124">NOTES</span></span>

## <span data-ttu-id="8fe82-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fe82-125">RELATED LINKS</span></span>
