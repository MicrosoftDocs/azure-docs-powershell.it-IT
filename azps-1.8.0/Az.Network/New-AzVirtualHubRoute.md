---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678228"
---
# <span data-ttu-id="28299-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="28299-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="28299-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28299-102">SYNOPSIS</span></span>
<span data-ttu-id="28299-103">Crea un oggetto Route hub virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="28299-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="28299-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28299-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28299-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28299-105">DESCRIPTION</span></span>
<span data-ttu-id="28299-106">Crea un oggetto Route hub virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="28299-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="28299-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28299-107">EXAMPLES</span></span>

### <span data-ttu-id="28299-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28299-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="28299-109">Il precedente creerà un oggetto Route hub virtuale che può essere incluso nella tabella route hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="28299-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="28299-110">La route Virtual Hub è un oggetto in memoria che può essere usato per creare un oggetto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="28299-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="28299-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28299-111">PARAMETERS</span></span>

### <span data-ttu-id="28299-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="28299-112">-AddressPrefix</span></span>
<span data-ttu-id="28299-113">Elenco dei prefissi degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="28299-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="28299-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28299-114">-DefaultProfile</span></span>
<span data-ttu-id="28299-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28299-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28299-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="28299-116">-NextHopIpAddress</span></span>
<span data-ttu-id="28299-117">L'hop successivo IpAddress.</span><span class="sxs-lookup"><span data-stu-id="28299-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="28299-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28299-118">CommonParameters</span></span>
<span data-ttu-id="28299-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28299-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28299-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28299-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28299-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28299-121">INPUTS</span></span>

### <span data-ttu-id="28299-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28299-122">None</span></span>

## <span data-ttu-id="28299-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28299-123">OUTPUTS</span></span>

### <span data-ttu-id="28299-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="28299-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="28299-125">Note</span><span class="sxs-lookup"><span data-stu-id="28299-125">NOTES</span></span>

## <span data-ttu-id="28299-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28299-126">RELATED LINKS</span></span>

[<span data-ttu-id="28299-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="28299-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)