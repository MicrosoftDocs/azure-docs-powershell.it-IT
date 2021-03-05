---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e849b109ba1f1fd43ca960d56581357729f5c344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010365"
---
# <span data-ttu-id="df501-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="df501-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="df501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df501-102">SYNOPSIS</span></span>
<span data-ttu-id="df501-103">Crea una configurazione di gradazioni automatica per il Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="df501-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="df501-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df501-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df501-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df501-105">DESCRIPTION</span></span>
<span data-ttu-id="df501-106">Il cmdlet **New-AzApplicationGatewayAutoscaleConfiguration crea** la configurazione di gradazione automatica per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df501-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="df501-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df501-107">EXAMPLES</span></span>

### <span data-ttu-id="df501-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df501-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="df501-109">Il primo comando crea una configurazione di gradazioni automatica con capacità minima 3.</span><span class="sxs-lookup"><span data-stu-id="df501-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="df501-110">Il secondo comando crea un gateway applicazione con la configurazione della gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="df501-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="df501-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df501-111">PARAMETERS</span></span>

### <span data-ttu-id="df501-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df501-112">-DefaultProfile</span></span>
<span data-ttu-id="df501-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df501-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df501-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="df501-114">-MaxCapacity</span></span>
<span data-ttu-id="df501-115">Unità di capacità massime che saranno sempre disponibili [e addebitate] per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="df501-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="df501-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="df501-116">-MinCapacity</span></span>
<span data-ttu-id="df501-117">Unità di capacità minime che saranno sempre disponibili [e addebitate] per il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="df501-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="df501-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df501-118">-Confirm</span></span>
<span data-ttu-id="df501-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df501-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df501-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df501-120">-WhatIf</span></span>
<span data-ttu-id="df501-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df501-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df501-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df501-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df501-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df501-123">CommonParameters</span></span>
<span data-ttu-id="df501-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df501-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df501-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df501-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df501-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="df501-126">INPUTS</span></span>

### <span data-ttu-id="df501-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="df501-127">None</span></span>

## <span data-ttu-id="df501-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df501-128">OUTPUTS</span></span>

### <span data-ttu-id="df501-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="df501-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="df501-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="df501-130">NOTES</span></span>

## <span data-ttu-id="df501-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df501-131">RELATED LINKS</span></span>

[<span data-ttu-id="df501-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="df501-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="df501-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="df501-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="df501-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="df501-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
