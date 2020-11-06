---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518935"
---
# <span data-ttu-id="e76e4-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e76e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e76e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e76e4-103">Ottiene un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e76e4-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e76e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e76e4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e76e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e76e4-105">DESCRIPTION</span></span>
<span data-ttu-id="e76e4-106">Il cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** ottiene un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e76e4-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e76e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e76e4-107">EXAMPLES</span></span>

## <span data-ttu-id="e76e4-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e76e4-108">PARAMETERS</span></span>

### <span data-ttu-id="e76e4-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e76e4-109">-ApplicationGateway</span></span>
<span data-ttu-id="e76e4-110">Specifica il nome del gateway dell'applicazione per cui questo cmdlet ottiene un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e76e4-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="e76e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76e4-111">-DefaultProfile</span></span>
<span data-ttu-id="e76e4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e76e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e76e4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e76e4-113">-Name</span></span>
<span data-ttu-id="e76e4-114">Specifica il nome del certificato di autenticazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e76e4-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e76e4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76e4-115">CommonParameters</span></span>
<span data-ttu-id="e76e4-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e76e4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76e4-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e76e4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76e4-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e76e4-118">INPUTS</span></span>

### <span data-ttu-id="e76e4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e76e4-119">System.String</span></span>

## <span data-ttu-id="e76e4-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e76e4-120">OUTPUTS</span></span>

### <span data-ttu-id="e76e4-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e76e4-122">Note</span><span class="sxs-lookup"><span data-stu-id="e76e4-122">NOTES</span></span>
* <span data-ttu-id="e76e4-123">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="e76e4-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e76e4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e76e4-124">RELATED LINKS</span></span>

[<span data-ttu-id="e76e4-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e76e4-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e76e4-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e76e4-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e76e4-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


