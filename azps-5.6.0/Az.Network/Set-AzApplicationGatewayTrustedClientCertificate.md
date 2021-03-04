---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952142"
---
# <span data-ttu-id="97231-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97231-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="97231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97231-102">SYNOPSIS</span></span>
<span data-ttu-id="97231-103">Modifica la catena di certificati CA del client attendibile di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="97231-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="97231-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97231-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97231-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97231-105">DESCRIPTION</span></span>
<span data-ttu-id="97231-106">Il cmdlet **Set-AzApplicationGatewayTrustedClientCertificate** modifica la catena di certificati CA del client attendibile di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="97231-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="97231-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97231-107">EXAMPLES</span></span>

### <span data-ttu-id="97231-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97231-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="97231-109">Negli scenari di esempio precedenti viene illustrato come aggiornare un oggetto della catena di certificati CA del client attendibile esistente.</span><span class="sxs-lookup"><span data-stu-id="97231-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="97231-110">Il primo comando ottiene un gateway applicazione e lo archivia nella $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="97231-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="97231-111">Il secondo comando modifica l'oggetto della catena di certificati CA del client attendibile esistente con un nuovo file della catena di certificati CA.</span><span class="sxs-lookup"><span data-stu-id="97231-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="97231-112">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="97231-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="97231-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97231-113">PARAMETERS</span></span>

### <span data-ttu-id="97231-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97231-114">-ApplicationGateway</span></span>
<span data-ttu-id="97231-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97231-115">The applicationGateway</span></span>

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

### <span data-ttu-id="97231-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="97231-116">-CertificateFile</span></span>
<span data-ttu-id="97231-117">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="97231-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="97231-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97231-118">-DefaultProfile</span></span>
<span data-ttu-id="97231-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97231-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97231-120">-Name</span><span class="sxs-lookup"><span data-stu-id="97231-120">-Name</span></span>
<span data-ttu-id="97231-121">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="97231-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="97231-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97231-122">-Confirm</span></span>
<span data-ttu-id="97231-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97231-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97231-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97231-124">-WhatIf</span></span>
<span data-ttu-id="97231-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97231-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97231-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97231-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97231-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97231-127">CommonParameters</span></span>
<span data-ttu-id="97231-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97231-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97231-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97231-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97231-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="97231-130">INPUTS</span></span>

### <span data-ttu-id="97231-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97231-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97231-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97231-132">OUTPUTS</span></span>

### <span data-ttu-id="97231-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97231-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97231-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="97231-134">NOTES</span></span>

## <span data-ttu-id="97231-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97231-135">RELATED LINKS</span></span>

[<span data-ttu-id="97231-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97231-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="97231-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97231-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="97231-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97231-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="97231-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="97231-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)