---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020499"
---
# <span data-ttu-id="fef23-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="fef23-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="fef23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fef23-102">SYNOPSIS</span></span>
<span data-ttu-id="fef23-103">Crea un oggetto VirtualHubRoute che può essere passato come parametro al comando Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="fef23-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="fef23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fef23-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fef23-105">DESCRIPTION</span></span>
<span data-ttu-id="fef23-106">Crea un oggetto VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="fef23-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="fef23-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fef23-107">EXAMPLES</span></span>

### <span data-ttu-id="fef23-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fef23-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="fef23-109">Il comando precedente creerà un oggetto VirtualHubRoute che potrà quindi essere aggiunto a una risorsa VirtualHubRouteTable e impostato su un VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fef23-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="fef23-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fef23-110">PARAMETERS</span></span>

### <span data-ttu-id="fef23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef23-111">-DefaultProfile</span></span>
<span data-ttu-id="fef23-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fef23-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef23-113">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="fef23-113">-Destination</span></span>
<span data-ttu-id="fef23-114">Elenco di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="fef23-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef23-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="fef23-115">-DestinationType</span></span>
<span data-ttu-id="fef23-116">Tipo di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="fef23-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef23-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="fef23-117">-NextHop</span></span>
<span data-ttu-id="fef23-118">Elenco dei passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="fef23-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef23-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="fef23-119">-NextHopType</span></span>
<span data-ttu-id="fef23-120">Il tipo di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="fef23-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef23-121">CommonParameters</span></span>
<span data-ttu-id="fef23-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef23-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fef23-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef23-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fef23-124">INPUTS</span></span>

### <span data-ttu-id="fef23-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fef23-125">None</span></span>

## <span data-ttu-id="fef23-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fef23-126">OUTPUTS</span></span>

### <span data-ttu-id="fef23-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="fef23-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="fef23-128">Note</span><span class="sxs-lookup"><span data-stu-id="fef23-128">NOTES</span></span>

## <span data-ttu-id="fef23-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fef23-129">RELATED LINKS</span></span>
