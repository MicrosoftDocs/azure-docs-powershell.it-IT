---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853638"
---
# <span data-ttu-id="c6a09-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c6a09-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c6a09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6a09-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a09-103">Visualizza la chiave condivisa usata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c6a09-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="c6a09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6a09-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6a09-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a09-106">Visualizza la chiave condivisa usata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c6a09-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="c6a09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6a09-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a09-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6a09-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="c6a09-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6a09-109">PARAMETERS</span></span>

### <span data-ttu-id="c6a09-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a09-110">-DefaultProfile</span></span>
<span data-ttu-id="c6a09-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a09-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a09-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6a09-112">-Name</span></span>
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

### <span data-ttu-id="c6a09-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a09-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c6a09-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a09-114">CommonParameters</span></span>
<span data-ttu-id="c6a09-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a09-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a09-116">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6a09-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a09-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6a09-117">INPUTS</span></span>

### <span data-ttu-id="c6a09-118">System. String</span><span class="sxs-lookup"><span data-stu-id="c6a09-118">System.String</span></span>

## <span data-ttu-id="c6a09-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6a09-119">OUTPUTS</span></span>

### <span data-ttu-id="c6a09-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c6a09-120">System.String</span></span>

## <span data-ttu-id="c6a09-121">Note</span><span class="sxs-lookup"><span data-stu-id="c6a09-121">NOTES</span></span>

## <span data-ttu-id="c6a09-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6a09-122">RELATED LINKS</span></span>

[<span data-ttu-id="c6a09-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c6a09-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c6a09-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c6a09-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
