---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867065"
---
# <span data-ttu-id="ec1cd-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ec1cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1cd-103">Ottiene un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec1cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec1cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="ec1cd-106">Il cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** ottiene un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ec1cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="ec1cd-108">1:</span><span class="sxs-lookup"><span data-stu-id="ec1cd-108">1:</span></span>
```

```

## <span data-ttu-id="ec1cd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-109">PARAMETERS</span></span>

### <span data-ttu-id="ec1cd-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec1cd-110">-ApplicationGateway</span></span>
<span data-ttu-id="ec1cd-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet ottiene un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="ec1cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1cd-112">-DefaultProfile</span></span>
<span data-ttu-id="ec1cd-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec1cd-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec1cd-114">-Name</span></span>
<span data-ttu-id="ec1cd-115">Specifica il nome del certificato di autenticazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ec1cd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1cd-116">CommonParameters</span></span>
<span data-ttu-id="ec1cd-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec1cd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1cd-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec1cd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1cd-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-119">INPUTS</span></span>

### <span data-ttu-id="ec1cd-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ec1cd-120">System.String</span></span>

## <span data-ttu-id="ec1cd-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec1cd-121">OUTPUTS</span></span>

### <span data-ttu-id="ec1cd-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ec1cd-123">Note</span><span class="sxs-lookup"><span data-stu-id="ec1cd-123">NOTES</span></span>
* <span data-ttu-id="ec1cd-124">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="ec1cd-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ec1cd-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec1cd-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec1cd-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ec1cd-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ec1cd-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ec1cd-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ec1cd-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


