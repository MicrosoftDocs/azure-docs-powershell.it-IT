---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866068"
---
# <span data-ttu-id="91a13-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="91a13-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="91a13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91a13-102">SYNOPSIS</span></span>
<span data-ttu-id="91a13-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91a13-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91a13-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91a13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a13-105">DESCRIPTION</span></span>
<span data-ttu-id="91a13-106">Il cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="91a13-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="91a13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91a13-107">EXAMPLES</span></span>

### <span data-ttu-id="91a13-108">1:</span><span class="sxs-lookup"><span data-stu-id="91a13-108">1:</span></span>
```

```

## <span data-ttu-id="91a13-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91a13-109">PARAMETERS</span></span>

### <span data-ttu-id="91a13-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91a13-110">-ApplicationGateway</span></span>
<span data-ttu-id="91a13-111">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="91a13-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="91a13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a13-112">-DefaultProfile</span></span>
<span data-ttu-id="91a13-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91a13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91a13-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="91a13-114">-Name</span></span>
<span data-ttu-id="91a13-115">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a13-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91a13-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91a13-116">-Confirm</span></span>
<span data-ttu-id="91a13-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a13-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a13-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a13-118">-WhatIf</span></span>
<span data-ttu-id="91a13-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91a13-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91a13-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91a13-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a13-121">CommonParameters</span></span>
<span data-ttu-id="91a13-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a13-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a13-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91a13-124">INPUTS</span></span>

### <span data-ttu-id="91a13-125">System. String</span><span class="sxs-lookup"><span data-stu-id="91a13-125">System.String</span></span>

## <span data-ttu-id="91a13-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91a13-126">OUTPUTS</span></span>

### <span data-ttu-id="91a13-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91a13-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91a13-128">Note</span><span class="sxs-lookup"><span data-stu-id="91a13-128">NOTES</span></span>
* <span data-ttu-id="91a13-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="91a13-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="91a13-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91a13-130">RELATED LINKS</span></span>

[<span data-ttu-id="91a13-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="91a13-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="91a13-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="91a13-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="91a13-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="91a13-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="91a13-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="91a13-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


