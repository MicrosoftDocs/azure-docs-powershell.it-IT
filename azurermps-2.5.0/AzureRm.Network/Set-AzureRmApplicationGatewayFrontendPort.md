---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 83c29e3c059664d7848fe66bd8ad7bcc005a8d47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866971"
---
# <span data-ttu-id="5b9e9-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5b9e9-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5b9e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9e9-103">Modifica una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b9e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b9e9-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b9e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="5b9e9-106">Il cmdlet **set-AzureRmApplicationGatewayFrontendPort** modifica una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="5b9e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b9e9-107">EXAMPLES</span></span>

### <span data-ttu-id="5b9e9-108">Esempio 1: impostare una porta di front-end gateway applicazione in 80</span><span class="sxs-lookup"><span data-stu-id="5b9e9-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5b9e9-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5b9e9-110">Il secondo comando modifica il gateway in $AppGw per usare la porta 80 per la porta front-end denominata FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="5b9e9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b9e9-111">PARAMETERS</span></span>

### <span data-ttu-id="5b9e9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b9e9-112">-ApplicationGateway</span></span>
<span data-ttu-id="5b9e9-113">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="5b9e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9e9-114">-DefaultProfile</span></span>
<span data-ttu-id="5b9e9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b9e9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b9e9-116">-Name</span></span>
<span data-ttu-id="5b9e9-117">Specifica il nome della porta front-end da modificare.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="5b9e9-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="5b9e9-118">-Port</span></span>
<span data-ttu-id="5b9e9-119">Specifica il numero di porta da usare per la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9e9-120">CommonParameters</span></span>
<span data-ttu-id="5b9e9-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b9e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9e9-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b9e9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9e9-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b9e9-123">INPUTS</span></span>

### <span data-ttu-id="5b9e9-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b9e9-124">PSApplicationGateway</span></span>
<span data-ttu-id="5b9e9-125">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5b9e9-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5b9e9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b9e9-126">OUTPUTS</span></span>

### <span data-ttu-id="5b9e9-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b9e9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b9e9-128">Note</span><span class="sxs-lookup"><span data-stu-id="5b9e9-128">NOTES</span></span>

## <span data-ttu-id="5b9e9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b9e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="5b9e9-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5b9e9-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5b9e9-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5b9e9-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5b9e9-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5b9e9-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5b9e9-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5b9e9-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
