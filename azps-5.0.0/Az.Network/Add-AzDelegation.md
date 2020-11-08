---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: c915f2e95c8912a071fd949a6c231a1eff79b97b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193224"
---
# <span data-ttu-id="7e47b-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="7e47b-101">Add-AzDelegation</span></span>

## <span data-ttu-id="7e47b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e47b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e47b-103">Aggiunge una delega a una subnet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="7e47b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e47b-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e47b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e47b-105">DESCRIPTION</span></span>
<span data-ttu-id="7e47b-106">Il cmdlet **Add-AzDelegation** aggiunge una delega di servizio a una subnet di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e47b-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="7e47b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e47b-107">EXAMPLES</span></span>

### <span data-ttu-id="7e47b-108">Esempio 1: aggiunta di una delega</span><span class="sxs-lookup"><span data-stu-id="7e47b-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="7e47b-109">Il primo comando Recupera la rete virtuale in cui si trova la subnet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="7e47b-110">Il secondo comando isola la subnet di interesse, quella che si vuole delegare.</span><span class="sxs-lookup"><span data-stu-id="7e47b-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="7e47b-111">Il terzo comando aggiunge una delega alla subnet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="7e47b-112">Questo particolare esempio sarebbe utile quando si vuole abilitare SQL per creare endpoint di interfaccia nella subnet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="7e47b-113">Il comando finale Invia la subnet aggiornata al server per aggiornare effettivamente la subnet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="7e47b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e47b-114">PARAMETERS</span></span>

### <span data-ttu-id="7e47b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e47b-115">-DefaultProfile</span></span>
<span data-ttu-id="7e47b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e47b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e47b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e47b-117">-Name</span></span>
<span data-ttu-id="7e47b-118">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="7e47b-118">The name of the delegation</span></span>

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

### <span data-ttu-id="7e47b-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7e47b-119">-ServiceName</span></span>
<span data-ttu-id="7e47b-120">Nome del servizio a cui la subnet deve essere delegata</span><span class="sxs-lookup"><span data-stu-id="7e47b-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="7e47b-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7e47b-121">-Subnet</span></span>
<span data-ttu-id="7e47b-122">Subnet</span><span class="sxs-lookup"><span data-stu-id="7e47b-122">The subnet</span></span>

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

### <span data-ttu-id="7e47b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e47b-123">CommonParameters</span></span>
<span data-ttu-id="7e47b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e47b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e47b-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e47b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e47b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e47b-126">INPUTS</span></span>

### <span data-ttu-id="7e47b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7e47b-127">System.String</span></span>

### <span data-ttu-id="7e47b-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7e47b-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7e47b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e47b-129">OUTPUTS</span></span>

### <span data-ttu-id="7e47b-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7e47b-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7e47b-131">Note</span><span class="sxs-lookup"><span data-stu-id="7e47b-131">NOTES</span></span>

## <span data-ttu-id="7e47b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e47b-132">RELATED LINKS</span></span>

<span data-ttu-id="7e47b-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="7e47b-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>