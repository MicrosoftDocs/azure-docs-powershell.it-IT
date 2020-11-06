---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 9ec4522da3c5a75a1c9e5bad977f294e0987f4fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511680"
---
# <span data-ttu-id="dfd50-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd50-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="dfd50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfd50-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd50-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfd50-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfd50-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd50-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfd50-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd50-106">Il cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd50-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="dfd50-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfd50-107">EXAMPLES</span></span>

## <span data-ttu-id="dfd50-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfd50-108">PARAMETERS</span></span>

### <span data-ttu-id="dfd50-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfd50-109">-ApplicationGateway</span></span>
<span data-ttu-id="dfd50-110">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="dfd50-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="dfd50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd50-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd50-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd50-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfd50-113">-Name</span></span>
<span data-ttu-id="dfd50-114">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd50-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd50-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfd50-115">-Confirm</span></span>
<span data-ttu-id="dfd50-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd50-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd50-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd50-117">-WhatIf</span></span>
<span data-ttu-id="dfd50-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfd50-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd50-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfd50-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd50-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd50-120">CommonParameters</span></span>
<span data-ttu-id="dfd50-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd50-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd50-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd50-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd50-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfd50-123">INPUTS</span></span>

### <span data-ttu-id="dfd50-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfd50-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="dfd50-125">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dfd50-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="dfd50-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfd50-126">OUTPUTS</span></span>

### <span data-ttu-id="dfd50-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfd50-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfd50-128">Note</span><span class="sxs-lookup"><span data-stu-id="dfd50-128">NOTES</span></span>
* <span data-ttu-id="dfd50-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="dfd50-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dfd50-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfd50-130">RELATED LINKS</span></span>

[<span data-ttu-id="dfd50-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd50-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dfd50-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd50-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dfd50-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd50-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="dfd50-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd50-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


