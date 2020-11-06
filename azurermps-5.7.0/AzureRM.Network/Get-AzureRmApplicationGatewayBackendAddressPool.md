---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 482e713a109a8ce202a832783c3f1e554ddb0e75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516728"
---
# <span data-ttu-id="d2c21-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d2c21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2c21-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c21-103">Ottiene un pool di indirizzi di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2c21-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2c21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2c21-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2c21-105">DESCRIPTION</span></span>

## <span data-ttu-id="d2c21-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2c21-106">EXAMPLES</span></span>

### <span data-ttu-id="d2c21-107">Esempio 1: ottenere un pool di server back-end specificato</span><span class="sxs-lookup"><span data-stu-id="d2c21-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d2c21-108">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d2c21-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d2c21-109">Il secondo comando ottiene il pool di indirizzi back-end associato $AppGw denominato Pool01 e lo archivia nella variabile $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="d2c21-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="d2c21-110">Esempio 2: ottenere un elenco di pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="d2c21-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="d2c21-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d2c21-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d2c21-112">Il secondo comando ottiene un elenco dei pool di indirizzi back-end associati a $AppGw e archivia l'elenco nella variabile $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="d2c21-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="d2c21-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2c21-113">PARAMETERS</span></span>

### <span data-ttu-id="d2c21-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c21-114">-ApplicationGateway</span></span>
<span data-ttu-id="d2c21-115">Il cmdlet **Get-AzureRmApplicationGatewayBackendAddressPool** ottiene un pool di indirizzi back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2c21-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="d2c21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c21-116">-DefaultProfile</span></span>
<span data-ttu-id="d2c21-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c21-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2c21-118">-Name</span></span>
<span data-ttu-id="d2c21-119">Specifica il nome del pool di indirizzi back-end che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="d2c21-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d2c21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c21-120">CommonParameters</span></span>
<span data-ttu-id="d2c21-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c21-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c21-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2c21-123">INPUTS</span></span>

### <span data-ttu-id="d2c21-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d2c21-124">System.String</span></span>

## <span data-ttu-id="d2c21-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2c21-125">OUTPUTS</span></span>

### <span data-ttu-id="d2c21-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d2c21-127">Note</span><span class="sxs-lookup"><span data-stu-id="d2c21-127">NOTES</span></span>

## <span data-ttu-id="d2c21-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2c21-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2c21-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d2c21-130">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d2c21-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d2c21-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d2c21-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


