---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986773"
---
# <span data-ttu-id="dd1b7-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="dd1b7-101">Add-AzDelegation</span></span>

## <span data-ttu-id="dd1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1b7-103">Aggiunge una delega a una subnet.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="dd1b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd1b7-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd1b7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1b7-106">Il cmdlet **Add-AzDelegation** aggiunge una delega del servizio a una subnet Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="dd1b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd1b7-107">EXAMPLES</span></span>

### <span data-ttu-id="dd1b7-108">Esempio 1: Aggiunta di una delega</span><span class="sxs-lookup"><span data-stu-id="dd1b7-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="dd1b7-109">Il primo comando recupera la rete virtuale su cui si trova la subnet.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="dd1b7-110">Il secondo comando isola la subnet di interesse, ovvero quella che si vuole delegare.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="dd1b7-111">Il terzo comando aggiunge una delega alla subnet.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="dd1b7-112">Questo esempio può risultare utile quando si vuole abilitare SQL di creare endpoint di interfaccia in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="dd1b7-113">Il comando finale invia la subnet aggiornata al server per aggiornare effettivamente la subnet.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="dd1b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd1b7-114">PARAMETERS</span></span>

### <span data-ttu-id="dd1b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1b7-115">-DefaultProfile</span></span>
<span data-ttu-id="dd1b7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1b7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dd1b7-117">-Name</span></span>
<span data-ttu-id="dd1b7-118">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="dd1b7-118">The name of the delegation</span></span>

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

### <span data-ttu-id="dd1b7-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dd1b7-119">-ServiceName</span></span>
<span data-ttu-id="dd1b7-120">Nome del servizio a cui deve essere delegata la subnet</span><span class="sxs-lookup"><span data-stu-id="dd1b7-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="dd1b7-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dd1b7-121">-Subnet</span></span>
<span data-ttu-id="dd1b7-122">La subnet</span><span class="sxs-lookup"><span data-stu-id="dd1b7-122">The subnet</span></span>

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

### <span data-ttu-id="dd1b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1b7-123">CommonParameters</span></span>
<span data-ttu-id="dd1b7-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1b7-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1b7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1b7-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd1b7-126">INPUTS</span></span>

### <span data-ttu-id="dd1b7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dd1b7-127">System.String</span></span>

### <span data-ttu-id="dd1b7-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dd1b7-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dd1b7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd1b7-129">OUTPUTS</span></span>

### <span data-ttu-id="dd1b7-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dd1b7-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dd1b7-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd1b7-131">NOTES</span></span>

## <span data-ttu-id="dd1b7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd1b7-132">RELATED LINKS</span></span>

<span data-ttu-id="dd1b7-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="dd1b7-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>