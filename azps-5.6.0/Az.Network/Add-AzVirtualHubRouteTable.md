---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5cf2756297a932269f2aee87a248a1ba0eeed20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979742"
---
# <span data-ttu-id="50aa4-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="50aa4-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="50aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="50aa4-103">Crea una risorsa Tabella route hub virtuale figlio di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="50aa4-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="50aa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50aa4-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50aa4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="50aa4-106">La risorsa tabella delle route dell'hub virtuale contiene l'elenco dei percorsi e un elenco delle connessioni a cui può essere collegata e usata per instradare il traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="50aa4-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="50aa4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="50aa4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50aa4-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="50aa4-109">Il comando precedente crea una risorsa Tabella route hub virtuale dalle route passate a essa e questo oggetto può essere usato per il routing del traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="50aa4-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="50aa4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="50aa4-111">-Connessione</span><span class="sxs-lookup"><span data-stu-id="50aa4-111">-Connection</span></span>
<span data-ttu-id="50aa4-112">Elenco delle connessioni a cui è collegata questa tabella di route.</span><span class="sxs-lookup"><span data-stu-id="50aa4-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="50aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="50aa4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50aa4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50aa4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="50aa4-115">-Name</span></span>
<span data-ttu-id="50aa4-116">Nome della tabella di route.</span><span class="sxs-lookup"><span data-stu-id="50aa4-116">Name of the route table.</span></span>

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

### <span data-ttu-id="50aa4-117">-Route</span><span class="sxs-lookup"><span data-stu-id="50aa4-117">-Route</span></span>
<span data-ttu-id="50aa4-118">Elenco delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="50aa4-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50aa4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aa4-119">CommonParameters</span></span>
<span data-ttu-id="50aa4-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50aa4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aa4-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50aa4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aa4-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="50aa4-122">INPUTS</span></span>

### <span data-ttu-id="50aa4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50aa4-123">None</span></span>

## <span data-ttu-id="50aa4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50aa4-124">OUTPUTS</span></span>

### <span data-ttu-id="50aa4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="50aa4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="50aa4-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="50aa4-126">NOTES</span></span>

## <span data-ttu-id="50aa4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50aa4-127">RELATED LINKS</span></span>
