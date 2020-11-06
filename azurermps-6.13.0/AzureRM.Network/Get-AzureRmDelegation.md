---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519724"
---
# <span data-ttu-id="3d694-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="3d694-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="3d694-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d694-102">SYNOPSIS</span></span>
<span data-ttu-id="3d694-103">Ottenere una delega (o tutte le delegazioni) in una subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="3d694-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d694-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d694-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d694-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d694-105">DESCRIPTION</span></span>
<span data-ttu-id="3d694-106">Il cmdlet **Get-AzureRmDelegation** ottiene la delega denominata da una subnet.</span><span class="sxs-lookup"><span data-stu-id="3d694-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="3d694-107">Se non viene assegnato un nome alla delega, verranno restituite tutte le delegazioni nella subnet specificata.</span><span class="sxs-lookup"><span data-stu-id="3d694-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="3d694-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d694-108">EXAMPLES</span></span>

### <span data-ttu-id="3d694-109">1: recupero di una delega specifica</span><span class="sxs-lookup"><span data-stu-id="3d694-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="3d694-110">La prima riga recupera la subnet di interesse.</span><span class="sxs-lookup"><span data-stu-id="3d694-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="3d694-111">La seconda riga Mostra le informazioni sulla delega per la delega denominata "delega".</span><span class="sxs-lookup"><span data-stu-id="3d694-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="3d694-112">2: recupero di tutte le delegazioni di subnet</span><span class="sxs-lookup"><span data-stu-id="3d694-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="3d694-113">La prima riga recupera la subnet di interesse.</span><span class="sxs-lookup"><span data-stu-id="3d694-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="3d694-114">La seconda riga archivia un elenco di tutte le delegazioni in _subnet_ nella variabile $Delegations.</span><span class="sxs-lookup"><span data-stu-id="3d694-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="3d694-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d694-115">PARAMETERS</span></span>

### <span data-ttu-id="3d694-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d694-116">-DefaultProfile</span></span>
<span data-ttu-id="3d694-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d694-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d694-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d694-118">-Name</span></span>
<span data-ttu-id="3d694-119">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="3d694-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d694-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3d694-120">-Subnet</span></span>
<span data-ttu-id="3d694-121">Subnet</span><span class="sxs-lookup"><span data-stu-id="3d694-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d694-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d694-122">CommonParameters</span></span>
<span data-ttu-id="3d694-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d694-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3d694-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d694-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d694-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d694-125">INPUTS</span></span>

### <span data-ttu-id="3d694-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3d694-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="3d694-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d694-127">OUTPUTS</span></span>

### <span data-ttu-id="3d694-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="3d694-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="3d694-129">Note</span><span class="sxs-lookup"><span data-stu-id="3d694-129">NOTES</span></span>

## <span data-ttu-id="3d694-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d694-130">RELATED LINKS</span></span>
<span data-ttu-id="3d694-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="3d694-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
