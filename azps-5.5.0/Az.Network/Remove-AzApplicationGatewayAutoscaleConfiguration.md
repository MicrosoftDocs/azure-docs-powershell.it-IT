---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179558"
---
# <span data-ttu-id="339fa-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="339fa-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="339fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339fa-102">SYNOPSIS</span></span>
<span data-ttu-id="339fa-103">Rimuove la configurazione della scala automatica da un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="339fa-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="339fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="339fa-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339fa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="339fa-105">DESCRIPTION</span></span>
<span data-ttu-id="339fa-106">Il cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** rimuove la configurazione di gradazione automatica da un Gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="339fa-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="339fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="339fa-107">EXAMPLES</span></span>

### <span data-ttu-id="339fa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="339fa-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="339fa-109">Il primo comando recupera il gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="339fa-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="339fa-110">Il secondo comando rimuove la configurazione di gradazioni automatica dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="339fa-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="339fa-111">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="339fa-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="339fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="339fa-112">PARAMETERS</span></span>

### <span data-ttu-id="339fa-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="339fa-113">-ApplicationGateway</span></span>
<span data-ttu-id="339fa-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="339fa-114">The applicationGateway</span></span>

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

### <span data-ttu-id="339fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339fa-115">-DefaultProfile</span></span>
<span data-ttu-id="339fa-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="339fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339fa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="339fa-117">-Force</span></span>
<span data-ttu-id="339fa-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="339fa-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="339fa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339fa-119">-Confirm</span></span>
<span data-ttu-id="339fa-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="339fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339fa-121">-WhatIf</span></span>
<span data-ttu-id="339fa-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="339fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339fa-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="339fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339fa-124">CommonParameters</span></span>
<span data-ttu-id="339fa-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339fa-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339fa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339fa-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="339fa-127">INPUTS</span></span>

### <span data-ttu-id="339fa-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="339fa-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="339fa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="339fa-129">OUTPUTS</span></span>

### <span data-ttu-id="339fa-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="339fa-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="339fa-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="339fa-131">NOTES</span></span>

## <span data-ttu-id="339fa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="339fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="339fa-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="339fa-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="339fa-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="339fa-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="339fa-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="339fa-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
