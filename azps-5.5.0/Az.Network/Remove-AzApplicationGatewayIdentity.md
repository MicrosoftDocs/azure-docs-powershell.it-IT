---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184327"
---
# <span data-ttu-id="57d3d-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="57d3d-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="57d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="57d3d-103">Rimuove un'identità da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="57d3d-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="57d3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57d3d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57d3d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="57d3d-106">Il cmdlet **Remove-AzApplicationGatewayIdentity** rimuove l'identità da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="57d3d-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="57d3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="57d3d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57d3d-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="57d3d-109">In questo esempio l'identità viene rimosso da un gateway applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="57d3d-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="57d3d-110">Nota: se il gateway fa riferimento a un segreto chiave, è anche importante rimuovere i riferimenti al certificato SSL durante questa operazione.</span><span class="sxs-lookup"><span data-stu-id="57d3d-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="57d3d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57d3d-111">PARAMETERS</span></span>

### <span data-ttu-id="57d3d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57d3d-112">-ApplicationGateway</span></span>
<span data-ttu-id="57d3d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57d3d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="57d3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d3d-114">-DefaultProfile</span></span>
<span data-ttu-id="57d3d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57d3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d3d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57d3d-116">-Confirm</span></span>
<span data-ttu-id="57d3d-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57d3d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d3d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d3d-118">-WhatIf</span></span>
<span data-ttu-id="57d3d-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57d3d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d3d-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57d3d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d3d-121">CommonParameters</span></span>
<span data-ttu-id="57d3d-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d3d-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d3d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d3d-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="57d3d-124">INPUTS</span></span>

### <span data-ttu-id="57d3d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57d3d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57d3d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57d3d-126">OUTPUTS</span></span>

### <span data-ttu-id="57d3d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57d3d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57d3d-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="57d3d-128">NOTES</span></span>

## <span data-ttu-id="57d3d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57d3d-129">RELATED LINKS</span></span>
