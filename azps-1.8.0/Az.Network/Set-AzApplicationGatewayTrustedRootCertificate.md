---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e94ca1bbed8e37643b301e5a5cb2ca3acc78d264
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677990"
---
# <span data-ttu-id="18ce0-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ce0-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="18ce0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="18ce0-103">Aggiorna un certificato radice attendibile di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18ce0-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="18ce0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18ce0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ce0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="18ce0-106">Il cmdlet **set-AzApplicationGatewayTrustedRootCertificate** modifica il certificato radice attendibile esistente di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18ce0-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="18ce0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="18ce0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18ce0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="18ce0-109">In scenari precedenti viene illustrato come aggiornare un certificato radice attendibile esistente quando viene eseguito il rollforward di un certificato radice.</span><span class="sxs-lookup"><span data-stu-id="18ce0-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="18ce0-110">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="18ce0-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="18ce0-111">Il secondo comando modifica il certificato radice attendibile esistente con un nuovo certificato radice.</span><span class="sxs-lookup"><span data-stu-id="18ce0-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="18ce0-112">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="18ce0-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="18ce0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18ce0-113">PARAMETERS</span></span>

### <span data-ttu-id="18ce0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18ce0-114">-ApplicationGateway</span></span>
<span data-ttu-id="18ce0-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18ce0-115">The applicationGateway</span></span>

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

### <span data-ttu-id="18ce0-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="18ce0-116">-CertificateFile</span></span>
<span data-ttu-id="18ce0-117">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="18ce0-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="18ce0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ce0-118">-DefaultProfile</span></span>
<span data-ttu-id="18ce0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18ce0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ce0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="18ce0-120">-Name</span></span>
<span data-ttu-id="18ce0-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="18ce0-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="18ce0-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18ce0-122">-Confirm</span></span>
<span data-ttu-id="18ce0-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ce0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ce0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ce0-124">-WhatIf</span></span>
<span data-ttu-id="18ce0-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18ce0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ce0-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18ce0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ce0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ce0-127">CommonParameters</span></span>
<span data-ttu-id="18ce0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ce0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ce0-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ce0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ce0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18ce0-130">INPUTS</span></span>

### <span data-ttu-id="18ce0-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18ce0-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18ce0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18ce0-132">OUTPUTS</span></span>

### <span data-ttu-id="18ce0-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18ce0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18ce0-134">Note</span><span class="sxs-lookup"><span data-stu-id="18ce0-134">NOTES</span></span>

## <span data-ttu-id="18ce0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18ce0-135">RELATED LINKS</span></span>

[<span data-ttu-id="18ce0-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ce0-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="18ce0-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ce0-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="18ce0-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ce0-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="18ce0-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="18ce0-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
