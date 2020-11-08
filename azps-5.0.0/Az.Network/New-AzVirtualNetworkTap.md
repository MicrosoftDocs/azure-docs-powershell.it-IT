---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201575"
---
# <span data-ttu-id="ecf6e-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecf6e-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="ecf6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf6e-103">Crea una risorsa VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ecf6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-104">SYNTAX</span></span>

### <span data-ttu-id="ecf6e-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecf6e-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf6e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf6e-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf6e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf6e-107">DESCRIPTION</span></span>
<span data-ttu-id="ecf6e-108">Il cmdlet **New-AzVirtualNetworkTap** crea una risorsa tap di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="ecf6e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-109">EXAMPLES</span></span>

### <span data-ttu-id="ecf6e-110">Esempio 1: creare un tocco di rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="ecf6e-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="ecf6e-111">Questo comando crea un tocco di rete virtuale denominato "VirtualNetworkTap1" con i dettagli di configurazione della VM di destinazione (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="ecf6e-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="ecf6e-112">Tutti i sorgenti toccare il traffico della VM configurata verranno indirizzati a questa porta IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="ecf6e-113">Esempio 2: creare un tocco di rete virtuale di Azure usando LoadBalancer IP</span><span class="sxs-lookup"><span data-stu-id="ecf6e-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="ecf6e-114">Questo comando crea un tocco di rete virtuale denominato "VirtualNetworkTap1" con i dettagli di configurazione della VM di destinazione (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="ecf6e-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="ecf6e-115">Tutti i sorgenti toccare il traffico della VM configurata verranno indirizzati a questo LoadBalancer IpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="ecf6e-116">La porta di destinazione predefinita è 4789.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="ecf6e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-117">PARAMETERS</span></span>

### <span data-ttu-id="ecf6e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecf6e-118">-AsJob</span></span>
<span data-ttu-id="ecf6e-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ecf6e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecf6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf6e-120">-DefaultProfile</span></span>
<span data-ttu-id="ecf6e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf6e-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf6e-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="ecf6e-123">Riferimento della risorsa di configurazione di front-end IP di bilanciamento del carico di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ecf6e-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="ecf6e-125">Riferimento della risorsa di configurazione di front-end IP di bilanciamento del carico di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf6e-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="ecf6e-127">Riferimento della risorsa di configurazione IP dell'interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ecf6e-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="ecf6e-129">Riferimento della risorsa di configurazione IP dell'interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ecf6e-130">-DestinationPort</span></span>
<span data-ttu-id="ecf6e-131">Porta di destinazione del raccoglitore di pacchetti</span><span class="sxs-lookup"><span data-stu-id="ecf6e-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ecf6e-132">-Force</span></span>
<span data-ttu-id="ecf6e-133">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="ecf6e-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ecf6e-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ecf6e-134">-Location</span></span>
<span data-ttu-id="ecf6e-135">La posizione.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecf6e-136">-Name</span></span>
<span data-ttu-id="ecf6e-137">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-137">The name of the tap.</span></span>

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

### <span data-ttu-id="ecf6e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf6e-138">-ResourceGroupName</span></span>
<span data-ttu-id="ecf6e-139">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="ecf6e-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecf6e-140">-Tag</span></span>
<span data-ttu-id="ecf6e-141">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf6e-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecf6e-142">-Confirm</span></span>
<span data-ttu-id="ecf6e-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf6e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf6e-144">-WhatIf</span></span>
<span data-ttu-id="ecf6e-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf6e-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf6e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf6e-147">CommonParameters</span></span>
<span data-ttu-id="ecf6e-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf6e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf6e-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf6e-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf6e-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-150">INPUTS</span></span>

### <span data-ttu-id="ecf6e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf6e-151">System.String</span></span>

### <span data-ttu-id="ecf6e-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ecf6e-152">System.Int32</span></span>

### <span data-ttu-id="ecf6e-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecf6e-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ecf6e-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf6e-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="ecf6e-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecf6e-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ecf6e-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecf6e-156">OUTPUTS</span></span>

### <span data-ttu-id="ecf6e-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecf6e-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ecf6e-158">Note</span><span class="sxs-lookup"><span data-stu-id="ecf6e-158">NOTES</span></span>

## <span data-ttu-id="ecf6e-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecf6e-159">RELATED LINKS</span></span>

[<span data-ttu-id="ecf6e-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecf6e-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="ecf6e-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecf6e-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="ecf6e-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecf6e-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
