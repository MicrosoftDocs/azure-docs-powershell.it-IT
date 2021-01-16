---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331516"
---
# <span data-ttu-id="ad04e-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="ad04e-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="ad04e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad04e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad04e-103">Elenca gli usi di rete per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="ad04e-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="ad04e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad04e-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad04e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad04e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad04e-106">Il cmdlet Get-AzNetworkUsage ottiene i limiti e l'utilizzo corrente per le risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="ad04e-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="ad04e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad04e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad04e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad04e-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="ad04e-109">Ottiene i dati sull'utilizzo delle risorse nell'area di westcentralus</span><span class="sxs-lookup"><span data-stu-id="ad04e-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="ad04e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad04e-110">PARAMETERS</span></span>

### <span data-ttu-id="ad04e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad04e-111">-DefaultProfile</span></span>
<span data-ttu-id="ad04e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad04e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad04e-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad04e-113">-Location</span></span>
<span data-ttu-id="ad04e-114">Posizione in cui viene eseguita la query sull'utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ad04e-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad04e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad04e-115">CommonParameters</span></span>
<span data-ttu-id="ad04e-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad04e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad04e-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad04e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad04e-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad04e-118">INPUTS</span></span>

### <span data-ttu-id="ad04e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ad04e-119">System.String</span></span>

## <span data-ttu-id="ad04e-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad04e-120">OUTPUTS</span></span>

### <span data-ttu-id="ad04e-121">Microsoft. Azure. Commands. Network. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="ad04e-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="ad04e-122">Note</span><span class="sxs-lookup"><span data-stu-id="ad04e-122">NOTES</span></span>

## <span data-ttu-id="ad04e-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad04e-123">RELATED LINKS</span></span>
