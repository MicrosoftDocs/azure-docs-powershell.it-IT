---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860601"
---
# <span data-ttu-id="60a58-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="60a58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60a58-102">SYNOPSIS</span></span>
<span data-ttu-id="60a58-103">Crea un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60a58-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="60a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a58-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a58-105">DESCRIPTION</span></span>
<span data-ttu-id="60a58-106">Il cmdlet **New-AzApplicationGatewayAuthenticationCertificate** crea un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="60a58-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="60a58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a58-107">EXAMPLES</span></span>

### <span data-ttu-id="60a58-108">1:</span><span class="sxs-lookup"><span data-stu-id="60a58-108">1:</span></span>
```

```

## <span data-ttu-id="60a58-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60a58-109">PARAMETERS</span></span>

### <span data-ttu-id="60a58-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="60a58-110">-CertificateFile</span></span>
<span data-ttu-id="60a58-111">Specifica il percorso del certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="60a58-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="60a58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a58-112">-DefaultProfile</span></span>
<span data-ttu-id="60a58-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60a58-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a58-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="60a58-114">-Name</span></span>
<span data-ttu-id="60a58-115">Specifica un nome per il certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="60a58-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="60a58-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60a58-116">-Confirm</span></span>
<span data-ttu-id="60a58-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a58-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a58-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a58-118">-WhatIf</span></span>
<span data-ttu-id="60a58-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a58-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a58-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a58-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a58-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a58-121">CommonParameters</span></span>
<span data-ttu-id="60a58-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a58-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a58-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a58-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a58-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60a58-124">INPUTS</span></span>

### <span data-ttu-id="60a58-125">System. String</span><span class="sxs-lookup"><span data-stu-id="60a58-125">System.String</span></span>

## <span data-ttu-id="60a58-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a58-126">OUTPUTS</span></span>

### <span data-ttu-id="60a58-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="60a58-128">Note</span><span class="sxs-lookup"><span data-stu-id="60a58-128">NOTES</span></span>
* <span data-ttu-id="60a58-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="60a58-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="60a58-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a58-130">RELATED LINKS</span></span>

[<span data-ttu-id="60a58-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="60a58-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="60a58-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="60a58-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="60a58-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


