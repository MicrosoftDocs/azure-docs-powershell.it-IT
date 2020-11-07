---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866298"
---
# <span data-ttu-id="9bcef-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9bcef-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="9bcef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bcef-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcef-103">Ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bcef-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bcef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bcef-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bcef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bcef-105">DESCRIPTION</span></span>
<span data-ttu-id="9bcef-106">Il cmdlet **Get-AzureRmApplicationGatewayFrontendIPConfig** ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bcef-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="9bcef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bcef-107">EXAMPLES</span></span>

### <span data-ttu-id="9bcef-108">Esempio 1: ottenere una configurazione IP front-end specificata</span><span class="sxs-lookup"><span data-stu-id="9bcef-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="9bcef-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la configurazione IP front-end denominata FrontEndIP01 da $AppGw e la archivia nella variabile $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="9bcef-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="9bcef-110">Esempio 2: ottenere un elenco di configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="9bcef-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="9bcef-111">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene un elenco delle configurazioni IP front-end da $AppGw e lo archivia nella variabile $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="9bcef-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="9bcef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bcef-112">PARAMETERS</span></span>

### <span data-ttu-id="9bcef-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bcef-113">-ApplicationGateway</span></span>
<span data-ttu-id="9bcef-114">Specifica l'oggetto gateway dell'applicazione che contiene la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="9bcef-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="9bcef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcef-115">-DefaultProfile</span></span>
<span data-ttu-id="9bcef-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bcef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bcef-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bcef-117">-Name</span></span>
<span data-ttu-id="9bcef-118">Specifica il nome della configurazione IP front-end ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bcef-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9bcef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcef-119">CommonParameters</span></span>
<span data-ttu-id="9bcef-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcef-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bcef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcef-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bcef-122">INPUTS</span></span>

### <span data-ttu-id="9bcef-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9bcef-123">System.String</span></span>

## <span data-ttu-id="9bcef-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bcef-124">OUTPUTS</span></span>

### <span data-ttu-id="9bcef-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bcef-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="9bcef-126">Note</span><span class="sxs-lookup"><span data-stu-id="9bcef-126">NOTES</span></span>

## <span data-ttu-id="9bcef-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bcef-127">RELATED LINKS</span></span>

[<span data-ttu-id="9bcef-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9bcef-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9bcef-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9bcef-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9bcef-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9bcef-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9bcef-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9bcef-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


