---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202688"
---
# <span data-ttu-id="86c78-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86c78-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="86c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c78-102">SYNOPSIS</span></span>
<span data-ttu-id="86c78-103">Crea una risorsa VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="86c78-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="86c78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86c78-104">SYNTAX</span></span>

### <span data-ttu-id="86c78-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86c78-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c78-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="86c78-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c78-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86c78-107">DESCRIPTION</span></span>
<span data-ttu-id="86c78-108">Il cmdlet **New-AzVirtualNetworkTap** crea una risorsa Tocco rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="86c78-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="86c78-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86c78-109">EXAMPLES</span></span>

### <span data-ttu-id="86c78-110">Esempio 1: Toccare Crea una rete virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="86c78-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="86c78-111">Questo comando crea un tocco di rete virtuale denominato "VirtualNetworkTap1" con i dettagli di configurazione della macchina virtuale di destinazione (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="86c78-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="86c78-112">Tutto il traffico della MACCHINA configurato per il tocco di origine verrà instradato a questo INDIRIZZO IP di destinazione + Porta.</span><span class="sxs-lookup"><span data-stu-id="86c78-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="86c78-113">Esempio 2: Creare un tocco di rete virtuale di Azure usando LoadBalancer IP</span><span class="sxs-lookup"><span data-stu-id="86c78-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="86c78-114">Questo comando crea un tocco di rete virtuale denominato "VirtualNetworkTap1" con i dettagli di configurazione della macchina virtuale di destinazione (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="86c78-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="86c78-115">Tutto il traffico della macchina virtuale configurata con tocco di origine verrà instradato a questa IpConfiguration di LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="86c78-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="86c78-116">La porta di destinazione predefinita è 4789.</span><span class="sxs-lookup"><span data-stu-id="86c78-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="86c78-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86c78-117">PARAMETERS</span></span>

### <span data-ttu-id="86c78-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86c78-118">-AsJob</span></span>
<span data-ttu-id="86c78-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="86c78-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86c78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c78-120">-DefaultProfile</span></span>
<span data-ttu-id="86c78-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86c78-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c78-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="86c78-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="86c78-123">Riferimento alla risorsa configurazione IP front-end di bilanciamento del carico di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86c78-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="86c78-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="86c78-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="86c78-125">Riferimento alla risorsa configurazione IP front-end di bilanciamento del carico di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86c78-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="86c78-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="86c78-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="86c78-127">Riferimento alla risorsa di configurazione IP dell'interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86c78-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="86c78-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="86c78-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="86c78-129">Riferimento alla risorsa di configurazione IP dell'interfaccia di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="86c78-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="86c78-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="86c78-130">-DestinationPort</span></span>
<span data-ttu-id="86c78-131">La porta di destinazione dell'agente di raccolta pacchetti</span><span class="sxs-lookup"><span data-stu-id="86c78-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="86c78-132">-Force</span><span class="sxs-lookup"><span data-stu-id="86c78-132">-Force</span></span>
<span data-ttu-id="86c78-133">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="86c78-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="86c78-134">-Location</span><span class="sxs-lookup"><span data-stu-id="86c78-134">-Location</span></span>
<span data-ttu-id="86c78-135">Posizione.</span><span class="sxs-lookup"><span data-stu-id="86c78-135">The location.</span></span>

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

### <span data-ttu-id="86c78-136">-Name</span><span class="sxs-lookup"><span data-stu-id="86c78-136">-Name</span></span>
<span data-ttu-id="86c78-137">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="86c78-137">The name of the tap.</span></span>

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

### <span data-ttu-id="86c78-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c78-138">-ResourceGroupName</span></span>
<span data-ttu-id="86c78-139">Il nome del gruppo di risorse del tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="86c78-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="86c78-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="86c78-140">-Tag</span></span>
<span data-ttu-id="86c78-141">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="86c78-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="86c78-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86c78-142">-Confirm</span></span>
<span data-ttu-id="86c78-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c78-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c78-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c78-144">-WhatIf</span></span>
<span data-ttu-id="86c78-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86c78-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c78-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86c78-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c78-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c78-147">CommonParameters</span></span>
<span data-ttu-id="86c78-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c78-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c78-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c78-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c78-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="86c78-150">INPUTS</span></span>

### <span data-ttu-id="86c78-151">System.String</span><span class="sxs-lookup"><span data-stu-id="86c78-151">System.String</span></span>

### <span data-ttu-id="86c78-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="86c78-152">System.Int32</span></span>

### <span data-ttu-id="86c78-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="86c78-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="86c78-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="86c78-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="86c78-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="86c78-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="86c78-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86c78-156">OUTPUTS</span></span>

### <span data-ttu-id="86c78-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86c78-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="86c78-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="86c78-158">NOTES</span></span>

## <span data-ttu-id="86c78-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86c78-159">RELATED LINKS</span></span>

[<span data-ttu-id="86c78-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86c78-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="86c78-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86c78-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="86c78-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="86c78-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
