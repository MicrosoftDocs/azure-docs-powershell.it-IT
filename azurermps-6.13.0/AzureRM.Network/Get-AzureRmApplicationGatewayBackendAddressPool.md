---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 05e71fc334ae45f8a74a4afbeaa33be5816b6532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520177"
---
# <span data-ttu-id="82c87-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="82c87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82c87-102">SYNOPSIS</span></span>
<span data-ttu-id="82c87-103">Ottiene un pool di indirizzi di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82c87-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82c87-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82c87-105">DESCRIPTION</span></span>

## <span data-ttu-id="82c87-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82c87-106">EXAMPLES</span></span>

### <span data-ttu-id="82c87-107">Esempio 1: ottenere un pool di server back-end specificato</span><span class="sxs-lookup"><span data-stu-id="82c87-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="82c87-108">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="82c87-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82c87-109">Il secondo comando ottiene il pool di indirizzi back-end associato $AppGw denominato Pool01 e lo archivia nella variabile $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="82c87-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="82c87-110">Esempio 2: ottenere un elenco di pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="82c87-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="82c87-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="82c87-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82c87-112">Il secondo comando ottiene un elenco dei pool di indirizzi back-end associati a $AppGw e archivia l'elenco nella variabile $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="82c87-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="82c87-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82c87-113">PARAMETERS</span></span>

### <span data-ttu-id="82c87-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c87-114">-ApplicationGateway</span></span>
<span data-ttu-id="82c87-115">Il cmdlet **Get-AzureRmApplicationGatewayBackendAddressPool** ottiene un pool di indirizzi back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="82c87-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="82c87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c87-116">-DefaultProfile</span></span>
<span data-ttu-id="82c87-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82c87-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82c87-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="82c87-118">-Name</span></span>
<span data-ttu-id="82c87-119">Specifica il nome del pool di indirizzi back-end che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="82c87-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c87-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c87-120">CommonParameters</span></span>
<span data-ttu-id="82c87-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c87-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c87-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c87-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c87-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82c87-123">INPUTS</span></span>

### <span data-ttu-id="82c87-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c87-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="82c87-125">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82c87-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="82c87-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82c87-126">OUTPUTS</span></span>

### <span data-ttu-id="82c87-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="82c87-128">Note</span><span class="sxs-lookup"><span data-stu-id="82c87-128">NOTES</span></span>

## <span data-ttu-id="82c87-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82c87-129">RELATED LINKS</span></span>

[<span data-ttu-id="82c87-130">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-130">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82c87-131">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-131">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82c87-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="82c87-133">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82c87-133">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


