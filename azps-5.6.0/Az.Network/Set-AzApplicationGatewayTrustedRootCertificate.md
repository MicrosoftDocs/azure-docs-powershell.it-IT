---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 839f2a647c4a06ddd1bdebe9b95fac0fdbdd91dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995313"
---
# <span data-ttu-id="0d03c-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d03c-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0d03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d03c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d03c-103">Aggiorna un certificato radice attendibile di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0d03c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="0d03c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d03c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d03c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0d03c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d03c-106">Il cmdlet **Set-AzApplicationGatewayTrustedRootCertificate modifica** il certificato radice attendibile esistente di un Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d03c-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="0d03c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d03c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d03c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d03c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0d03c-109">Negli scenari di esempio precedenti viene illustrato come aggiornare un certificato radice attendibile esistente durante l'implementazione di un certificato radice.</span><span class="sxs-lookup"><span data-stu-id="0d03c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="0d03c-110">Il primo comando ottiene un gateway applicazione e lo archivia nella variabile $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="0d03c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="0d03c-111">Il secondo comando modifica il certificato radice attendibile esistente con un nuovo certificato radice.</span><span class="sxs-lookup"><span data-stu-id="0d03c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="0d03c-112">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="0d03c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0d03c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d03c-113">PARAMETERS</span></span>

### <span data-ttu-id="0d03c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d03c-114">-ApplicationGateway</span></span>
<span data-ttu-id="0d03c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d03c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="0d03c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0d03c-116">-CertificateFile</span></span>
<span data-ttu-id="0d03c-117">Percorso del file CER del certificato</span><span class="sxs-lookup"><span data-stu-id="0d03c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="0d03c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d03c-118">-DefaultProfile</span></span>
<span data-ttu-id="0d03c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d03c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d03c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d03c-120">-Name</span></span>
<span data-ttu-id="0d03c-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="0d03c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="0d03c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d03c-122">-Confirm</span></span>
<span data-ttu-id="0d03c-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d03c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d03c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d03c-124">-WhatIf</span></span>
<span data-ttu-id="0d03c-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d03c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d03c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d03c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d03c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d03c-127">CommonParameters</span></span>
<span data-ttu-id="0d03c-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d03c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d03c-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d03c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d03c-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0d03c-130">INPUTS</span></span>

### <span data-ttu-id="0d03c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d03c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d03c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d03c-132">OUTPUTS</span></span>

### <span data-ttu-id="0d03c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d03c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0d03c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="0d03c-134">NOTES</span></span>

## <span data-ttu-id="0d03c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d03c-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d03c-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d03c-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0d03c-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d03c-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0d03c-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d03c-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="0d03c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0d03c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
