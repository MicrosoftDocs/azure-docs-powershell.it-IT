---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860917"
---
# <span data-ttu-id="149a4-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="149a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="149a4-102">SYNOPSIS</span></span>
<span data-ttu-id="149a4-103">Ottiene un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="149a4-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="149a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="149a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="149a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="149a4-105">DESCRIPTION</span></span>
<span data-ttu-id="149a4-106">Il cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** ottiene un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="149a4-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="149a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="149a4-107">EXAMPLES</span></span>

### <span data-ttu-id="149a4-108">1:</span><span class="sxs-lookup"><span data-stu-id="149a4-108">1:</span></span>
```

```

## <span data-ttu-id="149a4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="149a4-109">PARAMETERS</span></span>

### <span data-ttu-id="149a4-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="149a4-110">-ApplicationGateway</span></span>
<span data-ttu-id="149a4-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet ottiene un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="149a4-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="149a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149a4-112">-DefaultProfile</span></span>
<span data-ttu-id="149a4-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="149a4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="149a4-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="149a4-114">-Name</span></span>
<span data-ttu-id="149a4-115">Specifica il nome del certificato di autenticazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="149a4-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="149a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149a4-116">CommonParameters</span></span>
<span data-ttu-id="149a4-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149a4-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="149a4-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149a4-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="149a4-119">INPUTS</span></span>

### <span data-ttu-id="149a4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="149a4-120">System.String</span></span>

## <span data-ttu-id="149a4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="149a4-121">OUTPUTS</span></span>

### <span data-ttu-id="149a4-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="149a4-123">Note</span><span class="sxs-lookup"><span data-stu-id="149a4-123">NOTES</span></span>
* <span data-ttu-id="149a4-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="149a4-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="149a4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="149a4-125">RELATED LINKS</span></span>

[<span data-ttu-id="149a4-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="149a4-127">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="149a4-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="149a4-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="149a4-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


