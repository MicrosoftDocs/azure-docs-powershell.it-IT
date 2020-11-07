---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866269"
---
# <span data-ttu-id="b1d89-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b1d89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1d89-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d89-103">Crea un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1d89-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1d89-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1d89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d89-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d89-106">Il cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** crea un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d89-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b1d89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1d89-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d89-108">1:</span><span class="sxs-lookup"><span data-stu-id="b1d89-108">1:</span></span>
```

```

## <span data-ttu-id="b1d89-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1d89-109">PARAMETERS</span></span>

### <span data-ttu-id="b1d89-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b1d89-110">-CertificateFile</span></span>
<span data-ttu-id="b1d89-111">Specifica il percorso del certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b1d89-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="b1d89-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d89-112">-DefaultProfile</span></span>
<span data-ttu-id="b1d89-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d89-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d89-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1d89-114">-Name</span></span>
<span data-ttu-id="b1d89-115">Specifica un nome per il certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b1d89-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="b1d89-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1d89-116">-Confirm</span></span>
<span data-ttu-id="b1d89-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1d89-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1d89-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1d89-118">-WhatIf</span></span>
<span data-ttu-id="b1d89-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1d89-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1d89-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1d89-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1d89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d89-121">CommonParameters</span></span>
<span data-ttu-id="b1d89-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d89-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d89-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d89-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1d89-124">INPUTS</span></span>

### <span data-ttu-id="b1d89-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b1d89-125">System.String</span></span>

## <span data-ttu-id="b1d89-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1d89-126">OUTPUTS</span></span>

### <span data-ttu-id="b1d89-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b1d89-128">Note</span><span class="sxs-lookup"><span data-stu-id="b1d89-128">NOTES</span></span>
* <span data-ttu-id="b1d89-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="b1d89-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b1d89-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1d89-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1d89-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1d89-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1d89-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1d89-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1d89-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


