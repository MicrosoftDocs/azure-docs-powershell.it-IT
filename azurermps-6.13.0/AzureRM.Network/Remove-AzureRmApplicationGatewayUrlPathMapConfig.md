---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510864"
---
# <span data-ttu-id="e2122-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2122-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e2122-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2122-102">SYNOPSIS</span></span>
<span data-ttu-id="e2122-103">Rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="e2122-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2122-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2122-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2122-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2122-105">DESCRIPTION</span></span>
<span data-ttu-id="e2122-106">Il cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="e2122-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e2122-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2122-107">EXAMPLES</span></span>

## <span data-ttu-id="e2122-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2122-108">PARAMETERS</span></span>

### <span data-ttu-id="e2122-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2122-109">-ApplicationGateway</span></span>
<span data-ttu-id="e2122-110">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove la configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="e2122-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="e2122-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2122-111">-DefaultProfile</span></span>
<span data-ttu-id="e2122-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2122-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2122-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2122-113">-Name</span></span>
<span data-ttu-id="e2122-114">Specifica il nome della mappa percorso URL che questo cmdlet rimuove dal server back-end.</span><span class="sxs-lookup"><span data-stu-id="e2122-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2122-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2122-115">CommonParameters</span></span>
<span data-ttu-id="e2122-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2122-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2122-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2122-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2122-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2122-118">INPUTS</span></span>

### <span data-ttu-id="e2122-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2122-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e2122-120">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2122-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e2122-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2122-121">OUTPUTS</span></span>

### <span data-ttu-id="e2122-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2122-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2122-123">Note</span><span class="sxs-lookup"><span data-stu-id="e2122-123">NOTES</span></span>

## <span data-ttu-id="e2122-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2122-124">RELATED LINKS</span></span>

[<span data-ttu-id="e2122-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2122-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2122-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2122-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2122-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2122-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2122-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2122-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


