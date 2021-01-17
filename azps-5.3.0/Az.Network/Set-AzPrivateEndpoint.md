---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488877"
---
# <span data-ttu-id="f50e3-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f50e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f50e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f50e3-103">Aggiorna un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f50e3-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="f50e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f50e3-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f50e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f50e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f50e3-106">Il cmdlet **set-AzPrivateEndpoint** aggiorna un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f50e3-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="f50e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f50e3-107">EXAMPLES</span></span>

### <span data-ttu-id="f50e3-108">1: crea un endpoint privato e sostituisce una delle relative subnet a un'altra</span><span class="sxs-lookup"><span data-stu-id="f50e3-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="f50e3-109">Questo esempio crea un endpoint privato con una subnet, quindi viene sostituito in un'altra subnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f50e3-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f50e3-110">Il cmdlet Set-PrivateEndpoint viene quindi usato per scrivere lo stato dell'endpoint privato modificato sul lato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f50e3-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="f50e3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f50e3-111">PARAMETERS</span></span>

### <span data-ttu-id="f50e3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f50e3-112">-AsJob</span></span>
<span data-ttu-id="f50e3-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f50e3-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50e3-114">-DefaultProfile</span></span>
<span data-ttu-id="f50e3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f50e3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f50e3-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-116">-PrivateEndpoint</span></span>
<span data-ttu-id="f50e3-117">Specifica un oggetto endpoint privato che rappresenta lo stato in cui deve essere impostato l'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="f50e3-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f50e3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50e3-118">CommonParameters</span></span>
<span data-ttu-id="f50e3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f50e3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50e3-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f50e3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50e3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f50e3-121">INPUTS</span></span>

### <span data-ttu-id="f50e3-122">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f50e3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f50e3-123">OUTPUTS</span></span>

### <span data-ttu-id="f50e3-124">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f50e3-125">Note</span><span class="sxs-lookup"><span data-stu-id="f50e3-125">NOTES</span></span>

## <span data-ttu-id="f50e3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f50e3-126">RELATED LINKS</span></span>

[<span data-ttu-id="f50e3-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="f50e3-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="f50e3-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f50e3-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


