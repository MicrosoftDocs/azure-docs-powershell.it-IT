---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378839"
---
# <span data-ttu-id="6358a-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6358a-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6358a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6358a-102">SYNOPSIS</span></span>
<span data-ttu-id="6358a-103">Rimuove la configurazione di scala automatica da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6358a-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="6358a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6358a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6358a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6358a-105">DESCRIPTION</span></span>
<span data-ttu-id="6358a-106">Il cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** rimuove la configurazione di scala automatica da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="6358a-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="6358a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6358a-107">EXAMPLES</span></span>

### <span data-ttu-id="6358a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6358a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6358a-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="6358a-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="6358a-110">Il secondo comando rimuove la configurazione di scala automatica dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6358a-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="6358a-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="6358a-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6358a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6358a-112">PARAMETERS</span></span>

### <span data-ttu-id="6358a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6358a-113">-ApplicationGateway</span></span>
<span data-ttu-id="6358a-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6358a-114">The applicationGateway</span></span>

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

### <span data-ttu-id="6358a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6358a-115">-DefaultProfile</span></span>
<span data-ttu-id="6358a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6358a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6358a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6358a-117">-Force</span></span>
<span data-ttu-id="6358a-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6358a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6358a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6358a-119">-Confirm</span></span>
<span data-ttu-id="6358a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6358a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6358a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6358a-121">-WhatIf</span></span>
<span data-ttu-id="6358a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6358a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6358a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6358a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6358a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6358a-124">CommonParameters</span></span>
<span data-ttu-id="6358a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6358a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6358a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6358a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6358a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6358a-127">INPUTS</span></span>

### <span data-ttu-id="6358a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6358a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6358a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6358a-129">OUTPUTS</span></span>

### <span data-ttu-id="6358a-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6358a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6358a-131">Note</span><span class="sxs-lookup"><span data-stu-id="6358a-131">NOTES</span></span>

## <span data-ttu-id="6358a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6358a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6358a-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6358a-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6358a-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6358a-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6358a-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6358a-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
