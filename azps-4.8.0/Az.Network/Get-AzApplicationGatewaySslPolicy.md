---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190448"
---
# <span data-ttu-id="8445e-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8445e-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8445e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8445e-102">SYNOPSIS</span></span>
<span data-ttu-id="8445e-103">Ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8445e-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="8445e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8445e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8445e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8445e-105">DESCRIPTION</span></span>
<span data-ttu-id="8445e-106">Il cmdlet **Get-AzApplicationGatewaySslPolicy** ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8445e-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="8445e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8445e-107">EXAMPLES</span></span>

### <span data-ttu-id="8445e-108">1:</span><span class="sxs-lookup"><span data-stu-id="8445e-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="8445e-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8445e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8445e-110">Il secondo comando consente di ottenere i criteri SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8445e-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8445e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8445e-111">PARAMETERS</span></span>

### <span data-ttu-id="8445e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8445e-112">-ApplicationGateway</span></span>
<span data-ttu-id="8445e-113">Specifica il gateway dell'applicazione dei criteri SSL ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8445e-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8445e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8445e-114">-DefaultProfile</span></span>
<span data-ttu-id="8445e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8445e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8445e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8445e-116">CommonParameters</span></span>
<span data-ttu-id="8445e-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8445e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8445e-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8445e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8445e-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8445e-119">INPUTS</span></span>

### <span data-ttu-id="8445e-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8445e-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8445e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8445e-121">OUTPUTS</span></span>

### <span data-ttu-id="8445e-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8445e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="8445e-123">Note</span><span class="sxs-lookup"><span data-stu-id="8445e-123">NOTES</span></span>
* <span data-ttu-id="8445e-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="8445e-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8445e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8445e-125">RELATED LINKS</span></span>

[<span data-ttu-id="8445e-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8445e-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="8445e-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="8445e-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


