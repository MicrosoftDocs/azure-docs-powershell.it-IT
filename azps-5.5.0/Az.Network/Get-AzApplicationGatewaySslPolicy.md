---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191999"
---
# <span data-ttu-id="214c2-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="214c2-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="214c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214c2-102">SYNOPSIS</span></span>
<span data-ttu-id="214c2-103">Ottiene i criteri SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="214c2-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="214c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="214c2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="214c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="214c2-105">DESCRIPTION</span></span>
<span data-ttu-id="214c2-106">Il cmdlet **Get-AzApplicationGatewaySslPolicy** ottiene il criterio SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="214c2-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="214c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="214c2-107">EXAMPLES</span></span>

### <span data-ttu-id="214c2-108">1:</span><span class="sxs-lookup"><span data-stu-id="214c2-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="214c2-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="214c2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="214c2-110">Il secondo comando recupera i criteri SSL dal Gateway applicazione archiviati nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="214c2-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="214c2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="214c2-111">PARAMETERS</span></span>

### <span data-ttu-id="214c2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="214c2-112">-ApplicationGateway</span></span>
<span data-ttu-id="214c2-113">Specifica il gateway applicazione del criterio SSL che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214c2-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="214c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214c2-114">-DefaultProfile</span></span>
<span data-ttu-id="214c2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="214c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="214c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214c2-116">CommonParameters</span></span>
<span data-ttu-id="214c2-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214c2-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="214c2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214c2-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="214c2-119">INPUTS</span></span>

### <span data-ttu-id="214c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="214c2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="214c2-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="214c2-121">OUTPUTS</span></span>

### <span data-ttu-id="214c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="214c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="214c2-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="214c2-123">NOTES</span></span>
* <span data-ttu-id="214c2-124">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="214c2-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="214c2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="214c2-125">RELATED LINKS</span></span>

[<span data-ttu-id="214c2-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="214c2-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="214c2-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="214c2-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


