---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032303"
---
# <span data-ttu-id="e6cc7-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cc7-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="e6cc7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cc7-103">Aggiorna un certificato radice attendibile di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="e6cc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6cc7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6cc7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cc7-106">Il cmdlet **set-AzApplicationGatewayTrustedRootCertificate** modifica il certificato radice attendibile esistente di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="e6cc7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cc7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6cc7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="e6cc7-109">In scenari precedenti viene illustrato come aggiornare un certificato radice attendibile esistente quando viene eseguito il rollforward di un certificato radice.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="e6cc7-110">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="e6cc7-111">Il secondo comando modifica il certificato radice attendibile esistente con un nuovo certificato radice.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="e6cc7-112">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="e6cc7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6cc7-113">PARAMETERS</span></span>

### <span data-ttu-id="e6cc7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cc7-114">-ApplicationGateway</span></span>
<span data-ttu-id="e6cc7-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cc7-115">The applicationGateway</span></span>

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

### <span data-ttu-id="e6cc7-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e6cc7-116">-CertificateFile</span></span>
<span data-ttu-id="e6cc7-117">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="e6cc7-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="e6cc7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cc7-118">-DefaultProfile</span></span>
<span data-ttu-id="e6cc7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cc7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6cc7-120">-Name</span></span>
<span data-ttu-id="e6cc7-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="e6cc7-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="e6cc7-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6cc7-122">-Confirm</span></span>
<span data-ttu-id="e6cc7-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cc7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cc7-124">-WhatIf</span></span>
<span data-ttu-id="e6cc7-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cc7-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cc7-127">CommonParameters</span></span>
<span data-ttu-id="e6cc7-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cc7-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cc7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cc7-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6cc7-130">INPUTS</span></span>

### <span data-ttu-id="e6cc7-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cc7-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6cc7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6cc7-132">OUTPUTS</span></span>

### <span data-ttu-id="e6cc7-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cc7-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6cc7-134">Note</span><span class="sxs-lookup"><span data-stu-id="e6cc7-134">NOTES</span></span>

## <span data-ttu-id="e6cc7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6cc7-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6cc7-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cc7-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e6cc7-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cc7-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e6cc7-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cc7-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="e6cc7-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cc7-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
