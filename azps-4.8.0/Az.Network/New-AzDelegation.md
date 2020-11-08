---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190966"
---
# <span data-ttu-id="2cee7-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="2cee7-101">New-AzDelegation</span></span>

## <span data-ttu-id="2cee7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cee7-102">SYNOPSIS</span></span>
<span data-ttu-id="2cee7-103">Crea una delega di servizio.</span><span class="sxs-lookup"><span data-stu-id="2cee7-103">Creates a service delegation.</span></span>

## <span data-ttu-id="2cee7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cee7-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cee7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cee7-105">DESCRIPTION</span></span>
<span data-ttu-id="2cee7-106">Il cmdlet **New-AzDelegation** crea una delega del servizio che può essere aggiunta a una subnet.</span><span class="sxs-lookup"><span data-stu-id="2cee7-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="2cee7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cee7-107">EXAMPLES</span></span>

### <span data-ttu-id="2cee7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cee7-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="2cee7-109">Il primo cmdlet crea una delega che può essere aggiunta a una subnet e la archivia nella variabile $delegation.</span><span class="sxs-lookup"><span data-stu-id="2cee7-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="2cee7-110">Il secondo e il terzo cmdlet recuperano la subnet da delegare.</span><span class="sxs-lookup"><span data-stu-id="2cee7-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="2cee7-111">Il quarto cmdlet aggiunge la delega creata alla subnet di interesse e il cmdlet finale Invia la configurazione aggiornata al server.</span><span class="sxs-lookup"><span data-stu-id="2cee7-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="2cee7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cee7-112">PARAMETERS</span></span>

### <span data-ttu-id="2cee7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cee7-113">-DefaultProfile</span></span>
<span data-ttu-id="2cee7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cee7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cee7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cee7-115">-Name</span></span>
<span data-ttu-id="2cee7-116">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="2cee7-116">The name of the delegation</span></span>

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

### <span data-ttu-id="2cee7-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2cee7-117">-ServiceName</span></span>
<span data-ttu-id="2cee7-118">Nome del servizio a cui la subnet deve essere delegata</span><span class="sxs-lookup"><span data-stu-id="2cee7-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="2cee7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cee7-119">CommonParameters</span></span>
<span data-ttu-id="2cee7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cee7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cee7-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cee7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cee7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cee7-122">INPUTS</span></span>

### <span data-ttu-id="2cee7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2cee7-123">System.String</span></span>

## <span data-ttu-id="2cee7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cee7-124">OUTPUTS</span></span>

### <span data-ttu-id="2cee7-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="2cee7-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="2cee7-126">Note</span><span class="sxs-lookup"><span data-stu-id="2cee7-126">NOTES</span></span>

## <span data-ttu-id="2cee7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cee7-127">RELATED LINKS</span></span>

<span data-ttu-id="2cee7-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="2cee7-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>