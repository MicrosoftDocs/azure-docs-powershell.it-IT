---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189711"
---
# <span data-ttu-id="53e42-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="53e42-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="53e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53e42-102">SYNOPSIS</span></span>
<span data-ttu-id="53e42-103">Visualizza la chiave condivisa usata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="53e42-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="53e42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53e42-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53e42-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53e42-105">DESCRIPTION</span></span>
<span data-ttu-id="53e42-106">Visualizza la chiave condivisa usata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="53e42-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="53e42-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53e42-107">EXAMPLES</span></span>

### <span data-ttu-id="53e42-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53e42-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="53e42-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53e42-109">PARAMETERS</span></span>

### <span data-ttu-id="53e42-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e42-110">-DefaultProfile</span></span>
<span data-ttu-id="53e42-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53e42-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53e42-112">-Name</span><span class="sxs-lookup"><span data-stu-id="53e42-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53e42-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53e42-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="53e42-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e42-114">CommonParameters</span></span>
<span data-ttu-id="53e42-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e42-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e42-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53e42-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e42-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="53e42-117">INPUTS</span></span>

### <span data-ttu-id="53e42-118">System.String</span><span class="sxs-lookup"><span data-stu-id="53e42-118">System.String</span></span>

## <span data-ttu-id="53e42-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53e42-119">OUTPUTS</span></span>

### <span data-ttu-id="53e42-120">System.String</span><span class="sxs-lookup"><span data-stu-id="53e42-120">System.String</span></span>

## <span data-ttu-id="53e42-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="53e42-121">NOTES</span></span>

## <span data-ttu-id="53e42-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53e42-122">RELATED LINKS</span></span>

[<span data-ttu-id="53e42-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="53e42-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="53e42-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="53e42-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
