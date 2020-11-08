---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192322"
---
# <span data-ttu-id="6441e-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6441e-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="6441e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6441e-102">SYNOPSIS</span></span>
<span data-ttu-id="6441e-103">Crea un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="6441e-103">Creates a private link service</span></span>

## <span data-ttu-id="6441e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6441e-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6441e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6441e-105">DESCRIPTION</span></span>
<span data-ttu-id="6441e-106">Il cmdlet **New-AzPrivateLinkService** crea un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="6441e-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="6441e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6441e-107">EXAMPLES</span></span>

### <span data-ttu-id="6441e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6441e-108">Example 1</span></span>

<span data-ttu-id="6441e-109">L'esempio seguente crea un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="6441e-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="6441e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6441e-110">PARAMETERS</span></span>

### <span data-ttu-id="6441e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6441e-111">-AsJob</span></span>
<span data-ttu-id="6441e-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6441e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6441e-113">-Autoapprovazione</span><span class="sxs-lookup"><span data-stu-id="6441e-113">-AutoApproval</span></span>
<span data-ttu-id="6441e-114">Sottoscrizioni di approvazione automatica del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="6441e-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="6441e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6441e-115">-DefaultProfile</span></span>
<span data-ttu-id="6441e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6441e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6441e-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="6441e-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="6441e-118">Abilitare il protocollo proxy per il servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="6441e-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="6441e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6441e-119">-Force</span></span>
<span data-ttu-id="6441e-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6441e-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6441e-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6441e-121">-IpConfiguration</span></span>
<span data-ttu-id="6441e-122">Configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="6441e-122">The ip configurations</span></span>

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

### <span data-ttu-id="6441e-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6441e-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="6441e-124">Configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="6441e-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="6441e-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6441e-125">-Location</span></span>
<span data-ttu-id="6441e-126">posizione.</span><span class="sxs-lookup"><span data-stu-id="6441e-126">location.</span></span>

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

### <span data-ttu-id="6441e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6441e-127">-Name</span></span>
<span data-ttu-id="6441e-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="6441e-128">The name of the service.</span></span>

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

### <span data-ttu-id="6441e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6441e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6441e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6441e-130">The resource group name.</span></span>

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

### <span data-ttu-id="6441e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6441e-131">-Tag</span></span>
<span data-ttu-id="6441e-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6441e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6441e-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6441e-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6441e-134">-Visibilità</span><span class="sxs-lookup"><span data-stu-id="6441e-134">-Visibility</span></span>
<span data-ttu-id="6441e-135">Abbonamenti alla visibilità del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="6441e-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="6441e-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6441e-136">-Confirm</span></span>
<span data-ttu-id="6441e-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6441e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6441e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6441e-138">-WhatIf</span></span>
<span data-ttu-id="6441e-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6441e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6441e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6441e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6441e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6441e-141">CommonParameters</span></span>
<span data-ttu-id="6441e-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6441e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6441e-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6441e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6441e-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6441e-144">INPUTS</span></span>

### <span data-ttu-id="6441e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6441e-145">System.String</span></span>

### <span data-ttu-id="6441e-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6441e-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="6441e-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6441e-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="6441e-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6441e-148">OUTPUTS</span></span>

### <span data-ttu-id="6441e-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6441e-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6441e-150">Note</span><span class="sxs-lookup"><span data-stu-id="6441e-150">NOTES</span></span>

## <span data-ttu-id="6441e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6441e-151">RELATED LINKS</span></span>

[<span data-ttu-id="6441e-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6441e-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="6441e-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6441e-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="6441e-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6441e-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)