---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191004"
---
# <span data-ttu-id="eb009-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb009-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="eb009-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb009-102">SYNOPSIS</span></span>
<span data-ttu-id="eb009-103">Crea una risorsa della tabella route hub virtuale che è un elemento figlio di VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="eb009-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="eb009-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb009-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb009-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb009-105">DESCRIPTION</span></span>
<span data-ttu-id="eb009-106">La risorsa tabella route hub virtuale contiene l'elenco di route e un elenco di connessioni a cui può essere associato e viene usato per instradare il traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb009-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="eb009-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb009-107">EXAMPLES</span></span>

### <span data-ttu-id="eb009-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb009-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="eb009-109">Il comando precedente creerà una risorsa della tabella route hub virtuale dalle route passate e questo oggetto può essere usato per il routing del traffico in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb009-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="eb009-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb009-110">PARAMETERS</span></span>

### <span data-ttu-id="eb009-111">-Connessione</span><span class="sxs-lookup"><span data-stu-id="eb009-111">-Connection</span></span>
<span data-ttu-id="eb009-112">Elenco delle connessioni a cui è associata la tabella route.</span><span class="sxs-lookup"><span data-stu-id="eb009-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="eb009-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb009-113">-DefaultProfile</span></span>
<span data-ttu-id="eb009-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb009-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb009-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb009-115">-Name</span></span>
<span data-ttu-id="eb009-116">Nome della tabella di route.</span><span class="sxs-lookup"><span data-stu-id="eb009-116">Name of the route table.</span></span>

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

### <span data-ttu-id="eb009-117">-Route</span><span class="sxs-lookup"><span data-stu-id="eb009-117">-Route</span></span>
<span data-ttu-id="eb009-118">Elenco di route Hub virtuali.</span><span class="sxs-lookup"><span data-stu-id="eb009-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="eb009-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb009-119">CommonParameters</span></span>
<span data-ttu-id="eb009-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb009-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb009-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb009-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb009-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb009-122">INPUTS</span></span>

### <span data-ttu-id="eb009-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eb009-123">None</span></span>

## <span data-ttu-id="eb009-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb009-124">OUTPUTS</span></span>

### <span data-ttu-id="eb009-125">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb009-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="eb009-126">Note</span><span class="sxs-lookup"><span data-stu-id="eb009-126">NOTES</span></span>

## <span data-ttu-id="eb009-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb009-127">RELATED LINKS</span></span>