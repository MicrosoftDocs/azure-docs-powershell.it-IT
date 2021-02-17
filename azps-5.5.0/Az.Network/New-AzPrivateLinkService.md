---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184375"
---
# <span data-ttu-id="c335f-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c335f-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="c335f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c335f-102">SYNOPSIS</span></span>
<span data-ttu-id="c335f-103">Crea un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="c335f-103">Creates a private link service</span></span>

## <span data-ttu-id="c335f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c335f-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c335f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c335f-105">DESCRIPTION</span></span>
<span data-ttu-id="c335f-106">Il cmdlet **New-AzPrivateLinkService crea** un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="c335f-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="c335f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c335f-107">EXAMPLES</span></span>

### <span data-ttu-id="c335f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c335f-108">Example 1</span></span>

<span data-ttu-id="c335f-109">L'esempio seguente crea un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="c335f-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="c335f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c335f-110">PARAMETERS</span></span>

### <span data-ttu-id="c335f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c335f-111">-AsJob</span></span>
<span data-ttu-id="c335f-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c335f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c335f-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="c335f-113">-AutoApproval</span></span>
<span data-ttu-id="c335f-114">Sottoscrizioni di approvazione automatica del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="c335f-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c335f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c335f-115">-DefaultProfile</span></span>
<span data-ttu-id="c335f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c335f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c335f-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="c335f-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="c335f-118">Abilitare il protocollo proxy per il servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="c335f-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="c335f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c335f-119">-Force</span></span>
<span data-ttu-id="c335f-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="c335f-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c335f-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c335f-121">-IpConfiguration</span></span>
<span data-ttu-id="c335f-122">Le configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="c335f-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c335f-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c335f-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="c335f-124">Le configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="c335f-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c335f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="c335f-125">-Location</span></span>
<span data-ttu-id="c335f-126">posizione.</span><span class="sxs-lookup"><span data-stu-id="c335f-126">location.</span></span>

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

### <span data-ttu-id="c335f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c335f-127">-Name</span></span>
<span data-ttu-id="c335f-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="c335f-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c335f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c335f-129">-ResourceGroupName</span></span>
<span data-ttu-id="c335f-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c335f-130">The resource group name.</span></span>

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

### <span data-ttu-id="c335f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c335f-131">-Tag</span></span>
<span data-ttu-id="c335f-132">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c335f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c335f-133">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c335f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c335f-134">-Visibility</span><span class="sxs-lookup"><span data-stu-id="c335f-134">-Visibility</span></span>
<span data-ttu-id="c335f-135">Sottoscrizioni della visibilità del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="c335f-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c335f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c335f-136">-Confirm</span></span>
<span data-ttu-id="c335f-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c335f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c335f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c335f-138">-WhatIf</span></span>
<span data-ttu-id="c335f-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c335f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c335f-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c335f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c335f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c335f-141">CommonParameters</span></span>
<span data-ttu-id="c335f-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c335f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c335f-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c335f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c335f-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="c335f-144">INPUTS</span></span>

### <span data-ttu-id="c335f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c335f-145">System.String</span></span>

### <span data-ttu-id="c335f-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c335f-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="c335f-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c335f-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="c335f-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c335f-148">OUTPUTS</span></span>

### <span data-ttu-id="c335f-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c335f-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c335f-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="c335f-150">NOTES</span></span>

## <span data-ttu-id="c335f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c335f-151">RELATED LINKS</span></span>

[<span data-ttu-id="c335f-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c335f-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="c335f-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c335f-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="c335f-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c335f-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
