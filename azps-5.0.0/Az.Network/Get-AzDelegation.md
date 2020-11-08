---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203340"
---
# <span data-ttu-id="bfe7f-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="bfe7f-101">Get-AzDelegation</span></span>

## <span data-ttu-id="bfe7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfe7f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe7f-103">Ottenere una delega (o tutte le delegazioni) in una subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="bfe7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfe7f-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfe7f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfe7f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe7f-106">Il cmdlet **Get-AzDelegation** ottiene la delega denominata da una subnet.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="bfe7f-107">Se non viene assegnato un nome alla delega, verranno restituite tutte le delegazioni nella subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="bfe7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfe7f-108">EXAMPLES</span></span>

### <span data-ttu-id="bfe7f-109">1: recupero di una delega specifica</span><span class="sxs-lookup"><span data-stu-id="bfe7f-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="bfe7f-110">La prima riga recupera la subnet di interesse.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="bfe7f-111">La seconda riga Mostra le informazioni sulla delega per la delega denominata "delega".</span><span class="sxs-lookup"><span data-stu-id="bfe7f-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="bfe7f-112">2: recupero di tutte le delegazioni di subnet</span><span class="sxs-lookup"><span data-stu-id="bfe7f-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="bfe7f-113">La prima riga recupera la subnet di interesse.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="bfe7f-114">La seconda riga archivia un elenco di tutte le delegazioni in _subnet_ nella variabile $Delegations.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="bfe7f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfe7f-115">PARAMETERS</span></span>

### <span data-ttu-id="bfe7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe7f-116">-DefaultProfile</span></span>
<span data-ttu-id="bfe7f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfe7f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfe7f-118">-Name</span></span>
<span data-ttu-id="bfe7f-119">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="bfe7f-119">The name of the delegation</span></span>

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

### <span data-ttu-id="bfe7f-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bfe7f-120">-Subnet</span></span>
<span data-ttu-id="bfe7f-121">Subnet</span><span class="sxs-lookup"><span data-stu-id="bfe7f-121">The subnet</span></span>

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

### <span data-ttu-id="bfe7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe7f-122">CommonParameters</span></span>
<span data-ttu-id="bfe7f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe7f-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfe7f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe7f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfe7f-125">INPUTS</span></span>

### <span data-ttu-id="bfe7f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bfe7f-126">System.String</span></span>

### <span data-ttu-id="bfe7f-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="bfe7f-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="bfe7f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfe7f-128">OUTPUTS</span></span>

### <span data-ttu-id="bfe7f-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="bfe7f-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="bfe7f-130">Note</span><span class="sxs-lookup"><span data-stu-id="bfe7f-130">NOTES</span></span>

## <span data-ttu-id="bfe7f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfe7f-131">RELATED LINKS</span></span>

<span data-ttu-id="bfe7f-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="bfe7f-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
