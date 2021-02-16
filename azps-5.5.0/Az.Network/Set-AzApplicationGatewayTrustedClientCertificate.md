---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186887"
---
# <span data-ttu-id="f32f6-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f32f6-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="f32f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f32f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f32f6-103">Modifica la catena di certificati CA del client attendibile di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f32f6-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="f32f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f32f6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f32f6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f32f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f32f6-106">Il cmdlet **Set-AzApplicationGatewayTrustedClientCertificate** modifica la catena di certificati CA del client attendibile di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f32f6-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="f32f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f32f6-107">EXAMPLES</span></span>

### <span data-ttu-id="f32f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f32f6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f32f6-109">Negli scenari di esempio precedenti viene illustrato come aggiornare un oggetto della catena di certificati CA di un client attendibile esistente.</span><span class="sxs-lookup"><span data-stu-id="f32f6-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="f32f6-110">Il primo comando ottiene un gateway applicazione e lo archivia nella variabile $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="f32f6-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="f32f6-111">Il secondo comando modifica l'oggetto della catena di certificati CA del client attendibile esistente con un nuovo file della catena di certificati CA.</span><span class="sxs-lookup"><span data-stu-id="f32f6-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="f32f6-112">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f6-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f32f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f32f6-113">PARAMETERS</span></span>

### <span data-ttu-id="f32f6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f32f6-114">-ApplicationGateway</span></span>
<span data-ttu-id="f32f6-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f32f6-115">The applicationGateway</span></span>

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

### <span data-ttu-id="f32f6-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f32f6-116">-CertificateFile</span></span>
<span data-ttu-id="f32f6-117">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="f32f6-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="f32f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32f6-118">-DefaultProfile</span></span>
<span data-ttu-id="f32f6-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f32f6-120">-Name</span></span>
<span data-ttu-id="f32f6-121">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="f32f6-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="f32f6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f32f6-122">-Confirm</span></span>
<span data-ttu-id="f32f6-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f32f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f32f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32f6-124">-WhatIf</span></span>
<span data-ttu-id="f32f6-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f32f6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f32f6-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f32f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f32f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32f6-127">CommonParameters</span></span>
<span data-ttu-id="f32f6-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32f6-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f32f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32f6-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="f32f6-130">INPUTS</span></span>

### <span data-ttu-id="f32f6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f32f6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f32f6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f32f6-132">OUTPUTS</span></span>

### <span data-ttu-id="f32f6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f32f6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f32f6-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="f32f6-134">NOTES</span></span>

## <span data-ttu-id="f32f6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f32f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="f32f6-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f32f6-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f32f6-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f32f6-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f32f6-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f32f6-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="f32f6-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f32f6-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)