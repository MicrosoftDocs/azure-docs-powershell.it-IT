---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516224"
---
# <span data-ttu-id="f5860-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5860-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f5860-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5860-102">SYNOPSIS</span></span>
<span data-ttu-id="f5860-103">Rimuove una configurazione IP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5860-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5860-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5860-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5860-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5860-105">DESCRIPTION</span></span>
<span data-ttu-id="f5860-106">Il cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** consente di rimuovere una configurazione IP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f5860-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="f5860-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5860-107">EXAMPLES</span></span>

### <span data-ttu-id="f5860-108">Esempio 1: rimuovere una configurazione IP da un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="f5860-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="f5860-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f5860-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f5860-110">Il secondo comando rimuove la configurazione IP denominata Subnet02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f5860-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f5860-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5860-111">PARAMETERS</span></span>

### <span data-ttu-id="f5860-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5860-112">-ApplicationGateway</span></span>
<span data-ttu-id="f5860-113">Specifica il gateway dell'applicazione da cui rimuovere una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f5860-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="f5860-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5860-114">-Name</span></span>
<span data-ttu-id="f5860-115">Specifica il nome della configurazione IP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f5860-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="f5860-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5860-116">-DefaultProfile</span></span>
<span data-ttu-id="f5860-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5860-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5860-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5860-118">CommonParameters</span></span>
<span data-ttu-id="f5860-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5860-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5860-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5860-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5860-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5860-121">INPUTS</span></span>

### <span data-ttu-id="f5860-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f5860-122">System.String</span></span>

## <span data-ttu-id="f5860-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5860-123">OUTPUTS</span></span>

### <span data-ttu-id="f5860-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5860-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5860-125">Note</span><span class="sxs-lookup"><span data-stu-id="f5860-125">NOTES</span></span>

## <span data-ttu-id="f5860-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5860-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5860-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5860-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5860-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5860-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5860-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5860-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5860-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5860-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


