---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 013010e0b679c69a6fa5c6d8341879b95bd55692
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521019"
---
# <span data-ttu-id="d5fd2-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5fd2-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d5fd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fd2-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5fd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5fd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fd2-106">Il cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="d5fd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-107">EXAMPLES</span></span>

## <span data-ttu-id="d5fd2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-108">PARAMETERS</span></span>

### <span data-ttu-id="d5fd2-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5fd2-109">-ApplicationGateway</span></span>
<span data-ttu-id="d5fd2-110">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="d5fd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fd2-111">-DefaultProfile</span></span>
<span data-ttu-id="d5fd2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fd2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5fd2-113">-Name</span></span>
<span data-ttu-id="d5fd2-114">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5fd2-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5fd2-115">-Confirm</span></span>
<span data-ttu-id="d5fd2-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fd2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fd2-117">-WhatIf</span></span>
<span data-ttu-id="d5fd2-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5fd2-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fd2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fd2-120">CommonParameters</span></span>
<span data-ttu-id="d5fd2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fd2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fd2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fd2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fd2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-123">INPUTS</span></span>

### <span data-ttu-id="d5fd2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d5fd2-124">System.String</span></span>

## <span data-ttu-id="d5fd2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5fd2-125">OUTPUTS</span></span>

### <span data-ttu-id="d5fd2-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5fd2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5fd2-127">Note</span><span class="sxs-lookup"><span data-stu-id="d5fd2-127">NOTES</span></span>
* <span data-ttu-id="d5fd2-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="d5fd2-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d5fd2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5fd2-129">RELATED LINKS</span></span>

[<span data-ttu-id="d5fd2-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5fd2-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5fd2-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5fd2-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5fd2-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5fd2-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d5fd2-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d5fd2-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


