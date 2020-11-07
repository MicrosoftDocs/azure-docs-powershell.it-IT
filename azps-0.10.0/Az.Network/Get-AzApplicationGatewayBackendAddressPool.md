---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860910"
---
# <span data-ttu-id="6452b-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6452b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6452b-102">SYNOPSIS</span></span>
<span data-ttu-id="6452b-103">Ottiene un pool di indirizzi di back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6452b-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="6452b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6452b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6452b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6452b-105">DESCRIPTION</span></span>

## <span data-ttu-id="6452b-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6452b-106">EXAMPLES</span></span>

### <span data-ttu-id="6452b-107">Esempio 1: ottenere un pool di server back-end specificato</span><span class="sxs-lookup"><span data-stu-id="6452b-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6452b-108">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6452b-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6452b-109">Il secondo comando ottiene il pool di indirizzi back-end associato $AppGw denominato Pool01 e lo archivia nella variabile $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="6452b-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="6452b-110">Esempio 2: ottenere un elenco di pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="6452b-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="6452b-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6452b-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6452b-112">Il secondo comando ottiene un elenco dei pool di indirizzi back-end associati a $AppGw e archivia l'elenco nella variabile $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="6452b-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="6452b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6452b-113">PARAMETERS</span></span>

### <span data-ttu-id="6452b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6452b-114">-ApplicationGateway</span></span>
<span data-ttu-id="6452b-115">Il cmdlet **Get-AzApplicationGatewayBackendAddressPool** ottiene un pool di indirizzi back-end per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6452b-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="6452b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6452b-116">-DefaultProfile</span></span>
<span data-ttu-id="6452b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6452b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6452b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6452b-118">-Name</span></span>
<span data-ttu-id="6452b-119">Specifica il nome del pool di indirizzi back-end che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="6452b-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6452b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6452b-120">CommonParameters</span></span>
<span data-ttu-id="6452b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6452b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6452b-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6452b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6452b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6452b-123">INPUTS</span></span>

### <span data-ttu-id="6452b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6452b-124">System.String</span></span>

## <span data-ttu-id="6452b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6452b-125">OUTPUTS</span></span>

### <span data-ttu-id="6452b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6452b-127">Note</span><span class="sxs-lookup"><span data-stu-id="6452b-127">NOTES</span></span>

## <span data-ttu-id="6452b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6452b-128">RELATED LINKS</span></span>

[<span data-ttu-id="6452b-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6452b-130">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6452b-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6452b-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6452b-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


