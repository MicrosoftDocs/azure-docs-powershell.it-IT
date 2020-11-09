---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310854"
---
# <span data-ttu-id="6f03c-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6f03c-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6f03c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f03c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f03c-103">Rimuove un criterio SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6f03c-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="6f03c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f03c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f03c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f03c-105">DESCRIPTION</span></span>
<span data-ttu-id="6f03c-106">Il cmdlet Remove-AzApplicationGatewaySslPolicy rimuove i criteri SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6f03c-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="6f03c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f03c-107">EXAMPLES</span></span>

### <span data-ttu-id="6f03c-108">Esempio 1: rimuovere un criterio SSL da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="6f03c-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="6f03c-109">Questo comando rimuove i criteri SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="6f03c-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="6f03c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f03c-110">PARAMETERS</span></span>

### <span data-ttu-id="6f03c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f03c-111">-ApplicationGateway</span></span>
<span data-ttu-id="6f03c-112">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="6f03c-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="6f03c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f03c-113">-DefaultProfile</span></span>
<span data-ttu-id="6f03c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f03c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f03c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f03c-115">-Force</span></span>
<span data-ttu-id="6f03c-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6f03c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6f03c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6f03c-117">-Confirm</span></span>
<span data-ttu-id="6f03c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f03c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f03c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f03c-119">-WhatIf</span></span>
<span data-ttu-id="6f03c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f03c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f03c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f03c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f03c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f03c-122">CommonParameters</span></span>
<span data-ttu-id="6f03c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f03c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f03c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f03c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f03c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f03c-125">INPUTS</span></span>

### <span data-ttu-id="6f03c-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f03c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f03c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f03c-127">OUTPUTS</span></span>

### <span data-ttu-id="6f03c-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f03c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f03c-129">Note</span><span class="sxs-lookup"><span data-stu-id="6f03c-129">NOTES</span></span>
<span data-ttu-id="6f03c-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="6f03c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6f03c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f03c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6f03c-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6f03c-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6f03c-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6f03c-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6f03c-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6f03c-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

