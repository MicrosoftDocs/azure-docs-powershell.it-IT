---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188462"
---
# <span data-ttu-id="814e2-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="814e2-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="814e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="814e2-102">SYNOPSIS</span></span>
<span data-ttu-id="814e2-103">Crea un oggetto VHubRoute che può essere passato come parametro al comando New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="814e2-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="814e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="814e2-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="814e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="814e2-105">DESCRIPTION</span></span>

<span data-ttu-id="814e2-106">Crea un oggetto VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="814e2-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="814e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="814e2-107">EXAMPLES</span></span>

### <span data-ttu-id="814e2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="814e2-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="814e2-109">Il comando precedente creerà un oggetto VHubRoute con nextHop come firewall specificato, che potrà quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="814e2-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="814e2-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="814e2-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="814e2-111">Il comando precedente creerà un oggetto VHubRoute con nextHop come hubVnetConnection specificato, che potrà quindi essere aggiunto a una risorsa VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="814e2-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="814e2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="814e2-112">PARAMETERS</span></span>

### <span data-ttu-id="814e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814e2-113">-DefaultProfile</span></span>
<span data-ttu-id="814e2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="814e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="814e2-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="814e2-115">-Destination</span></span>
<span data-ttu-id="814e2-116">Elenco di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="814e2-116">List of Destinations.</span></span>

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

### <span data-ttu-id="814e2-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="814e2-117">-DestinationType</span></span>
<span data-ttu-id="814e2-118">Tipo di destinazioni.</span><span class="sxs-lookup"><span data-stu-id="814e2-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="814e2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="814e2-119">-Name</span></span>
<span data-ttu-id="814e2-120">Nome della route.</span><span class="sxs-lookup"><span data-stu-id="814e2-120">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814e2-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="814e2-121">-NextHop</span></span>
<span data-ttu-id="814e2-122">L'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="814e2-122">The next hop.</span></span>

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

### <span data-ttu-id="814e2-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="814e2-123">-NextHopType</span></span>
<span data-ttu-id="814e2-124">Il tipo di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="814e2-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="814e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814e2-125">CommonParameters</span></span>
<span data-ttu-id="814e2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="814e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814e2-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="814e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814e2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="814e2-128">INPUTS</span></span>

### <span data-ttu-id="814e2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="814e2-129">System.String</span></span>

## <span data-ttu-id="814e2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="814e2-130">OUTPUTS</span></span>

### <span data-ttu-id="814e2-131">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="814e2-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="814e2-132">Note</span><span class="sxs-lookup"><span data-stu-id="814e2-132">NOTES</span></span>

## <span data-ttu-id="814e2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="814e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="814e2-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="814e2-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="814e2-135">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="814e2-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="814e2-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="814e2-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="814e2-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="814e2-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)