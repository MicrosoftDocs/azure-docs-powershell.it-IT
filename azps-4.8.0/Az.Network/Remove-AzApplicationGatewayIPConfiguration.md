---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192068"
---
# <span data-ttu-id="9f5a7-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f5a7-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9f5a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5a7-103">Rimuove una configurazione IP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="9f5a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f5a7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="9f5a7-106">Il cmdlet **Remove-AzApplicationGatewayIPConfiguration** consente di rimuovere una configurazione IP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="9f5a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="9f5a7-108">Esempio 1: rimuovere una configurazione IP da un gateway dell'applicazione Azure</span><span class="sxs-lookup"><span data-stu-id="9f5a7-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="9f5a7-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9f5a7-110">Il secondo comando rimuove la configurazione IP denominata Subnet02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9f5a7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f5a7-111">PARAMETERS</span></span>

### <span data-ttu-id="9f5a7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f5a7-112">-ApplicationGateway</span></span>
<span data-ttu-id="9f5a7-113">Specifica il gateway dell'applicazione da cui rimuovere una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="9f5a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5a7-114">-DefaultProfile</span></span>
<span data-ttu-id="9f5a7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f5a7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f5a7-116">-Name</span></span>
<span data-ttu-id="9f5a7-117">Specifica il nome della configurazione IP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="9f5a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5a7-118">CommonParameters</span></span>
<span data-ttu-id="9f5a7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5a7-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5a7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5a7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f5a7-121">INPUTS</span></span>

### <span data-ttu-id="9f5a7-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f5a7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f5a7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f5a7-123">OUTPUTS</span></span>

### <span data-ttu-id="9f5a7-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f5a7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f5a7-125">Note</span><span class="sxs-lookup"><span data-stu-id="9f5a7-125">NOTES</span></span>

## <span data-ttu-id="9f5a7-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f5a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="9f5a7-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f5a7-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f5a7-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f5a7-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f5a7-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f5a7-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9f5a7-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f5a7-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


