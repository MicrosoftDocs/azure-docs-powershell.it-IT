---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201982"
---
# <span data-ttu-id="1fa1a-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="1fa1a-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="1fa1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fa1a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa1a-103">Rimuove un'identità da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="1fa1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fa1a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fa1a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fa1a-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa1a-106">Cmdlet **Remove-AzApplicationGatewayIdentity** consente di rimuovere l'identità da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="1fa1a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fa1a-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa1a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1fa1a-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="1fa1a-109">In questo esempio rimuoviamo l'identità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="1fa1a-110">Nota: se il gateway fa riferimento a un segreto di un Vault, è anche importante rimuovere i riferimenti ai certificati SSL lungo questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="1fa1a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fa1a-111">PARAMETERS</span></span>

### <span data-ttu-id="1fa1a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fa1a-112">-ApplicationGateway</span></span>
<span data-ttu-id="1fa1a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fa1a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1fa1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa1a-114">-DefaultProfile</span></span>
<span data-ttu-id="1fa1a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fa1a-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fa1a-116">-Confirm</span></span>
<span data-ttu-id="1fa1a-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa1a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa1a-118">-WhatIf</span></span>
<span data-ttu-id="1fa1a-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fa1a-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa1a-121">CommonParameters</span></span>
<span data-ttu-id="1fa1a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa1a-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa1a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa1a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fa1a-124">INPUTS</span></span>

### <span data-ttu-id="1fa1a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fa1a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fa1a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fa1a-126">OUTPUTS</span></span>

### <span data-ttu-id="1fa1a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fa1a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fa1a-128">Note</span><span class="sxs-lookup"><span data-stu-id="1fa1a-128">NOTES</span></span>

## <span data-ttu-id="1fa1a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fa1a-129">RELATED LINKS</span></span>
