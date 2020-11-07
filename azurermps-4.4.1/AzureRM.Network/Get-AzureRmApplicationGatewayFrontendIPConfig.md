---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 071a6930ce7724c5db9d6bb21689ecb001a84424
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685673"
---
# <span data-ttu-id="24528-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24528-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="24528-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24528-102">SYNOPSIS</span></span>
<span data-ttu-id="24528-103">Ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24528-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24528-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24528-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24528-105">DESCRIPTION</span></span>
<span data-ttu-id="24528-106">Il cmdlet **Get-AzureRmApplicationGatewayFrontendIPConfig** ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24528-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="24528-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24528-107">EXAMPLES</span></span>

### <span data-ttu-id="24528-108">Esempio 1: ottenere una configurazione IP front-end specificata</span><span class="sxs-lookup"><span data-stu-id="24528-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="24528-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la configurazione IP front-end denominata FrontEndIP01 da $AppGw e la archivia nella variabile $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="24528-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="24528-110">Esempio 2: ottenere un elenco di configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="24528-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="24528-111">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene un elenco delle configurazioni IP front-end da $AppGw e lo archivia nella variabile $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="24528-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="24528-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24528-112">PARAMETERS</span></span>

### <span data-ttu-id="24528-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24528-113">-ApplicationGateway</span></span>
<span data-ttu-id="24528-114">Specifica l'oggetto gateway dell'applicazione che contiene la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="24528-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="24528-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="24528-115">-Name</span></span>
<span data-ttu-id="24528-116">Specifica il nome della configurazione IP front-end ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24528-116">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24528-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24528-117">-DefaultProfile</span></span>
<span data-ttu-id="24528-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24528-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24528-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24528-119">CommonParameters</span></span>
<span data-ttu-id="24528-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24528-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24528-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24528-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24528-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24528-122">INPUTS</span></span>

### <span data-ttu-id="24528-123">System. String</span><span class="sxs-lookup"><span data-stu-id="24528-123">System.String</span></span>

## <span data-ttu-id="24528-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24528-124">OUTPUTS</span></span>

### <span data-ttu-id="24528-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24528-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="24528-126">Note</span><span class="sxs-lookup"><span data-stu-id="24528-126">NOTES</span></span>

## <span data-ttu-id="24528-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24528-127">RELATED LINKS</span></span>

[<span data-ttu-id="24528-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24528-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24528-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24528-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24528-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24528-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="24528-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="24528-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

