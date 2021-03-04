---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: bfa5cbfdb8ab734a8c6ca8b651808213b9b10f3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958110"
---
# <span data-ttu-id="c9311-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9311-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c9311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9311-102">SYNOPSIS</span></span>
<span data-ttu-id="c9311-103">Aggiorna la configurazione della scala automatica di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c9311-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="c9311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9311-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9311-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9311-105">DESCRIPTION</span></span>
<span data-ttu-id="c9311-106">Il cmdlet **Set-AzApplicationGatewayAutoscaleConfiguration** modifica la configurazione esistente di gradazioni automatiche di un Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9311-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="c9311-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9311-107">EXAMPLES</span></span>

### <span data-ttu-id="c9311-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9311-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c9311-109">Il primo comando recupera il gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="c9311-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c9311-110">Il secondo comando aggiorna la configurazione di gradazioni automatica dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9311-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="c9311-111">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c9311-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c9311-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9311-112">PARAMETERS</span></span>

### <span data-ttu-id="c9311-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9311-113">-ApplicationGateway</span></span>
<span data-ttu-id="c9311-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9311-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c9311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9311-115">-DefaultProfile</span></span>
<span data-ttu-id="c9311-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9311-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9311-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="c9311-117">-MaxCapacity</span></span>
<span data-ttu-id="c9311-118">Capacità massima per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9311-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9311-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c9311-119">-MinCapacity</span></span>
<span data-ttu-id="c9311-120">Capacità minima per il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c9311-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9311-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9311-121">-Confirm</span></span>
<span data-ttu-id="c9311-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9311-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9311-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9311-123">-WhatIf</span></span>
<span data-ttu-id="c9311-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9311-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9311-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9311-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9311-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9311-126">CommonParameters</span></span>
<span data-ttu-id="c9311-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9311-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9311-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9311-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9311-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9311-129">INPUTS</span></span>

### <span data-ttu-id="c9311-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9311-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9311-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9311-131">OUTPUTS</span></span>

### <span data-ttu-id="c9311-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9311-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9311-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9311-133">NOTES</span></span>

## <span data-ttu-id="c9311-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9311-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9311-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9311-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9311-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9311-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9311-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9311-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
