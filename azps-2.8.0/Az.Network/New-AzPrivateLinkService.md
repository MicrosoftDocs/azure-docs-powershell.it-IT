---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852909"
---
# <span data-ttu-id="a5b10-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5b10-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="a5b10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5b10-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b10-103">Crea un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5b10-103">Creates a private link service</span></span>

## <span data-ttu-id="a5b10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5b10-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5b10-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b10-106">Il cmdlet **New-AzPrivateLinkService** crea un servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5b10-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="a5b10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5b10-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b10-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5b10-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="a5b10-109">Questo esempio crea un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="a5b10-109">This example creates a private link service.</span></span>

## <span data-ttu-id="a5b10-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5b10-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b10-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b10-111">-AsJob</span></span>
<span data-ttu-id="a5b10-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a5b10-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5b10-113">-Autoapprovazione</span><span class="sxs-lookup"><span data-stu-id="a5b10-113">-AutoApproval</span></span>
<span data-ttu-id="a5b10-114">Sottoscrizioni di approvazione automatica del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5b10-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="a5b10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b10-115">-DefaultProfile</span></span>
<span data-ttu-id="a5b10-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b10-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a5b10-117">-Force</span></span>
<span data-ttu-id="a5b10-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="a5b10-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a5b10-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5b10-119">-IpConfiguration</span></span>
<span data-ttu-id="a5b10-120">Configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="a5b10-120">The ip configurations</span></span>

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

### <span data-ttu-id="a5b10-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5b10-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="a5b10-122">Configurazioni IP front-end</span><span class="sxs-lookup"><span data-stu-id="a5b10-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="a5b10-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a5b10-123">-Location</span></span>
<span data-ttu-id="a5b10-124">posizione.</span><span class="sxs-lookup"><span data-stu-id="a5b10-124">location.</span></span>

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

### <span data-ttu-id="a5b10-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5b10-125">-Name</span></span>
<span data-ttu-id="a5b10-126">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a5b10-126">The name of the service.</span></span>

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

### <span data-ttu-id="a5b10-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b10-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5b10-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5b10-128">The resource group name.</span></span>

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

### <span data-ttu-id="a5b10-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5b10-129">-Tag</span></span>
<span data-ttu-id="a5b10-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a5b10-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5b10-131">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a5b10-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a5b10-132">-Visibilità</span><span class="sxs-lookup"><span data-stu-id="a5b10-132">-Visibility</span></span>
<span data-ttu-id="a5b10-133">Abbonamenti alla visibilità del servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5b10-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="a5b10-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5b10-134">-Confirm</span></span>
<span data-ttu-id="a5b10-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b10-136">-WhatIf</span></span>
<span data-ttu-id="a5b10-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5b10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b10-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5b10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b10-139">CommonParameters</span></span>
<span data-ttu-id="a5b10-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b10-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b10-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b10-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5b10-142">INPUTS</span></span>

### <span data-ttu-id="a5b10-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b10-143">System.String</span></span>

### <span data-ttu-id="a5b10-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="a5b10-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="a5b10-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="a5b10-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="a5b10-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5b10-146">OUTPUTS</span></span>

### <span data-ttu-id="a5b10-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5b10-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a5b10-148">Note</span><span class="sxs-lookup"><span data-stu-id="a5b10-148">NOTES</span></span>

## <span data-ttu-id="a5b10-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5b10-149">RELATED LINKS</span></span>

[<span data-ttu-id="a5b10-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5b10-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="a5b10-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a5b10-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="a5b10-152">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a5b10-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
