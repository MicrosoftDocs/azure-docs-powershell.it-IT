---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 42553004f8d084496a1f4809bca408e0b4c62cef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990022"
---
# <span data-ttu-id="908ca-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="908ca-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="908ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908ca-102">SYNOPSIS</span></span>
<span data-ttu-id="908ca-103">Crea un oggetto Percorso hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="908ca-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="908ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="908ca-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="908ca-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="908ca-105">DESCRIPTION</span></span>
<span data-ttu-id="908ca-106">Crea un oggetto Percorso hub virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="908ca-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="908ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="908ca-107">EXAMPLES</span></span>

### <span data-ttu-id="908ca-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="908ca-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="908ca-109">Gli elementi descritti in precedenza creeranno un oggetto percorso dell'hub virtuale che può essere incluso nella tabella delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="908ca-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="908ca-110">La route dell'hub virtuale è un oggetto in memoria che può essere usato per creare un oggetto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="908ca-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="908ca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="908ca-111">PARAMETERS</span></span>

### <span data-ttu-id="908ca-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="908ca-112">-AddressPrefix</span></span>
<span data-ttu-id="908ca-113">Elenco dei prefissi di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="908ca-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908ca-114">-DefaultProfile</span></span>
<span data-ttu-id="908ca-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="908ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="908ca-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="908ca-116">-NextHopIpAddress</span></span>
<span data-ttu-id="908ca-117">The Next Hop IpAddress.</span><span class="sxs-lookup"><span data-stu-id="908ca-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="908ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908ca-118">CommonParameters</span></span>
<span data-ttu-id="908ca-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908ca-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908ca-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908ca-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="908ca-121">INPUTS</span></span>

### <span data-ttu-id="908ca-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="908ca-122">None</span></span>

## <span data-ttu-id="908ca-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="908ca-123">OUTPUTS</span></span>

### <span data-ttu-id="908ca-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="908ca-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="908ca-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="908ca-125">NOTES</span></span>

## <span data-ttu-id="908ca-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="908ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="908ca-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="908ca-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
