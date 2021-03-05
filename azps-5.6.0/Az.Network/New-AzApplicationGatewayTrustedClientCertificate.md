---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990035"
---
# <span data-ttu-id="709ce-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="709ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709ce-102">SYNOPSIS</span></span>
<span data-ttu-id="709ce-103">Crea una catena di certificati CA client attendibili per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="709ce-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="709ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="709ce-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="709ce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="709ce-105">DESCRIPTION</span></span>
<span data-ttu-id="709ce-106">Il cmdlet New-AzApplicationGatewayTrustedClientCertificate crea una catena di certificati CA del client attendibile per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="709ce-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="709ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="709ce-107">EXAMPLES</span></span>

### <span data-ttu-id="709ce-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="709ce-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="709ce-109">Il comando crea un nuovo oggetto catena di certificati CA del client attendibile che prende come input il percorso del certificato CA client.</span><span class="sxs-lookup"><span data-stu-id="709ce-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="709ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="709ce-110">PARAMETERS</span></span>

### <span data-ttu-id="709ce-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="709ce-111">-CertificateFile</span></span>
<span data-ttu-id="709ce-112">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="709ce-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="709ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709ce-113">-DefaultProfile</span></span>
<span data-ttu-id="709ce-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="709ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709ce-115">-Name</span><span class="sxs-lookup"><span data-stu-id="709ce-115">-Name</span></span>
<span data-ttu-id="709ce-116">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="709ce-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="709ce-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="709ce-117">-Confirm</span></span>
<span data-ttu-id="709ce-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="709ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709ce-119">-WhatIf</span></span>
<span data-ttu-id="709ce-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="709ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="709ce-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="709ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709ce-122">CommonParameters</span></span>
<span data-ttu-id="709ce-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709ce-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="709ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709ce-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="709ce-125">INPUTS</span></span>

### <span data-ttu-id="709ce-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="709ce-126">None</span></span>

## <span data-ttu-id="709ce-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="709ce-127">OUTPUTS</span></span>

### <span data-ttu-id="709ce-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="709ce-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="709ce-129">NOTES</span></span>

## <span data-ttu-id="709ce-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="709ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="709ce-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="709ce-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="709ce-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="709ce-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ce-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)