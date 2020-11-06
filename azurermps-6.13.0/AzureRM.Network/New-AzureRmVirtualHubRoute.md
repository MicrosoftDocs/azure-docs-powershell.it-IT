---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519257"
---
# <span data-ttu-id="e1309-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e1309-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="e1309-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1309-102">SYNOPSIS</span></span>
<span data-ttu-id="e1309-103">Crea un oggetto Route hub virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="e1309-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1309-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1309-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1309-105">DESCRIPTION</span></span>
<span data-ttu-id="e1309-106">Crea un oggetto Route hub virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="e1309-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="e1309-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1309-107">EXAMPLES</span></span>

### <span data-ttu-id="e1309-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1309-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="e1309-109">Il precedente creerà un oggetto Route hub virtuale che può essere incluso nella tabella route hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1309-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="e1309-110">La route Virtual Hub è un oggetto in memoria che può essere usato per creare un oggetto VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e1309-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="e1309-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1309-111">PARAMETERS</span></span>

### <span data-ttu-id="e1309-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e1309-112">-AddressPrefix</span></span>
<span data-ttu-id="e1309-113">Elenco dei prefissi degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="e1309-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="e1309-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1309-114">-DefaultProfile</span></span>
<span data-ttu-id="e1309-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1309-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1309-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1309-116">-NextHopIpAddress</span></span>
<span data-ttu-id="e1309-117">L'hop successivo IpAddress.</span><span class="sxs-lookup"><span data-stu-id="e1309-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="e1309-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1309-118">CommonParameters</span></span>
<span data-ttu-id="e1309-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1309-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1309-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1309-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1309-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1309-121">INPUTS</span></span>

### <span data-ttu-id="e1309-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1309-122">None</span></span>

## <span data-ttu-id="e1309-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1309-123">OUTPUTS</span></span>

### <span data-ttu-id="e1309-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e1309-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="e1309-125">Note</span><span class="sxs-lookup"><span data-stu-id="e1309-125">NOTES</span></span>

## <span data-ttu-id="e1309-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1309-126">RELATED LINKS</span></span>
