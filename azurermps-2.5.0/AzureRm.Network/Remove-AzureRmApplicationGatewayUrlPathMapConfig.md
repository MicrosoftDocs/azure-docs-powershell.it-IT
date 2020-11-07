---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866053"
---
# <span data-ttu-id="7981d-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7981d-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7981d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7981d-102">SYNOPSIS</span></span>
<span data-ttu-id="7981d-103">Rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="7981d-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7981d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7981d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7981d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7981d-105">DESCRIPTION</span></span>
<span data-ttu-id="7981d-106">Il cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="7981d-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7981d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7981d-107">EXAMPLES</span></span>

### <span data-ttu-id="7981d-108">1:</span><span class="sxs-lookup"><span data-stu-id="7981d-108">1:</span></span>
```

```

## <span data-ttu-id="7981d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7981d-109">PARAMETERS</span></span>

### <span data-ttu-id="7981d-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7981d-110">-ApplicationGateway</span></span>
<span data-ttu-id="7981d-111">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove la configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="7981d-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="7981d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7981d-112">-DefaultProfile</span></span>
<span data-ttu-id="7981d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7981d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7981d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7981d-114">-Name</span></span>
<span data-ttu-id="7981d-115">Specifica il nome della mappa percorso URL che questo cmdlet rimuove dal server back-end.</span><span class="sxs-lookup"><span data-stu-id="7981d-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="7981d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7981d-116">CommonParameters</span></span>
<span data-ttu-id="7981d-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7981d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7981d-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7981d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7981d-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7981d-119">INPUTS</span></span>

### <span data-ttu-id="7981d-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7981d-120">PSApplicationGateway</span></span>
<span data-ttu-id="7981d-121">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7981d-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7981d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7981d-122">OUTPUTS</span></span>

### <span data-ttu-id="7981d-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7981d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7981d-124">Note</span><span class="sxs-lookup"><span data-stu-id="7981d-124">NOTES</span></span>

## <span data-ttu-id="7981d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7981d-125">RELATED LINKS</span></span>

[<span data-ttu-id="7981d-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7981d-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7981d-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7981d-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7981d-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7981d-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7981d-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7981d-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


