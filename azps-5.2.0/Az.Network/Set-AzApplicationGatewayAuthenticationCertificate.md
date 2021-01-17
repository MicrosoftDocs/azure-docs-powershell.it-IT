---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329707"
---
# <span data-ttu-id="b2868-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b2868-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b2868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2868-102">SYNOPSIS</span></span>
<span data-ttu-id="b2868-103">Aggiorna un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2868-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b2868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2868-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2868-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2868-105">DESCRIPTION</span></span>
<span data-ttu-id="b2868-106">Il cmdlet **set-AzApplicationGatewayAuthenticationCertificate** aggiorna un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b2868-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b2868-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2868-107">EXAMPLES</span></span>

### <span data-ttu-id="b2868-108">Esempio 1: aggiornare un certificato di autenticazione</span><span class="sxs-lookup"><span data-stu-id="b2868-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b2868-109">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e archivia il risultato nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="b2868-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="b2868-110">Il secondo comando Aggiorna il certificato di autenticazione denominato cert01 nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2868-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="b2868-111">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2868-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="b2868-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2868-112">PARAMETERS</span></span>

### <span data-ttu-id="b2868-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2868-113">-ApplicationGateway</span></span>
<span data-ttu-id="b2868-114">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiorna un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b2868-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b2868-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b2868-115">-CertificateFile</span></span>
<span data-ttu-id="b2868-116">Specifica il percorso del file del certificato di autenticazione con cui questo cmdlet aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="b2868-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b2868-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2868-117">-DefaultProfile</span></span>
<span data-ttu-id="b2868-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2868-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2868-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2868-119">-Name</span></span>
<span data-ttu-id="b2868-120">Specifica il nome del certificato di autenticazione che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="b2868-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b2868-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2868-121">-Confirm</span></span>
<span data-ttu-id="b2868-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2868-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2868-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2868-123">-WhatIf</span></span>
<span data-ttu-id="b2868-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2868-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2868-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2868-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2868-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2868-126">CommonParameters</span></span>
<span data-ttu-id="b2868-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2868-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2868-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2868-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2868-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2868-129">INPUTS</span></span>

### <span data-ttu-id="b2868-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2868-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2868-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2868-131">OUTPUTS</span></span>

### <span data-ttu-id="b2868-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2868-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2868-133">Note</span><span class="sxs-lookup"><span data-stu-id="b2868-133">NOTES</span></span>
* <span data-ttu-id="b2868-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="b2868-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b2868-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2868-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2868-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b2868-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b2868-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b2868-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b2868-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b2868-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b2868-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b2868-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


