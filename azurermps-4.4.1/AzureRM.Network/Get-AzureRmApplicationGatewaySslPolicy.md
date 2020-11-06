---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 29f9d1b13704f190a94bffaa70b900bc5a3b29e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520034"
---
# <span data-ttu-id="c3723-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3723-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c3723-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3723-102">SYNOPSIS</span></span>
<span data-ttu-id="c3723-103">Ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3723-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3723-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3723-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3723-105">DESCRIPTION</span></span>
<span data-ttu-id="c3723-106">Il cmdlet **Get-AzureRmApplicationGatewaySslPolicy** ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3723-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="c3723-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3723-107">EXAMPLES</span></span>

### <span data-ttu-id="c3723-108">1:</span><span class="sxs-lookup"><span data-stu-id="c3723-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="c3723-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c3723-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c3723-110">Il secondo comando consente di ottenere i criteri SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c3723-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c3723-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3723-111">PARAMETERS</span></span>

### <span data-ttu-id="c3723-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3723-112">-ApplicationGateway</span></span>
<span data-ttu-id="c3723-113">Specifica il gateway dell'applicazione dei criteri SSL ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3723-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3723-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3723-114">-DefaultProfile</span></span>
<span data-ttu-id="c3723-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3723-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3723-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3723-116">CommonParameters</span></span>
<span data-ttu-id="c3723-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3723-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3723-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3723-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3723-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3723-119">INPUTS</span></span>

### <span data-ttu-id="c3723-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c3723-120">System.String</span></span>

## <span data-ttu-id="c3723-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3723-121">OUTPUTS</span></span>

### <span data-ttu-id="c3723-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3723-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c3723-123">Note</span><span class="sxs-lookup"><span data-stu-id="c3723-123">NOTES</span></span>
* <span data-ttu-id="c3723-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="c3723-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c3723-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3723-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3723-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3723-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c3723-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3723-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


