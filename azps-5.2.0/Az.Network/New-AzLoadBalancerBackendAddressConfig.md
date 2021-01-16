---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341335"
---
# <span data-ttu-id="cecda-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="cecda-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="cecda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cecda-102">SYNOPSIS</span></span>
<span data-ttu-id="cecda-103">Restituisce una configurazione dell'indirizzo backend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cecda-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="cecda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cecda-104">SYNTAX</span></span>

### <span data-ttu-id="cecda-105">SetByResourcePublicIpAddress (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cecda-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cecda-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cecda-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cecda-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cecda-107">DESCRIPTION</span></span>
<span data-ttu-id="cecda-108">Restituisce una configurazione dell'indirizzo backend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cecda-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="cecda-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cecda-109">EXAMPLES</span></span>

### <span data-ttu-id="cecda-110">Esempio 1: nuova configurazione dell'indirizzo LoadBalancer con riferimento alla rete virtuale</span><span class="sxs-lookup"><span data-stu-id="cecda-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="cecda-111">Esempio 2: nuova configurazione degli indirizzi di LoadBalancer con riferimento per le configurazioni IP di LoadBalancer frontend</span><span class="sxs-lookup"><span data-stu-id="cecda-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="cecda-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cecda-112">PARAMETERS</span></span>

### <span data-ttu-id="cecda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecda-113">-DefaultProfile</span></span>
<span data-ttu-id="cecda-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cecda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cecda-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="cecda-115">-IpAddress</span></span>
<span data-ttu-id="cecda-116">IPAddress da aggiungere al pool back-end</span><span class="sxs-lookup"><span data-stu-id="cecda-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecda-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cecda-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="cecda-118">Configurazione IP dell'interfaccia di bilanciamento del carico associata all'indirizzo di backend config</span><span class="sxs-lookup"><span data-stu-id="cecda-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecda-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cecda-119">-Name</span></span>
<span data-ttu-id="cecda-120">Nome della configurazione dell'indirizzo back-end</span><span class="sxs-lookup"><span data-stu-id="cecda-120">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecda-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cecda-121">-VirtualNetworkId</span></span>
<span data-ttu-id="cecda-122">Rete virtuale associata alla configurazione dell'indirizzo backend</span><span class="sxs-lookup"><span data-stu-id="cecda-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecda-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cecda-123">-Confirm</span></span>
<span data-ttu-id="cecda-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cecda-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cecda-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cecda-125">-WhatIf</span></span>
<span data-ttu-id="cecda-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cecda-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cecda-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cecda-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cecda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecda-128">CommonParameters</span></span>
<span data-ttu-id="cecda-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cecda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecda-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cecda-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecda-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cecda-131">INPUTS</span></span>

### <span data-ttu-id="cecda-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cecda-132">System.String</span></span>

### <span data-ttu-id="cecda-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecda-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cecda-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cecda-134">OUTPUTS</span></span>

### <span data-ttu-id="cecda-135">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="cecda-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="cecda-136">Note</span><span class="sxs-lookup"><span data-stu-id="cecda-136">NOTES</span></span>

## <span data-ttu-id="cecda-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cecda-137">RELATED LINKS</span></span>
