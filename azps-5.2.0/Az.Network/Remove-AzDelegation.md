---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356730"
---
# <span data-ttu-id="512b9-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="512b9-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="512b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="512b9-102">SYNOPSIS</span></span>
<span data-ttu-id="512b9-103">Rimuove una delega di servizio dalla subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="512b9-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="512b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="512b9-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="512b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="512b9-105">DESCRIPTION</span></span>
<span data-ttu-id="512b9-106">Il cmdlet **Remove-AzDelegation** accetta una subnet con le delegazioni e rimuove la delega denominata dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="512b9-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="512b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="512b9-107">EXAMPLES</span></span>

### <span data-ttu-id="512b9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="512b9-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="512b9-109">In questo esempio, la prima metà (trovata in _"aggiunta di una delega a una subnet esistente"_) è identica a [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="512b9-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="512b9-110">Nel secondo semestre i primi due cmdlet recuperano la subnet di interesse, aggiornando la copia locale con il server.</span><span class="sxs-lookup"><span data-stu-id="512b9-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="512b9-111">Il terzo cmdlet rimuove la delega creata nel primo semestre da _subnet_ e archivia la subnet aggiornata in _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="512b9-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="512b9-112">Il cmdlet finale aggiorna il server con la delega rimossa.</span><span class="sxs-lookup"><span data-stu-id="512b9-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="512b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="512b9-113">PARAMETERS</span></span>

### <span data-ttu-id="512b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512b9-114">-DefaultProfile</span></span>
<span data-ttu-id="512b9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="512b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="512b9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="512b9-116">-Name</span></span>
<span data-ttu-id="512b9-117">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="512b9-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512b9-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="512b9-118">-Subnet</span></span>
<span data-ttu-id="512b9-119">Subnet da cui rimuovere la delega</span><span class="sxs-lookup"><span data-stu-id="512b9-119">The subnet from which to remove the delegation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="512b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512b9-120">CommonParameters</span></span>
<span data-ttu-id="512b9-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512b9-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512b9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512b9-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="512b9-123">INPUTS</span></span>

### <span data-ttu-id="512b9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="512b9-124">System.String</span></span>

### <span data-ttu-id="512b9-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="512b9-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="512b9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="512b9-126">OUTPUTS</span></span>

### <span data-ttu-id="512b9-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="512b9-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="512b9-128">Note</span><span class="sxs-lookup"><span data-stu-id="512b9-128">NOTES</span></span>

## <span data-ttu-id="512b9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="512b9-129">RELATED LINKS</span></span>

<span data-ttu-id="512b9-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="512b9-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>