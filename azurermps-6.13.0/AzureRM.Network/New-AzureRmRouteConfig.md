---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: ba5a389bd726822c24931fecb631f6c70cf7ce48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515040"
---
# <span data-ttu-id="d98f6-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d98f6-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="d98f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d98f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d98f6-103">Crea una route per una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d98f6-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d98f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d98f6-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d98f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d98f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d98f6-106">Il cmdlet **New-AzureRmRouteConfig** crea una route per una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="d98f6-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="d98f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d98f6-107">EXAMPLES</span></span>

### <span data-ttu-id="d98f6-108">Esempio 1: creare una route</span><span class="sxs-lookup"><span data-stu-id="d98f6-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="d98f6-109">Il primo comando crea una route denominata Route07 e la archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="d98f6-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="d98f6-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="d98f6-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="d98f6-111">Il secondo comando Visualizza le proprietà della route.</span><span class="sxs-lookup"><span data-stu-id="d98f6-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="d98f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d98f6-112">PARAMETERS</span></span>

### <span data-ttu-id="d98f6-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d98f6-113">-AddressPrefix</span></span>
<span data-ttu-id="d98f6-114">Specifica la destinazione, in formato CIDR (classe Interdomain Routing) a cui si applica la route.</span><span class="sxs-lookup"><span data-stu-id="d98f6-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="d98f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98f6-115">-DefaultProfile</span></span>
<span data-ttu-id="d98f6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d98f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d98f6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d98f6-117">-Name</span></span>
<span data-ttu-id="d98f6-118">Specifica un nome per la route.</span><span class="sxs-lookup"><span data-stu-id="d98f6-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="d98f6-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="d98f6-119">-NextHopIpAddress</span></span>
<span data-ttu-id="d98f6-120">Specifica l'indirizzo IP di un'appliance virtuale aggiunta alla rete Azurevirtual.</span><span class="sxs-lookup"><span data-stu-id="d98f6-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="d98f6-121">Questa route inoltra i pacchetti a quell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="d98f6-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="d98f6-122">Specifica questo parametro solo se specifichi un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="d98f6-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="d98f6-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="d98f6-123">-NextHopType</span></span>
<span data-ttu-id="d98f6-124">Specifica il modo in cui questa route inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d98f6-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="d98f6-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d98f6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d98f6-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="d98f6-126">Internet.</span></span>
<span data-ttu-id="d98f6-127">Il gateway Internet predefinito fornito da Azure.</span><span class="sxs-lookup"><span data-stu-id="d98f6-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="d98f6-128">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="d98f6-128">None.</span></span>
<span data-ttu-id="d98f6-129">Se specifichi questo valore, la route non inoltra i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d98f6-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="d98f6-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="d98f6-130">VirtualAppliance.</span></span>
<span data-ttu-id="d98f6-131">Un'appliance virtuale aggiunta alla rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="d98f6-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="d98f6-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="d98f6-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="d98f6-133">Un gateway di rete privata virtuale di Azure da server a server.</span><span class="sxs-lookup"><span data-stu-id="d98f6-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="d98f6-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="d98f6-134">VnetLocal.</span></span>
<span data-ttu-id="d98f6-135">Rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="d98f6-135">The local virtual network.</span></span>
<span data-ttu-id="d98f6-136">Se sono presenti due subnet, 10.1.0.0/16 e 10.2.0.0/16 nella stessa rete virtuale, selezionare un valore di VnetLocal per ogni subnet da inoltrare all'altra subnet.</span><span class="sxs-lookup"><span data-stu-id="d98f6-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="d98f6-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d98f6-137">-Confirm</span></span>
<span data-ttu-id="d98f6-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d98f6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98f6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98f6-139">-WhatIf</span></span>
<span data-ttu-id="d98f6-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d98f6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d98f6-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d98f6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98f6-142">CommonParameters</span></span>
<span data-ttu-id="d98f6-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98f6-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98f6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98f6-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d98f6-145">INPUTS</span></span>

### <span data-ttu-id="d98f6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d98f6-146">System.String</span></span>

## <span data-ttu-id="d98f6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d98f6-147">OUTPUTS</span></span>

### <span data-ttu-id="d98f6-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="d98f6-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="d98f6-149">Note</span><span class="sxs-lookup"><span data-stu-id="d98f6-149">NOTES</span></span>

## <span data-ttu-id="d98f6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d98f6-150">RELATED LINKS</span></span>

[<span data-ttu-id="d98f6-151">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d98f6-151">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="d98f6-152">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d98f6-152">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="d98f6-153">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d98f6-153">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="d98f6-154">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d98f6-154">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


