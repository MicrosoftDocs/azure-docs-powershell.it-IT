---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 07b7d0decd196fba9cbf0a813af4d252d01dfc8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678241"
---
# <span data-ttu-id="f4d77-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f4d77-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="f4d77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4d77-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d77-103">Crea una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="f4d77-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="f4d77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4d77-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4d77-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d77-106">Il cmdlet **New-AzRouteConfig** crea una route per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d77-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="f4d77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4d77-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d77-108">Esempio 1: creare una route</span><span class="sxs-lookup"><span data-stu-id="f4d77-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="f4d77-109">Il primo comando crea una route denominata Route07 e la archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="f4d77-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="f4d77-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="f4d77-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="f4d77-111">Il secondo comando Visualizza le proprietà della route.</span><span class="sxs-lookup"><span data-stu-id="f4d77-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="f4d77-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4d77-112">PARAMETERS</span></span>

### <span data-ttu-id="f4d77-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f4d77-113">-AddressPrefix</span></span>
<span data-ttu-id="f4d77-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="f4d77-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d77-115">-DefaultProfile</span></span>
<span data-ttu-id="f4d77-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d77-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4d77-117">-Name</span></span>
<span data-ttu-id="f4d77-118">Specifica un nome per la route.</span><span class="sxs-lookup"><span data-stu-id="f4d77-118">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4d77-119">-NextHopIpAddress</span></span>
<span data-ttu-id="f4d77-120">Specifica l'indirizzo IP di un'appliance virtuale aggiunta alla rete Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="f4d77-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="f4d77-121">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f4d77-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="f4d77-122">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="f4d77-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="f4d77-123">-NextHopType</span></span>
<span data-ttu-id="f4d77-124">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f4d77-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="f4d77-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4d77-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4d77-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="f4d77-126">Internet.</span></span>
<span data-ttu-id="f4d77-127">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d77-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="f4d77-128">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f4d77-128">None.</span></span>
<span data-ttu-id="f4d77-129">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f4d77-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="f4d77-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="f4d77-130">VirtualAppliance.</span></span>
<span data-ttu-id="f4d77-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d77-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="f4d77-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f4d77-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="f4d77-133">Un gateway di rete privata virtuale di Azure da server a server.</span><span class="sxs-lookup"><span data-stu-id="f4d77-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="f4d77-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="f4d77-134">VnetLocal.</span></span>
<span data-ttu-id="f4d77-135">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="f4d77-135">The local virtual network.</span></span>
<span data-ttu-id="f4d77-136">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="f4d77-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4d77-137">-Confirm</span></span>
<span data-ttu-id="f4d77-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4d77-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d77-139">-WhatIf</span></span>
<span data-ttu-id="f4d77-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4d77-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4d77-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4d77-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d77-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d77-142">CommonParameters</span></span>
<span data-ttu-id="f4d77-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d77-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d77-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d77-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d77-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4d77-145">INPUTS</span></span>

### <span data-ttu-id="f4d77-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d77-146">System.String</span></span>

## <span data-ttu-id="f4d77-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4d77-147">OUTPUTS</span></span>

### <span data-ttu-id="f4d77-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="f4d77-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="f4d77-149">Note</span><span class="sxs-lookup"><span data-stu-id="f4d77-149">NOTES</span></span>

## <span data-ttu-id="f4d77-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4d77-150">RELATED LINKS</span></span>

[<span data-ttu-id="f4d77-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f4d77-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="f4d77-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f4d77-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="f4d77-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f4d77-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="f4d77-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f4d77-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


