---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 4bed76f6fa80e5f901d5deeba45940d16332fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854341"
---
# <span data-ttu-id="fe389-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe389-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fe389-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe389-102">SYNOPSIS</span></span>
<span data-ttu-id="fe389-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe389-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="fe389-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe389-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe389-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe389-105">DESCRIPTION</span></span>
<span data-ttu-id="fe389-106">Il cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="fe389-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="fe389-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe389-107">EXAMPLES</span></span>

### <span data-ttu-id="fe389-108">Esempio 1: rimuovere un certificato di autenticazione da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="fe389-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="fe389-109">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e archivia il risultato nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="fe389-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="fe389-110">Il secondo comando rimuove il certificato di autenticazione denominato cert01 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe389-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="fe389-111">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe389-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="fe389-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe389-112">PARAMETERS</span></span>

### <span data-ttu-id="fe389-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe389-113">-ApplicationGateway</span></span>
<span data-ttu-id="fe389-114">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fe389-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="fe389-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe389-115">-DefaultProfile</span></span>
<span data-ttu-id="fe389-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe389-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe389-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe389-117">-Name</span></span>
<span data-ttu-id="fe389-118">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe389-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe389-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe389-119">-Confirm</span></span>
<span data-ttu-id="fe389-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe389-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe389-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe389-121">-WhatIf</span></span>
<span data-ttu-id="fe389-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe389-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe389-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe389-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe389-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe389-124">CommonParameters</span></span>
<span data-ttu-id="fe389-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe389-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe389-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe389-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe389-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe389-127">INPUTS</span></span>

### <span data-ttu-id="fe389-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe389-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe389-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe389-129">OUTPUTS</span></span>

### <span data-ttu-id="fe389-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe389-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe389-131">Note</span><span class="sxs-lookup"><span data-stu-id="fe389-131">NOTES</span></span>
* <span data-ttu-id="fe389-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="fe389-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe389-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe389-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe389-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe389-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe389-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe389-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe389-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe389-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe389-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe389-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


