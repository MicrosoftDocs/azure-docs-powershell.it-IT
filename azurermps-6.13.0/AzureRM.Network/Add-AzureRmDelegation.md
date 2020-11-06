---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520180"
---
# <span data-ttu-id="2ac37-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="2ac37-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="2ac37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ac37-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac37-103">Aggiunge una delega a una subnet.</span><span class="sxs-lookup"><span data-stu-id="2ac37-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ac37-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ac37-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac37-106">Il cmdlet **Add-AzureRmDelegation** aggiunge una delega di servizio a una subnet di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac37-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="2ac37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ac37-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac37-108">1: aggiunta di una delega</span><span class="sxs-lookup"><span data-stu-id="2ac37-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="2ac37-109">Il primo comando Recupera la rete virtuale in cui si trova la subnet.</span><span class="sxs-lookup"><span data-stu-id="2ac37-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="2ac37-110">Il secondo comando isola la subnet di interesse, quella che si vuole delegare.</span><span class="sxs-lookup"><span data-stu-id="2ac37-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="2ac37-111">Il terzo comando aggiunge una delega alla subnet.</span><span class="sxs-lookup"><span data-stu-id="2ac37-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="2ac37-112">Questo particolare esempio sarebbe utile quando si vuole abilitare SQL per creare endpoint di interfaccia nella subnet.</span><span class="sxs-lookup"><span data-stu-id="2ac37-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="2ac37-113">Il comando finale Invia la subnet aggiornata al server per aggiornare effettivamente la subnet.</span><span class="sxs-lookup"><span data-stu-id="2ac37-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="2ac37-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ac37-114">PARAMETERS</span></span>

### <span data-ttu-id="2ac37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac37-115">-DefaultProfile</span></span>
<span data-ttu-id="2ac37-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac37-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ac37-117">-Name</span></span>
<span data-ttu-id="2ac37-118">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="2ac37-118">The name of the delegation</span></span>

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

### <span data-ttu-id="2ac37-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2ac37-119">-ServiceName</span></span>
<span data-ttu-id="2ac37-120">Nome del servizio a cui la subnet deve essere delegata</span><span class="sxs-lookup"><span data-stu-id="2ac37-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac37-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="2ac37-121">-Subnet</span></span>
<span data-ttu-id="2ac37-122">Subnet</span><span class="sxs-lookup"><span data-stu-id="2ac37-122">The subnet</span></span>

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

### <span data-ttu-id="2ac37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac37-123">CommonParameters</span></span>
<span data-ttu-id="2ac37-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ac37-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac37-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac37-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ac37-126">INPUTS</span></span>

### <span data-ttu-id="2ac37-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac37-127">System.String</span></span>

### <span data-ttu-id="2ac37-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2ac37-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2ac37-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ac37-129">OUTPUTS</span></span>

### <span data-ttu-id="2ac37-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2ac37-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2ac37-131">Note</span><span class="sxs-lookup"><span data-stu-id="2ac37-131">NOTES</span></span>

## <span data-ttu-id="2ac37-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ac37-132">RELATED LINKS</span></span>
<span data-ttu-id="2ac37-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="2ac37-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
