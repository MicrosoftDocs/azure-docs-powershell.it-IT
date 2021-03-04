---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: d90d25776f895bee47549dfb08a4588f0e446883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979757"
---
# <span data-ttu-id="e8939-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e8939-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="e8939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8939-102">SYNOPSIS</span></span>
<span data-ttu-id="e8939-103">Crea un oggetto VirtualHubRoute che può essere passato come parametro al comando Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e8939-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="e8939-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8939-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8939-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8939-105">DESCRIPTION</span></span>
<span data-ttu-id="e8939-106">Crea un oggetto VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="e8939-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="e8939-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8939-107">EXAMPLES</span></span>

### <span data-ttu-id="e8939-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8939-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="e8939-109">Il comando precedente crea un oggetto VirtualHubRoute che può quindi essere aggiunto a una risorsa VirtualHubRouteTable e impostato su VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e8939-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="e8939-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8939-110">PARAMETERS</span></span>

### <span data-ttu-id="e8939-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8939-111">-DefaultProfile</span></span>
<span data-ttu-id="e8939-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8939-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8939-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="e8939-113">-Destination</span></span>
<span data-ttu-id="e8939-114">Elenco delle destinazioni.</span><span class="sxs-lookup"><span data-stu-id="e8939-114">List of Destinations.</span></span>

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

### <span data-ttu-id="e8939-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="e8939-115">-DestinationType</span></span>
<span data-ttu-id="e8939-116">Tipo di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="e8939-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="e8939-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="e8939-117">-NextHop</span></span>
<span data-ttu-id="e8939-118">Elenco dei passaggi successivi.</span><span class="sxs-lookup"><span data-stu-id="e8939-118">List of Next hops.</span></span>

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

### <span data-ttu-id="e8939-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e8939-119">-NextHopType</span></span>
<span data-ttu-id="e8939-120">Tipo di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="e8939-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="e8939-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8939-121">CommonParameters</span></span>
<span data-ttu-id="e8939-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8939-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8939-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8939-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8939-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8939-124">INPUTS</span></span>

### <span data-ttu-id="e8939-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e8939-125">None</span></span>

## <span data-ttu-id="e8939-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8939-126">OUTPUTS</span></span>

### <span data-ttu-id="e8939-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e8939-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="e8939-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8939-128">NOTES</span></span>

## <span data-ttu-id="e8939-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8939-129">RELATED LINKS</span></span>
