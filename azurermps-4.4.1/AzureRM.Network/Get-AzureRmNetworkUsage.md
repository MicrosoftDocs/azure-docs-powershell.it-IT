---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: c5bb92ad330b49ff015f21ae14fab42d6583305c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521587"
---
# <span data-ttu-id="8be21-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="8be21-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="8be21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8be21-102">SYNOPSIS</span></span>
<span data-ttu-id="8be21-103">Elenca gli usi di rete per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="8be21-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be21-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8be21-105">DESCRIPTION</span></span>
<span data-ttu-id="8be21-106">Il cmdlet Get-AzureRmNetworkUsage ottiene i limiti e l'utilizzo corrente per le risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="8be21-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="8be21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be21-107">EXAMPLES</span></span>

### <span data-ttu-id="8be21-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8be21-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="8be21-109">Ottiene i dati sull'utilizzo delle risorse nell'area di westcentralus</span><span class="sxs-lookup"><span data-stu-id="8be21-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="8be21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8be21-110">PARAMETERS</span></span>

### <span data-ttu-id="8be21-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8be21-111">-Location</span></span>
<span data-ttu-id="8be21-112">Posizione in cui viene eseguita la query sull'utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8be21-112">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="8be21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be21-113">-DefaultProfile</span></span>
<span data-ttu-id="8be21-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8be21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be21-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be21-115">CommonParameters</span></span>
<span data-ttu-id="8be21-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be21-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be21-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be21-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be21-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8be21-118">INPUTS</span></span>

### <span data-ttu-id="8be21-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8be21-119">System.String</span></span>

## <span data-ttu-id="8be21-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be21-120">OUTPUTS</span></span>

### <span data-ttu-id="8be21-121">Microsoft. Azure. Commands. Network. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="8be21-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="8be21-122">Note</span><span class="sxs-lookup"><span data-stu-id="8be21-122">NOTES</span></span>

## <span data-ttu-id="8be21-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be21-123">RELATED LINKS</span></span>

