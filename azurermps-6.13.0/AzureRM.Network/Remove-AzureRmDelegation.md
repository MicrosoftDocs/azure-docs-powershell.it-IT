---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687800"
---
# <span data-ttu-id="81a04-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="81a04-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="81a04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81a04-102">SYNOPSIS</span></span>
<span data-ttu-id="81a04-103">Rimuove una delega di servizio dalla subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="81a04-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81a04-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81a04-105">DESCRIPTION</span></span>
<span data-ttu-id="81a04-106">Il cmdlet **Remove-AzureRmDelegation** accetta una subnet con le delegazioni e rimuove la delega denominata dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="81a04-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="81a04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81a04-107">EXAMPLES</span></span>

### <span data-ttu-id="81a04-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81a04-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="81a04-109">In questo esempio, la prima metà (trovata in _"aggiunta di una delega a una subnet esistente"_ ) è identica a [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="81a04-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="81a04-110">Nel secondo semestre i primi due cmdlet recuperano la subnet di interesse, aggiornando la copia locale con il server.</span><span class="sxs-lookup"><span data-stu-id="81a04-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="81a04-111">Il terzo cmdlet rimuove la delega creata nel primo semestre da _subnet_ e archivia la subnet aggiornata in _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="81a04-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="81a04-112">Il cmdlet finale aggiorna il server con la delega rimossa.</span><span class="sxs-lookup"><span data-stu-id="81a04-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="81a04-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81a04-113">PARAMETERS</span></span>

### <span data-ttu-id="81a04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a04-114">-DefaultProfile</span></span>
<span data-ttu-id="81a04-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81a04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a04-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="81a04-116">-Name</span></span>
<span data-ttu-id="81a04-117">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="81a04-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a04-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81a04-118">-ServiceName</span></span>
<span data-ttu-id="81a04-119">Nome del servizio a cui la subnet deve essere delegata</span><span class="sxs-lookup"><span data-stu-id="81a04-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="81a04-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="81a04-120">-Subnet</span></span>
<span data-ttu-id="81a04-121">Subnet da cui rimuovere la delega</span><span class="sxs-lookup"><span data-stu-id="81a04-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="81a04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a04-122">CommonParameters</span></span>
<span data-ttu-id="81a04-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a04-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a04-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a04-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81a04-125">INPUTS</span></span>

### <span data-ttu-id="81a04-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="81a04-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="81a04-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81a04-127">System.String</span></span>
## <span data-ttu-id="81a04-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81a04-128">OUTPUTS</span></span>

### <span data-ttu-id="81a04-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="81a04-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="81a04-130">Note</span><span class="sxs-lookup"><span data-stu-id="81a04-130">NOTES</span></span>

## <span data-ttu-id="81a04-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81a04-131">RELATED LINKS</span></span>

<span data-ttu-id="81a04-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="81a04-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
