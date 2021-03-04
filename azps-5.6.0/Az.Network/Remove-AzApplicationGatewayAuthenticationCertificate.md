---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: aa8bd1b8850c1aa7f859d1797a961e32c22aa9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953773"
---
# <span data-ttu-id="756f7-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="756f7-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="756f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756f7-102">SYNOPSIS</span></span>
<span data-ttu-id="756f7-103">Rimuove un certificato di autenticazione da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="756f7-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="756f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="756f7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="756f7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="756f7-105">DESCRIPTION</span></span>
<span data-ttu-id="756f7-106">Il cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate rimuove** un certificato di autenticazione da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="756f7-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="756f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="756f7-107">EXAMPLES</span></span>

### <span data-ttu-id="756f7-108">Esempio 1: Rimuovere un certificato di autenticazione da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="756f7-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="756f7-109">Il primo comando recupera il gateway applicazione denominato appGwName e archivia il risultato nella $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="756f7-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="756f7-110">Il secondo comando rimuove il certificato di autenticazione denominato cert01 dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="756f7-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="756f7-111">Il terzo comando aggiorna il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="756f7-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="756f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="756f7-112">PARAMETERS</span></span>

### <span data-ttu-id="756f7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="756f7-113">-ApplicationGateway</span></span>
<span data-ttu-id="756f7-114">Specifica il nome del gateway applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="756f7-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="756f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756f7-115">-DefaultProfile</span></span>
<span data-ttu-id="756f7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="756f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="756f7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="756f7-117">-Name</span></span>
<span data-ttu-id="756f7-118">Specifica il nome del certificato di autenticazione rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="756f7-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="756f7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="756f7-119">-Confirm</span></span>
<span data-ttu-id="756f7-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="756f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="756f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756f7-121">-WhatIf</span></span>
<span data-ttu-id="756f7-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="756f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="756f7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="756f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="756f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756f7-124">CommonParameters</span></span>
<span data-ttu-id="756f7-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756f7-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756f7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756f7-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="756f7-127">INPUTS</span></span>

### <span data-ttu-id="756f7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="756f7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="756f7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="756f7-129">OUTPUTS</span></span>

### <span data-ttu-id="756f7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="756f7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="756f7-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="756f7-131">NOTES</span></span>
* <span data-ttu-id="756f7-132">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="756f7-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="756f7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="756f7-133">RELATED LINKS</span></span>

[<span data-ttu-id="756f7-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="756f7-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="756f7-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="756f7-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="756f7-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="756f7-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="756f7-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="756f7-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


