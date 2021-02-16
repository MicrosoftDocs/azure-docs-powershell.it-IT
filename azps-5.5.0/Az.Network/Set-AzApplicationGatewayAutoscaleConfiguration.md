---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179390"
---
# <span data-ttu-id="fb95f-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb95f-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="fb95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb95f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb95f-103">Aggiorna la configurazione della gradazione automatica di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fb95f-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="fb95f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb95f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb95f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fb95f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb95f-106">Il cmdlet **Set-AzApplicationGatewayAutoscaleConfiguration** modifica la configurazione esistente di gradazioni automatiche di un Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb95f-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="fb95f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb95f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb95f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb95f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="fb95f-109">Il primo comando recupera il gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="fb95f-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="fb95f-110">Il secondo comando aggiorna la configurazione di gradazioni automatica dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb95f-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="fb95f-111">Il terzo comando aggiorna il gateway applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="fb95f-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="fb95f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb95f-112">PARAMETERS</span></span>

### <span data-ttu-id="fb95f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb95f-113">-ApplicationGateway</span></span>
<span data-ttu-id="fb95f-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb95f-114">The applicationGateway</span></span>

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

### <span data-ttu-id="fb95f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb95f-115">-DefaultProfile</span></span>
<span data-ttu-id="fb95f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb95f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb95f-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="fb95f-117">-MaxCapacity</span></span>
<span data-ttu-id="fb95f-118">Capacità massima per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb95f-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="fb95f-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="fb95f-119">-MinCapacity</span></span>
<span data-ttu-id="fb95f-120">Capacità minima per il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fb95f-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="fb95f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb95f-121">-Confirm</span></span>
<span data-ttu-id="fb95f-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb95f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb95f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb95f-123">-WhatIf</span></span>
<span data-ttu-id="fb95f-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb95f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb95f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb95f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb95f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb95f-126">CommonParameters</span></span>
<span data-ttu-id="fb95f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb95f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb95f-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb95f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb95f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="fb95f-129">INPUTS</span></span>

### <span data-ttu-id="fb95f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb95f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb95f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb95f-131">OUTPUTS</span></span>

### <span data-ttu-id="fb95f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb95f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb95f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="fb95f-133">NOTES</span></span>

## <span data-ttu-id="fb95f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb95f-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb95f-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb95f-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="fb95f-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb95f-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="fb95f-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb95f-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
