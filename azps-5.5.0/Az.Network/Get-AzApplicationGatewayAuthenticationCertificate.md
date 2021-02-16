---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 00d5d84f3f9895aec42f9728de6eec1bf2ff9b06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189919"
---
# <span data-ttu-id="64e69-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="64e69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64e69-102">SYNOPSIS</span></span>
<span data-ttu-id="64e69-103">Ottiene un certificato di autenticazione per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="64e69-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="64e69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64e69-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64e69-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64e69-105">DESCRIPTION</span></span>
<span data-ttu-id="64e69-106">Il cmdlet **Get-AzApplicationGatewayAuthenticationCertificate ottiene** un certificato di autenticazione per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="64e69-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="64e69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64e69-107">EXAMPLES</span></span>

### <span data-ttu-id="64e69-108">Esempio 1: Ottenere un certificato di autenticazione specificato</span><span class="sxs-lookup"><span data-stu-id="64e69-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="64e69-109">Il primo comando recupera il gateway applicazione denominato appGwName e lo archivia nella $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="64e69-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="64e69-110">Il secondo comando recupera il certificato di autenticazione denominato cert01 e lo archivia nella $cert variabile.</span><span class="sxs-lookup"><span data-stu-id="64e69-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="64e69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64e69-111">PARAMETERS</span></span>

### <span data-ttu-id="64e69-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64e69-112">-ApplicationGateway</span></span>
<span data-ttu-id="64e69-113">Specifica il nome del gateway applicazione per cui questo cmdlet riceve un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="64e69-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="64e69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e69-114">-DefaultProfile</span></span>
<span data-ttu-id="64e69-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64e69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64e69-116">-Name</span><span class="sxs-lookup"><span data-stu-id="64e69-116">-Name</span></span>
<span data-ttu-id="64e69-117">Specifica il nome del certificato di autenticazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64e69-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="64e69-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e69-118">CommonParameters</span></span>
<span data-ttu-id="64e69-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64e69-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e69-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64e69-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e69-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="64e69-121">INPUTS</span></span>

### <span data-ttu-id="64e69-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64e69-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="64e69-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64e69-123">OUTPUTS</span></span>

### <span data-ttu-id="64e69-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="64e69-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="64e69-125">NOTES</span></span>
* <span data-ttu-id="64e69-126">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="64e69-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="64e69-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64e69-127">RELATED LINKS</span></span>

[<span data-ttu-id="64e69-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="64e69-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="64e69-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="64e69-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="64e69-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


