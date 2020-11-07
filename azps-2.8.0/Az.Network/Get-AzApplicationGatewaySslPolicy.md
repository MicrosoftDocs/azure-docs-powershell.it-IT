---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853805"
---
# <span data-ttu-id="e8c13-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8c13-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e8c13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8c13-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c13-103">Ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8c13-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e8c13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8c13-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8c13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8c13-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c13-106">Il cmdlet **Get-AzApplicationGatewaySslPolicy** ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e8c13-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e8c13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8c13-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c13-108">1:</span><span class="sxs-lookup"><span data-stu-id="e8c13-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e8c13-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8c13-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e8c13-110">Il secondo comando consente di ottenere i criteri SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e8c13-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="e8c13-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8c13-111">PARAMETERS</span></span>

### <span data-ttu-id="e8c13-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c13-112">-ApplicationGateway</span></span>
<span data-ttu-id="e8c13-113">Specifica il gateway dell'applicazione dei criteri SSL ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8c13-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e8c13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c13-114">-DefaultProfile</span></span>
<span data-ttu-id="e8c13-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c13-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8c13-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c13-116">CommonParameters</span></span>
<span data-ttu-id="e8c13-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c13-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c13-118">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8c13-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c13-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8c13-119">INPUTS</span></span>

### <span data-ttu-id="e8c13-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c13-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8c13-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8c13-121">OUTPUTS</span></span>

### <span data-ttu-id="e8c13-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8c13-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e8c13-123">Note</span><span class="sxs-lookup"><span data-stu-id="e8c13-123">NOTES</span></span>
* <span data-ttu-id="e8c13-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="e8c13-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e8c13-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8c13-125">RELATED LINKS</span></span>

[<span data-ttu-id="e8c13-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8c13-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e8c13-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8c13-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


