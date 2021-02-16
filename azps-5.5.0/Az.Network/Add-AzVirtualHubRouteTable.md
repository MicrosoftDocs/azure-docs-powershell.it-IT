---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193943"
---
# <span data-ttu-id="fbeff-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fbeff-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="fbeff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbeff-102">SYNOPSIS</span></span>
<span data-ttu-id="fbeff-103">Crea una risorsa Tabella route hub virtuale figlio di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fbeff-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="fbeff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbeff-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbeff-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbeff-105">DESCRIPTION</span></span>
<span data-ttu-id="fbeff-106">La risorsa tabella delle route dell'hub virtuale contiene l'elenco dei percorsi e un elenco di connessioni a cui può essere collegata e usata per instradare il traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbeff-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="fbeff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbeff-107">EXAMPLES</span></span>

### <span data-ttu-id="fbeff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbeff-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="fbeff-109">Il comando precedente crea una risorsa Tabella route hub virtuale dalle route passate a essa e questo oggetto può essere usato per il routing del traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbeff-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="fbeff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbeff-110">PARAMETERS</span></span>

### <span data-ttu-id="fbeff-111">-Connessione</span><span class="sxs-lookup"><span data-stu-id="fbeff-111">-Connection</span></span>
<span data-ttu-id="fbeff-112">Elenco delle connessioni a cui è collegata questa tabella di route.</span><span class="sxs-lookup"><span data-stu-id="fbeff-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="fbeff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbeff-113">-DefaultProfile</span></span>
<span data-ttu-id="fbeff-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbeff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbeff-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fbeff-115">-Name</span></span>
<span data-ttu-id="fbeff-116">Nome della tabella di route.</span><span class="sxs-lookup"><span data-stu-id="fbeff-116">Name of the route table.</span></span>

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

### <span data-ttu-id="fbeff-117">-Route</span><span class="sxs-lookup"><span data-stu-id="fbeff-117">-Route</span></span>
<span data-ttu-id="fbeff-118">Elenco delle route dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbeff-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="fbeff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbeff-119">CommonParameters</span></span>
<span data-ttu-id="fbeff-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbeff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbeff-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbeff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbeff-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbeff-122">INPUTS</span></span>

### <span data-ttu-id="fbeff-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbeff-123">None</span></span>

## <span data-ttu-id="fbeff-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbeff-124">OUTPUTS</span></span>

### <span data-ttu-id="fbeff-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fbeff-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="fbeff-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbeff-126">NOTES</span></span>

## <span data-ttu-id="fbeff-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbeff-127">RELATED LINKS</span></span>
