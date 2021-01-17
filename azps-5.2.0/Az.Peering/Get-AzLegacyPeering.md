---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: e7b5ef8ef41c66cc3c19fd5ebdcfd53ddcc6f3a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350179"
---
# <span data-ttu-id="0d2e4-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="0d2e4-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="0d2e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2e4-103">Usato per convertire le risorse peer legacy in risorse di gestione delle risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="0d2e4-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="0d2e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d2e4-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d2e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d2e4-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2e4-106">Il comando viene usato per visualizzare le risorse peer legacy che vengono convertite in risorse di gestione delle risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="0d2e4-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="0d2e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d2e4-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2e4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d2e4-108">Example 1</span></span>
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

<span data-ttu-id="0d2e4-109">Ottiene il peering legacy per Seattle</span><span class="sxs-lookup"><span data-stu-id="0d2e4-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="0d2e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d2e4-110">PARAMETERS</span></span>

### <span data-ttu-id="0d2e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2e4-111">-DefaultProfile</span></span>
<span data-ttu-id="0d2e4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d2e4-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="0d2e4-113">-Kind</span></span>
<span data-ttu-id="0d2e4-114">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="0d2e4-114">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="0d2e4-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0d2e4-115">-PeeringLocation</span></span>
<span data-ttu-id="0d2e4-116">Mostra tutte le risorse di peering per tipo.</span><span class="sxs-lookup"><span data-stu-id="0d2e4-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="0d2e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2e4-117">CommonParameters</span></span>
<span data-ttu-id="0d2e4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2e4-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d2e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2e4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d2e4-120">INPUTS</span></span>

### <span data-ttu-id="0d2e4-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0d2e4-121">None</span></span>

## <span data-ttu-id="0d2e4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d2e4-122">OUTPUTS</span></span>

### <span data-ttu-id="0d2e4-123">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="0d2e4-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="0d2e4-124">Note</span><span class="sxs-lookup"><span data-stu-id="0d2e4-124">NOTES</span></span>

## <span data-ttu-id="0d2e4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d2e4-125">RELATED LINKS</span></span>
