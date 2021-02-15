---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186983"
---
# <span data-ttu-id="4b272-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b272-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="4b272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b272-102">SYNOPSIS</span></span>
<span data-ttu-id="4b272-103">Rimuove l'oggetto catena di certificati DELLA CA del client attendibile da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4b272-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="4b272-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b272-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b272-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b272-105">DESCRIPTION</span></span>
<span data-ttu-id="4b272-106">Il cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** rimuove l'oggetto catena di certificati CA del client attendibile da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b272-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="4b272-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b272-107">EXAMPLES</span></span>

### <span data-ttu-id="4b272-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b272-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="4b272-109">Il primo comando ottiene un gateway applicazione e lo archivia nella variabile $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="4b272-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="4b272-110">Il secondo comando rimuove la catena di certificati CA del client attendibile denominata "TrustedClientCertificate01" dal gateway applicazione archiviato in $gw.</span><span class="sxs-lookup"><span data-stu-id="4b272-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="4b272-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b272-111">PARAMETERS</span></span>

### <span data-ttu-id="4b272-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b272-112">-ApplicationGateway</span></span>
<span data-ttu-id="4b272-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b272-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4b272-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b272-114">-DefaultProfile</span></span>
<span data-ttu-id="4b272-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b272-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b272-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4b272-116">-Name</span></span>
<span data-ttu-id="4b272-117">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="4b272-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="4b272-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b272-118">-Confirm</span></span>
<span data-ttu-id="4b272-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b272-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b272-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b272-120">-WhatIf</span></span>
<span data-ttu-id="4b272-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b272-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b272-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b272-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b272-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b272-123">CommonParameters</span></span>
<span data-ttu-id="4b272-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b272-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b272-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b272-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b272-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b272-126">INPUTS</span></span>

### <span data-ttu-id="4b272-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b272-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b272-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b272-128">OUTPUTS</span></span>

### <span data-ttu-id="4b272-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b272-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b272-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b272-130">NOTES</span></span>

## <span data-ttu-id="4b272-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b272-131">RELATED LINKS</span></span>

[<span data-ttu-id="4b272-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b272-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4b272-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b272-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4b272-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b272-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="4b272-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4b272-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)