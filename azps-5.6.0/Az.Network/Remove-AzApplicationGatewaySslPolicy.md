---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: e5ac68f10a75dff94313fa17830720466e82da5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990974"
---
# <span data-ttu-id="488c5-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="488c5-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="488c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="488c5-102">SYNOPSIS</span></span>
<span data-ttu-id="488c5-103">Rimuove un criterio SSL da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="488c5-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="488c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="488c5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="488c5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="488c5-105">DESCRIPTION</span></span>
<span data-ttu-id="488c5-106">Il cmdlet Remove-AzApplicationGatewaySslPolicy rimuove i criteri SSL da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="488c5-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="488c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="488c5-107">EXAMPLES</span></span>

### <span data-ttu-id="488c5-108">Esempio 1: Rimuovere un criterio SSL da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="488c5-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="488c5-109">Questo comando rimuove il criterio SSL dal gateway applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="488c5-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="488c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="488c5-110">PARAMETERS</span></span>

### <span data-ttu-id="488c5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="488c5-111">-ApplicationGateway</span></span>
<span data-ttu-id="488c5-112">Specifica il gateway applicazione da cui questo cmdlet rimuove il criterio SSL.</span><span class="sxs-lookup"><span data-stu-id="488c5-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="488c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488c5-113">-DefaultProfile</span></span>
<span data-ttu-id="488c5-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="488c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="488c5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="488c5-115">-Force</span></span>
<span data-ttu-id="488c5-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="488c5-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="488c5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="488c5-117">-Confirm</span></span>
<span data-ttu-id="488c5-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="488c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="488c5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="488c5-119">-WhatIf</span></span>
<span data-ttu-id="488c5-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488c5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="488c5-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488c5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="488c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488c5-122">CommonParameters</span></span>
<span data-ttu-id="488c5-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="488c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488c5-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488c5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488c5-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="488c5-125">INPUTS</span></span>

### <span data-ttu-id="488c5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="488c5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="488c5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="488c5-127">OUTPUTS</span></span>

### <span data-ttu-id="488c5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="488c5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="488c5-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="488c5-129">NOTES</span></span>
<span data-ttu-id="488c5-130">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="488c5-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="488c5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="488c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="488c5-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="488c5-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="488c5-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="488c5-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="488c5-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="488c5-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

