---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a060ddde57fc3d0cfadde487a147b8743acd5fbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003502"
---
# <span data-ttu-id="8f6eb-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6eb-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8f6eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6eb-103">Aggiorna un certificato di autenticazione per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="8f6eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f6eb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6eb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f6eb-105">DESCRIPTION</span></span>
<span data-ttu-id="8f6eb-106">Il cmdlet **Set-AzApplicationGatewayAuthenticationCertificate** aggiorna un certificato di autenticazione per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8f6eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f6eb-107">EXAMPLES</span></span>

### <span data-ttu-id="8f6eb-108">Esempio 1: Aggiornare un certificato di autenticazione</span><span class="sxs-lookup"><span data-stu-id="8f6eb-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8f6eb-109">Il primo comando recupera il gateway applicazione denominato appGwName e archivia il risultato nella $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="8f6eb-110">Il secondo comando aggiorna il certificato di autenticazione denominato cert01 nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="8f6eb-111">Il terzo comando aggiorna il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="8f6eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f6eb-112">PARAMETERS</span></span>

### <span data-ttu-id="8f6eb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f6eb-113">-ApplicationGateway</span></span>
<span data-ttu-id="8f6eb-114">Specifica il nome del gateway applicazione per il quale questo cmdlet aggiorna un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="8f6eb-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8f6eb-115">-CertificateFile</span></span>
<span data-ttu-id="8f6eb-116">Specifica il percorso del file del certificato di autenticazione con cui questo cmdlet aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="8f6eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6eb-117">-DefaultProfile</span></span>
<span data-ttu-id="8f6eb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f6eb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8f6eb-119">-Name</span></span>
<span data-ttu-id="8f6eb-120">Specifica il nome del certificato di autenticazione aggiornato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8f6eb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f6eb-121">-Confirm</span></span>
<span data-ttu-id="8f6eb-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6eb-123">-WhatIf</span></span>
<span data-ttu-id="8f6eb-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6eb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6eb-126">CommonParameters</span></span>
<span data-ttu-id="8f6eb-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6eb-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6eb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6eb-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f6eb-129">INPUTS</span></span>

### <span data-ttu-id="8f6eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f6eb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f6eb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f6eb-131">OUTPUTS</span></span>

### <span data-ttu-id="8f6eb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f6eb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f6eb-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f6eb-133">NOTES</span></span>
* <span data-ttu-id="8f6eb-134">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="8f6eb-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8f6eb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f6eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="8f6eb-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6eb-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8f6eb-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6eb-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8f6eb-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6eb-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8f6eb-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8f6eb-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


