---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 901d8209cc18a5d64285bf45f7169d55d3c7a41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866868"
---
# <span data-ttu-id="ad47e-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad47e-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ad47e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad47e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad47e-103">Rimuove una configurazione IP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad47e-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad47e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad47e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad47e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad47e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad47e-106">Il cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** consente di rimuovere una configurazione IP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ad47e-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ad47e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad47e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad47e-108">Esempio 1: rimuovere una configurazione IP da un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="ad47e-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="ad47e-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ad47e-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ad47e-110">Il secondo comando rimuove la configurazione IP denominata Subnet02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ad47e-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ad47e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad47e-111">PARAMETERS</span></span>

### <span data-ttu-id="ad47e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad47e-112">-ApplicationGateway</span></span>
<span data-ttu-id="ad47e-113">Specifica il gateway dell'applicazione da cui rimuovere una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="ad47e-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="ad47e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad47e-114">-DefaultProfile</span></span>
<span data-ttu-id="ad47e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad47e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad47e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad47e-116">-Name</span></span>
<span data-ttu-id="ad47e-117">Specifica il nome della configurazione IP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ad47e-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad47e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad47e-118">CommonParameters</span></span>
<span data-ttu-id="ad47e-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad47e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad47e-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad47e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad47e-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad47e-121">INPUTS</span></span>

### <span data-ttu-id="ad47e-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ad47e-122">System.String</span></span>

## <span data-ttu-id="ad47e-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad47e-123">OUTPUTS</span></span>

### <span data-ttu-id="ad47e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad47e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ad47e-125">Note</span><span class="sxs-lookup"><span data-stu-id="ad47e-125">NOTES</span></span>

## <span data-ttu-id="ad47e-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad47e-126">RELATED LINKS</span></span>

[<span data-ttu-id="ad47e-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad47e-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ad47e-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad47e-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ad47e-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad47e-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ad47e-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad47e-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


