---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016173"
---
# <span data-ttu-id="93199-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="93199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93199-102">SYNOPSIS</span></span>
<span data-ttu-id="93199-103">Aggiorna un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="93199-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="93199-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93199-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93199-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93199-105">DESCRIPTION</span></span>
<span data-ttu-id="93199-106">Il cmdlet **Set-AzPrivateEndpoint** aggiorna un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="93199-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="93199-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93199-107">EXAMPLES</span></span>

### <span data-ttu-id="93199-108">1: crea un endpoint privato e sostituisce una delle sue subnet con un altro</span><span class="sxs-lookup"><span data-stu-id="93199-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="93199-109">Questo esempio crea un endpoint privato con una subnet e quindi viene sostituito con un'altra subnet dalla rappresentazione in memoria della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="93199-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="93199-110">Il Set-PrivateEndpoint cmdlet viene quindi usato per scrivere lo stato modificato dell'endpoint privato sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="93199-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="93199-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93199-111">PARAMETERS</span></span>

### <span data-ttu-id="93199-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93199-112">-AsJob</span></span>
<span data-ttu-id="93199-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="93199-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93199-114">-DefaultProfile</span></span>
<span data-ttu-id="93199-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93199-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93199-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-116">-PrivateEndpoint</span></span>
<span data-ttu-id="93199-117">Specifica un oggetto endpoint privato che rappresenta lo stato su cui deve essere impostato l'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="93199-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="93199-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93199-118">CommonParameters</span></span>
<span data-ttu-id="93199-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93199-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93199-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93199-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93199-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="93199-121">INPUTS</span></span>

### <span data-ttu-id="93199-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="93199-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93199-123">OUTPUTS</span></span>

### <span data-ttu-id="93199-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="93199-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="93199-125">NOTES</span></span>

## <span data-ttu-id="93199-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93199-126">RELATED LINKS</span></span>

[<span data-ttu-id="93199-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="93199-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="93199-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="93199-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


