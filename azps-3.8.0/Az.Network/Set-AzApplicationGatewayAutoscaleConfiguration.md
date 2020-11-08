---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021884"
---
# <span data-ttu-id="c5678-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5678-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c5678-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5678-102">SYNOPSIS</span></span>
<span data-ttu-id="c5678-103">Aggiorna la configurazione di un gateway applicazione in scala automatica.</span><span class="sxs-lookup"><span data-stu-id="c5678-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="c5678-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5678-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5678-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5678-105">DESCRIPTION</span></span>
<span data-ttu-id="c5678-106">Il cmdlet **set-AzApplicationGatewayAutoscaleConfiguration** modifica la configurazione di scala automatica esistente di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5678-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="c5678-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5678-107">EXAMPLES</span></span>

### <span data-ttu-id="c5678-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5678-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c5678-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="c5678-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c5678-110">Il secondo comando Aggiorna la configurazione di scala automatica dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5678-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="c5678-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c5678-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c5678-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5678-112">PARAMETERS</span></span>

### <span data-ttu-id="c5678-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5678-113">-ApplicationGateway</span></span>
<span data-ttu-id="c5678-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5678-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c5678-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5678-115">-DefaultProfile</span></span>
<span data-ttu-id="c5678-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5678-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5678-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="c5678-117">-MaxCapacity</span></span>
<span data-ttu-id="c5678-118">Capacità massima per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5678-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="c5678-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c5678-119">-MinCapacity</span></span>
<span data-ttu-id="c5678-120">Capacità minima per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5678-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="c5678-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5678-121">-Confirm</span></span>
<span data-ttu-id="c5678-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5678-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5678-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5678-123">-WhatIf</span></span>
<span data-ttu-id="c5678-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5678-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5678-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5678-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5678-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5678-126">CommonParameters</span></span>
<span data-ttu-id="c5678-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5678-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5678-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5678-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5678-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5678-129">INPUTS</span></span>

### <span data-ttu-id="c5678-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5678-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5678-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5678-131">OUTPUTS</span></span>

### <span data-ttu-id="c5678-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5678-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5678-133">Note</span><span class="sxs-lookup"><span data-stu-id="c5678-133">NOTES</span></span>

## <span data-ttu-id="c5678-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5678-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5678-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5678-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c5678-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5678-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c5678-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5678-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
