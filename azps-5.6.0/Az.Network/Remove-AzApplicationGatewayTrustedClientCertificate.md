---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: c7fdf250ad7c322e47c26e023f04689a12a8eee5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976670"
---
# <span data-ttu-id="35b31-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="35b31-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="35b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35b31-102">SYNOPSIS</span></span>
<span data-ttu-id="35b31-103">Rimuove l'oggetto della catena di certificati della CA del client attendibile da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="35b31-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="35b31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35b31-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35b31-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35b31-105">DESCRIPTION</span></span>
<span data-ttu-id="35b31-106">Il cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** rimuove l'oggetto catena di certificati CA del client attendibile da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="35b31-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="35b31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35b31-107">EXAMPLES</span></span>

### <span data-ttu-id="35b31-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35b31-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="35b31-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="35b31-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="35b31-110">Il secondo comando rimuove la catena di certificati CA del client attendibile denominata "TrustedClientCertificate01" dal gateway applicazione archiviato in $gw.</span><span class="sxs-lookup"><span data-stu-id="35b31-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="35b31-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35b31-111">PARAMETERS</span></span>

### <span data-ttu-id="35b31-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b31-112">-ApplicationGateway</span></span>
<span data-ttu-id="35b31-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b31-113">The applicationGateway</span></span>

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

### <span data-ttu-id="35b31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b31-114">-DefaultProfile</span></span>
<span data-ttu-id="35b31-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35b31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35b31-116">-Name</span><span class="sxs-lookup"><span data-stu-id="35b31-116">-Name</span></span>
<span data-ttu-id="35b31-117">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="35b31-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="35b31-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35b31-118">-Confirm</span></span>
<span data-ttu-id="35b31-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35b31-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b31-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b31-120">-WhatIf</span></span>
<span data-ttu-id="35b31-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b31-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b31-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b31-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b31-123">CommonParameters</span></span>
<span data-ttu-id="35b31-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b31-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35b31-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b31-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="35b31-126">INPUTS</span></span>

### <span data-ttu-id="35b31-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b31-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35b31-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35b31-128">OUTPUTS</span></span>

### <span data-ttu-id="35b31-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b31-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35b31-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="35b31-130">NOTES</span></span>

## <span data-ttu-id="35b31-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35b31-131">RELATED LINKS</span></span>

[<span data-ttu-id="35b31-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="35b31-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="35b31-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="35b31-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="35b31-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="35b31-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="35b31-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="35b31-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)