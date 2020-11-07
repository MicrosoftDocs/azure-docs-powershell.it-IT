---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688608"
---
# <span data-ttu-id="bc074-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc074-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bc074-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc074-102">SYNOPSIS</span></span>
<span data-ttu-id="bc074-103">Aggiorna un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc074-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc074-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc074-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc074-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc074-105">DESCRIPTION</span></span>
<span data-ttu-id="bc074-106">Il cmdlet **set-AzureRmApplicationGatewayAuthenticationCertificate** aggiorna un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="bc074-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="bc074-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc074-107">EXAMPLES</span></span>

## <span data-ttu-id="bc074-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc074-108">PARAMETERS</span></span>

### <span data-ttu-id="bc074-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc074-109">-ApplicationGateway</span></span>
<span data-ttu-id="bc074-110">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiorna un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="bc074-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="bc074-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bc074-111">-CertificateFile</span></span>
<span data-ttu-id="bc074-112">Specifica il percorso del file del certificato di autenticazione con cui questo cmdlet aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="bc074-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="bc074-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc074-113">-Name</span></span>
<span data-ttu-id="bc074-114">Specifica il nome del certificato di autenticazione che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="bc074-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="bc074-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc074-115">-Confirm</span></span>
<span data-ttu-id="bc074-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc074-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc074-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc074-117">-WhatIf</span></span>
<span data-ttu-id="bc074-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc074-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc074-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc074-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc074-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc074-120">-DefaultProfile</span></span>
<span data-ttu-id="bc074-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc074-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc074-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc074-122">CommonParameters</span></span>
<span data-ttu-id="bc074-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc074-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc074-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc074-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc074-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc074-125">INPUTS</span></span>

### <span data-ttu-id="bc074-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bc074-126">System.String</span></span>

## <span data-ttu-id="bc074-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc074-127">OUTPUTS</span></span>

### <span data-ttu-id="bc074-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc074-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc074-129">Note</span><span class="sxs-lookup"><span data-stu-id="bc074-129">NOTES</span></span>
* <span data-ttu-id="bc074-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="bc074-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bc074-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc074-131">RELATED LINKS</span></span>

[<span data-ttu-id="bc074-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc074-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc074-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc074-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc074-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc074-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bc074-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bc074-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


