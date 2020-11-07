---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860330"
---
# <span data-ttu-id="26bc5-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26bc5-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="26bc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="26bc5-103">Rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="26bc5-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26bc5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26bc5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="26bc5-106">Il cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="26bc5-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26bc5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="26bc5-108">1:</span><span class="sxs-lookup"><span data-stu-id="26bc5-108">1:</span></span>
```

```

## <span data-ttu-id="26bc5-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26bc5-109">PARAMETERS</span></span>

### <span data-ttu-id="26bc5-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26bc5-110">-ApplicationGateway</span></span>
<span data-ttu-id="26bc5-111">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove la configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="26bc5-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="26bc5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bc5-112">-DefaultProfile</span></span>
<span data-ttu-id="26bc5-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26bc5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26bc5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="26bc5-114">-Name</span></span>
<span data-ttu-id="26bc5-115">Specifica il nome della mappa percorso URL che questo cmdlet rimuove dal server back-end.</span><span class="sxs-lookup"><span data-stu-id="26bc5-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="26bc5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bc5-116">CommonParameters</span></span>
<span data-ttu-id="26bc5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bc5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26bc5-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26bc5-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bc5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26bc5-119">INPUTS</span></span>

### <span data-ttu-id="26bc5-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26bc5-120">PSApplicationGateway</span></span>
<span data-ttu-id="26bc5-121">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="26bc5-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="26bc5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26bc5-122">OUTPUTS</span></span>

### <span data-ttu-id="26bc5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26bc5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26bc5-124">Note</span><span class="sxs-lookup"><span data-stu-id="26bc5-124">NOTES</span></span>

## <span data-ttu-id="26bc5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26bc5-125">RELATED LINKS</span></span>

[<span data-ttu-id="26bc5-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26bc5-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26bc5-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26bc5-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26bc5-128">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26bc5-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26bc5-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26bc5-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


