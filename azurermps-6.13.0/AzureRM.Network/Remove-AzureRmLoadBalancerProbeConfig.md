---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510856"
---
# <span data-ttu-id="e04f1-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e04f1-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e04f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e04f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e04f1-103">Rimuove la configurazione di una sonda da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e04f1-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e04f1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e04f1-105">DESCRIPTION</span></span>
<span data-ttu-id="e04f1-106">Il cmdlet **Remove-AzureRmLoadBalancerProbeConfig** rimuove una configurazione di probe da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e04f1-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e04f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e04f1-107">EXAMPLES</span></span>

### <span data-ttu-id="e04f1-108">Esempio 1: rimuovere una configurazione di una sonda da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e04f1-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e04f1-109">Il primo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e04f1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="e04f1-110">Il secondo comando Elimina la configurazione denominata Probe dal bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e04f1-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e04f1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e04f1-111">PARAMETERS</span></span>

### <span data-ttu-id="e04f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04f1-112">-DefaultProfile</span></span>
<span data-ttu-id="e04f1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e04f1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04f1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e04f1-114">-LoadBalancer</span></span>
<span data-ttu-id="e04f1-115">Specifica il bilanciamento del carico che contiene la configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f1-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e04f1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e04f1-116">-Name</span></span>
<span data-ttu-id="e04f1-117">Specifica il nome della configurazione della sonda rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f1-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04f1-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e04f1-118">-Confirm</span></span>
<span data-ttu-id="e04f1-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04f1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04f1-120">-WhatIf</span></span>
<span data-ttu-id="e04f1-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e04f1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e04f1-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e04f1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04f1-123">CommonParameters</span></span>
<span data-ttu-id="e04f1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e04f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04f1-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04f1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04f1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e04f1-126">INPUTS</span></span>

### <span data-ttu-id="e04f1-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e04f1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e04f1-128">Parametri: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e04f1-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="e04f1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e04f1-129">OUTPUTS</span></span>

### <span data-ttu-id="e04f1-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e04f1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e04f1-131">Note</span><span class="sxs-lookup"><span data-stu-id="e04f1-131">NOTES</span></span>

## <span data-ttu-id="e04f1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e04f1-132">RELATED LINKS</span></span>

[<span data-ttu-id="e04f1-133">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e04f1-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e04f1-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e04f1-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e04f1-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e04f1-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e04f1-136">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e04f1-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e04f1-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e04f1-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


