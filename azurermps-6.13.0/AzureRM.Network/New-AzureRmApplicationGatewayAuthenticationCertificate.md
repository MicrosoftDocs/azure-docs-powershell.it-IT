---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bdc2821c8499c5a95acd180c9bbfa28568cc5034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513700"
---
# <span data-ttu-id="7ece1-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7ece1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ece1-102">SYNOPSIS</span></span>
<span data-ttu-id="7ece1-103">Crea un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ece1-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ece1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ece1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ece1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ece1-105">DESCRIPTION</span></span>
<span data-ttu-id="7ece1-106">Il cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** crea un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7ece1-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7ece1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ece1-107">EXAMPLES</span></span>

## <span data-ttu-id="7ece1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ece1-108">PARAMETERS</span></span>

### <span data-ttu-id="7ece1-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7ece1-109">-CertificateFile</span></span>
<span data-ttu-id="7ece1-110">Specifica il percorso del certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="7ece1-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="7ece1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ece1-111">-DefaultProfile</span></span>
<span data-ttu-id="7ece1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ece1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ece1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ece1-113">-Name</span></span>
<span data-ttu-id="7ece1-114">Specifica un nome per il certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="7ece1-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="7ece1-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ece1-115">-Confirm</span></span>
<span data-ttu-id="7ece1-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ece1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ece1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ece1-117">-WhatIf</span></span>
<span data-ttu-id="7ece1-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ece1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ece1-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ece1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ece1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ece1-120">CommonParameters</span></span>
<span data-ttu-id="7ece1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ece1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ece1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ece1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ece1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ece1-123">INPUTS</span></span>

### <span data-ttu-id="7ece1-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7ece1-124">None</span></span>

## <span data-ttu-id="7ece1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ece1-125">OUTPUTS</span></span>

### <span data-ttu-id="7ece1-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7ece1-127">Note</span><span class="sxs-lookup"><span data-stu-id="7ece1-127">NOTES</span></span>
* <span data-ttu-id="7ece1-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="7ece1-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7ece1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ece1-129">RELATED LINKS</span></span>

[<span data-ttu-id="7ece1-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7ece1-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7ece1-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7ece1-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7ece1-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


