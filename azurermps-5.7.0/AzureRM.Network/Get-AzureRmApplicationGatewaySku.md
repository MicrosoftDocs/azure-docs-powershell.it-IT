---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 425955dd9b39b78c599262f7681c97dd15c93fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509831"
---
# <span data-ttu-id="08e07-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="08e07-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="08e07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08e07-102">SYNOPSIS</span></span>
<span data-ttu-id="08e07-103">Ottiene l'USK di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08e07-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08e07-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08e07-105">DESCRIPTION</span></span>
<span data-ttu-id="08e07-106">Il cmdlet **Get-AzureRmApplicationGatewaySku** Ottiene l'unità di conservazione delle scorte (SKU) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08e07-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="08e07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08e07-107">EXAMPLES</span></span>

### <span data-ttu-id="08e07-108">Esempio 1: ottenere una SKU gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="08e07-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="08e07-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="08e07-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="08e07-110">Il secondo comando ottiene l'USK di un gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $SKU.</span><span class="sxs-lookup"><span data-stu-id="08e07-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="08e07-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08e07-111">PARAMETERS</span></span>

### <span data-ttu-id="08e07-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08e07-112">-ApplicationGateway</span></span>
<span data-ttu-id="08e07-113">Specifica l'oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08e07-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="08e07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e07-114">-DefaultProfile</span></span>
<span data-ttu-id="08e07-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08e07-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e07-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e07-116">CommonParameters</span></span>
<span data-ttu-id="08e07-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e07-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e07-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e07-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e07-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08e07-119">INPUTS</span></span>

### <span data-ttu-id="08e07-120">System. String</span><span class="sxs-lookup"><span data-stu-id="08e07-120">System.String</span></span>

## <span data-ttu-id="08e07-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08e07-121">OUTPUTS</span></span>

### <span data-ttu-id="08e07-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="08e07-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="08e07-123">Note</span><span class="sxs-lookup"><span data-stu-id="08e07-123">NOTES</span></span>

## <span data-ttu-id="08e07-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08e07-124">RELATED LINKS</span></span>

[<span data-ttu-id="08e07-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="08e07-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="08e07-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="08e07-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


