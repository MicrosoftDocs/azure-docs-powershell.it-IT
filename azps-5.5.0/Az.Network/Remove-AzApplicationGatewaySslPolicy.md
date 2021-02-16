---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179534"
---
# <span data-ttu-id="deb6f-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="deb6f-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="deb6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="deb6f-103">Rimuove un criterio SSL da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="deb6f-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="deb6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="deb6f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb6f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="deb6f-105">DESCRIPTION</span></span>
<span data-ttu-id="deb6f-106">Il cmdlet Remove-AzApplicationGatewaySslPolicy rimuove i criteri SSL da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="deb6f-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="deb6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="deb6f-107">EXAMPLES</span></span>

### <span data-ttu-id="deb6f-108">Esempio 1: Rimuovere un criterio SSL da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="deb6f-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="deb6f-109">Questo comando rimuove il criterio SSL dal gateway applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="deb6f-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="deb6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deb6f-110">PARAMETERS</span></span>

### <span data-ttu-id="deb6f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deb6f-111">-ApplicationGateway</span></span>
<span data-ttu-id="deb6f-112">Specifica il gateway applicazione da cui questo cmdlet rimuove i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="deb6f-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="deb6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb6f-113">-DefaultProfile</span></span>
<span data-ttu-id="deb6f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="deb6f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deb6f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="deb6f-115">-Force</span></span>
<span data-ttu-id="deb6f-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="deb6f-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="deb6f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deb6f-117">-Confirm</span></span>
<span data-ttu-id="deb6f-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb6f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb6f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb6f-119">-WhatIf</span></span>
<span data-ttu-id="deb6f-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deb6f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb6f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="deb6f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb6f-122">CommonParameters</span></span>
<span data-ttu-id="deb6f-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb6f-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb6f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb6f-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="deb6f-125">INPUTS</span></span>

### <span data-ttu-id="deb6f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deb6f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="deb6f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="deb6f-127">OUTPUTS</span></span>

### <span data-ttu-id="deb6f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deb6f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="deb6f-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="deb6f-129">NOTES</span></span>
<span data-ttu-id="deb6f-130">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="deb6f-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="deb6f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="deb6f-131">RELATED LINKS</span></span>

[<span data-ttu-id="deb6f-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="deb6f-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="deb6f-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="deb6f-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="deb6f-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="deb6f-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

