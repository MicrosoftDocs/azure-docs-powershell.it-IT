---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853341"
---
# <span data-ttu-id="faf02-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="faf02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faf02-102">SYNOPSIS</span></span>
<span data-ttu-id="faf02-103">Ottiene un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="faf02-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="faf02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faf02-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf02-105">DESCRIPTION</span></span>
<span data-ttu-id="faf02-106">Il cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** ottiene un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="faf02-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="faf02-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faf02-107">EXAMPLES</span></span>

### <span data-ttu-id="faf02-108">Esempio 1: ottenere un certificato di autenticazione specificato</span><span class="sxs-lookup"><span data-stu-id="faf02-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="faf02-109">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e lo archivia nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="faf02-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="faf02-110">Il secondo comando ottiene il certificato di autenticazione denominato Pool01 e lo archivia nella variabile $pool.</span><span class="sxs-lookup"><span data-stu-id="faf02-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="faf02-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faf02-111">PARAMETERS</span></span>

### <span data-ttu-id="faf02-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faf02-112">-ApplicationGateway</span></span>
<span data-ttu-id="faf02-113">Specifica il nome del gateway dell'applicazione per cui questo cmdlet ottiene un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="faf02-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="faf02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf02-114">-DefaultProfile</span></span>
<span data-ttu-id="faf02-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faf02-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf02-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="faf02-116">-Name</span></span>
<span data-ttu-id="faf02-117">Specifica il nome del certificato di autenticazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf02-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="faf02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf02-118">CommonParameters</span></span>
<span data-ttu-id="faf02-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf02-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faf02-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf02-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faf02-121">INPUTS</span></span>

### <span data-ttu-id="faf02-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faf02-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="faf02-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faf02-123">OUTPUTS</span></span>

### <span data-ttu-id="faf02-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="faf02-125">Note</span><span class="sxs-lookup"><span data-stu-id="faf02-125">NOTES</span></span>
* <span data-ttu-id="faf02-126">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="faf02-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="faf02-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faf02-127">RELATED LINKS</span></span>

[<span data-ttu-id="faf02-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="faf02-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="faf02-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="faf02-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="faf02-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


