---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3a25db38f26fe1714035acebba1063303cdc0934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686493"
---
# <span data-ttu-id="3a239-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3a239-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3a239-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a239-102">SYNOPSIS</span></span>
<span data-ttu-id="3a239-103">Ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a239-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a239-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a239-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a239-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a239-105">DESCRIPTION</span></span>
<span data-ttu-id="3a239-106">Il cmdlet **Get-AzureRmApplicationGatewaySslPolicy** ottiene i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a239-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="3a239-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a239-107">EXAMPLES</span></span>

### <span data-ttu-id="3a239-108">1:</span><span class="sxs-lookup"><span data-stu-id="3a239-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="3a239-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3a239-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3a239-110">Il secondo comando consente di ottenere i criteri SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3a239-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="3a239-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a239-111">PARAMETERS</span></span>

### <span data-ttu-id="3a239-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a239-112">-ApplicationGateway</span></span>
<span data-ttu-id="3a239-113">Specifica il gateway dell'applicazione dei criteri SSL ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a239-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a239-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a239-114">-DefaultProfile</span></span>
<span data-ttu-id="3a239-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a239-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a239-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a239-116">CommonParameters</span></span>
<span data-ttu-id="3a239-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a239-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a239-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a239-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a239-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a239-119">INPUTS</span></span>

### <span data-ttu-id="3a239-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3a239-120">System.String</span></span>

## <span data-ttu-id="3a239-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a239-121">OUTPUTS</span></span>

### <span data-ttu-id="3a239-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3a239-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3a239-123">Note</span><span class="sxs-lookup"><span data-stu-id="3a239-123">NOTES</span></span>
* <span data-ttu-id="3a239-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="3a239-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3a239-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a239-125">RELATED LINKS</span></span>

[<span data-ttu-id="3a239-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3a239-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="3a239-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3a239-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


