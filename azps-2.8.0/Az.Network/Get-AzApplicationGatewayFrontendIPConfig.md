---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 88393e7c40ba9888602f144410263e7210a3db9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853826"
---
# <span data-ttu-id="912f5-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="912f5-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="912f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="912f5-102">SYNOPSIS</span></span>
<span data-ttu-id="912f5-103">Ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="912f5-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="912f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="912f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="912f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="912f5-105">DESCRIPTION</span></span>
<span data-ttu-id="912f5-106">Il cmdlet **Get-AzApplicationGatewayFrontendIPConfig** ottiene la configurazione IP front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="912f5-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="912f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="912f5-107">EXAMPLES</span></span>

### <span data-ttu-id="912f5-108">Esempio 1: ottenere una configurazione IP front-end specificata</span><span class="sxs-lookup"><span data-stu-id="912f5-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="912f5-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la configurazione IP front-end denominata FrontEndIP01 da $AppGw e la archivia nella variabile $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="912f5-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="912f5-110">Esempio 2: ottenere un elenco di configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="912f5-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="912f5-111">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene un elenco delle configurazioni IP front-end da $AppGw e lo archivia nella variabile $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="912f5-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="912f5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="912f5-112">PARAMETERS</span></span>

### <span data-ttu-id="912f5-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="912f5-113">-ApplicationGateway</span></span>
<span data-ttu-id="912f5-114">Specifica l'oggetto gateway dell'applicazione che contiene la configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="912f5-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="912f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912f5-115">-DefaultProfile</span></span>
<span data-ttu-id="912f5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="912f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912f5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="912f5-117">-Name</span></span>
<span data-ttu-id="912f5-118">Specifica il nome della configurazione IP front-end ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="912f5-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="912f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912f5-119">CommonParameters</span></span>
<span data-ttu-id="912f5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912f5-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="912f5-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912f5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="912f5-122">INPUTS</span></span>

### <span data-ttu-id="912f5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="912f5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="912f5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="912f5-124">OUTPUTS</span></span>

### <span data-ttu-id="912f5-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="912f5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="912f5-126">Note</span><span class="sxs-lookup"><span data-stu-id="912f5-126">NOTES</span></span>

## <span data-ttu-id="912f5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="912f5-127">RELATED LINKS</span></span>

[<span data-ttu-id="912f5-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="912f5-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="912f5-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="912f5-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="912f5-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="912f5-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="912f5-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="912f5-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


