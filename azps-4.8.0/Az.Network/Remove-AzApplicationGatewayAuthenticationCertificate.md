---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188455"
---
# <span data-ttu-id="62e60-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62e60-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="62e60-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62e60-102">SYNOPSIS</span></span>
<span data-ttu-id="62e60-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62e60-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="62e60-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62e60-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e60-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62e60-105">DESCRIPTION</span></span>
<span data-ttu-id="62e60-106">Il cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="62e60-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="62e60-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62e60-107">EXAMPLES</span></span>

### <span data-ttu-id="62e60-108">Esempio 1: rimuovere un certificato di autenticazione da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="62e60-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="62e60-109">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e archivia il risultato nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="62e60-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="62e60-110">Il secondo comando rimuove il certificato di autenticazione denominato cert01 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62e60-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="62e60-111">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62e60-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="62e60-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62e60-112">PARAMETERS</span></span>

### <span data-ttu-id="62e60-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e60-113">-ApplicationGateway</span></span>
<span data-ttu-id="62e60-114">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="62e60-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="62e60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e60-115">-DefaultProfile</span></span>
<span data-ttu-id="62e60-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62e60-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e60-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="62e60-117">-Name</span></span>
<span data-ttu-id="62e60-118">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e60-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62e60-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62e60-119">-Confirm</span></span>
<span data-ttu-id="62e60-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e60-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e60-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e60-121">-WhatIf</span></span>
<span data-ttu-id="62e60-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62e60-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e60-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62e60-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e60-124">CommonParameters</span></span>
<span data-ttu-id="62e60-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e60-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e60-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e60-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62e60-127">INPUTS</span></span>

### <span data-ttu-id="62e60-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e60-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62e60-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62e60-129">OUTPUTS</span></span>

### <span data-ttu-id="62e60-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62e60-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62e60-131">Note</span><span class="sxs-lookup"><span data-stu-id="62e60-131">NOTES</span></span>
* <span data-ttu-id="62e60-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="62e60-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="62e60-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62e60-133">RELATED LINKS</span></span>

[<span data-ttu-id="62e60-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62e60-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62e60-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62e60-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62e60-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62e60-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="62e60-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="62e60-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


