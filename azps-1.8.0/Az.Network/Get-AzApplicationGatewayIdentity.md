---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678601"
---
# <span data-ttu-id="26fa3-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="26fa3-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="26fa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="26fa3-103">Ottenere l'identità assegnata al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26fa3-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="26fa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26fa3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26fa3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="26fa3-106">Il cmdlet **Get-AzApplicationGatewayIdentity** Ottiene l'identità assegnata al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26fa3-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="26fa3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="26fa3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26fa3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="26fa3-109">In questo esempio viene illustrato come ottenere l'identità del gateway applicazione dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26fa3-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="26fa3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="26fa3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26fa3-111">-ApplicationGateway</span></span>
<span data-ttu-id="26fa3-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26fa3-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26fa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fa3-113">-DefaultProfile</span></span>
<span data-ttu-id="26fa3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26fa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fa3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fa3-115">CommonParameters</span></span>
<span data-ttu-id="26fa3-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fa3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fa3-117">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26fa3-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fa3-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26fa3-118">INPUTS</span></span>

### <span data-ttu-id="26fa3-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26fa3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26fa3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26fa3-120">OUTPUTS</span></span>

### <span data-ttu-id="26fa3-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="26fa3-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="26fa3-122">Note</span><span class="sxs-lookup"><span data-stu-id="26fa3-122">NOTES</span></span>

## <span data-ttu-id="26fa3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26fa3-123">RELATED LINKS</span></span>
