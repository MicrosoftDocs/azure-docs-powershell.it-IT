---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865917"
---
# <span data-ttu-id="f7efa-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7efa-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f7efa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7efa-102">SYNOPSIS</span></span>
<span data-ttu-id="f7efa-103">Ottiene una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f7efa-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7efa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7efa-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7efa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7efa-105">DESCRIPTION</span></span>
<span data-ttu-id="f7efa-106">Il cmdlet **Get-AzureRmApplicationGatewayURLPathMapConfig** ottiene una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f7efa-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f7efa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7efa-107">EXAMPLES</span></span>

### <span data-ttu-id="f7efa-108">Esempio 1: ottenere una configurazione della mappa percorso URL</span><span class="sxs-lookup"><span data-stu-id="f7efa-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="f7efa-109">Questo comando consente di ottenere le configurazioni della mappa percorso URL dal server back-end situato nel gateway dell'applicazione denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="f7efa-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="f7efa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7efa-110">PARAMETERS</span></span>

### <span data-ttu-id="f7efa-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7efa-111">-ApplicationGateway</span></span>
<span data-ttu-id="f7efa-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="f7efa-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="f7efa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7efa-113">-DefaultProfile</span></span>
<span data-ttu-id="f7efa-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7efa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7efa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7efa-115">-Name</span></span>
<span data-ttu-id="f7efa-116">Specifica il nome della mappa percorso URL in cui questo cmdlet ottiene la configurazione della mappa di percorso.</span><span class="sxs-lookup"><span data-stu-id="f7efa-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7efa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7efa-117">CommonParameters</span></span>
<span data-ttu-id="f7efa-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7efa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7efa-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7efa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7efa-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7efa-120">INPUTS</span></span>

### <span data-ttu-id="f7efa-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7efa-121">PSApplicationGateway</span></span>
<span data-ttu-id="f7efa-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f7efa-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f7efa-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7efa-123">OUTPUTS</span></span>

### <span data-ttu-id="f7efa-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f7efa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="f7efa-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="f7efa-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="f7efa-126">Note</span><span class="sxs-lookup"><span data-stu-id="f7efa-126">NOTES</span></span>

## <span data-ttu-id="f7efa-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7efa-127">RELATED LINKS</span></span>

[<span data-ttu-id="f7efa-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7efa-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f7efa-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7efa-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f7efa-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7efa-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f7efa-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7efa-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


