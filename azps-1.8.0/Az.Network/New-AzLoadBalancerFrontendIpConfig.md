---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0299494ca775df60c94151f36efe554d0b876d22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678281"
---
# <span data-ttu-id="d86db-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d86db-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d86db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d86db-102">SYNOPSIS</span></span>
<span data-ttu-id="d86db-103">Crea una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d86db-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="d86db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d86db-104">SYNTAX</span></span>

### <span data-ttu-id="d86db-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d86db-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86db-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="d86db-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86db-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86db-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d86db-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d86db-109">DESCRIPTION</span></span>
<span data-ttu-id="d86db-110">Il cmdlet **New-AzLoadBalancerFrontendIpConfig** crea una configurazione IP front-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="d86db-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d86db-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d86db-111">EXAMPLES</span></span>

### <span data-ttu-id="d86db-112">Esempio 1: creare una configurazione IP front-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="d86db-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="d86db-113">Il primo comando crea un indirizzo IP pubblico dinamico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="d86db-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="d86db-114">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip.</span><span class="sxs-lookup"><span data-stu-id="d86db-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="d86db-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d86db-115">PARAMETERS</span></span>

### <span data-ttu-id="d86db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86db-116">-DefaultProfile</span></span>
<span data-ttu-id="d86db-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d86db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d86db-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d86db-118">-Name</span></span>
<span data-ttu-id="d86db-119">Specifica la configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d86db-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-120">-PrivateIpAddress</span></span>
<span data-ttu-id="d86db-121">Specifica l'indirizzo IP privato del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="d86db-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="d86db-122">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="d86db-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-123">-PublicIpAddress</span></span>
<span data-ttu-id="d86db-124">Specifica l'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="d86db-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d86db-125">-PublicIpAddressId</span></span>
<span data-ttu-id="d86db-126">Specifica l'ID dell'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="d86db-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d86db-127">-Subnet</span></span>
<span data-ttu-id="d86db-128">Specifica l'oggetto **subnet** in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="d86db-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d86db-129">-SubnetId</span></span>
<span data-ttu-id="d86db-130">Specifica l'ID della subnet in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="d86db-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86db-131">-Zona</span><span class="sxs-lookup"><span data-stu-id="d86db-131">-Zone</span></span>
<span data-ttu-id="d86db-132">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="d86db-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="d86db-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d86db-133">-Confirm</span></span>
<span data-ttu-id="d86db-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d86db-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d86db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86db-135">-WhatIf</span></span>
<span data-ttu-id="d86db-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d86db-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d86db-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d86db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d86db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86db-138">CommonParameters</span></span>
<span data-ttu-id="d86db-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d86db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86db-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86db-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86db-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d86db-141">INPUTS</span></span>

### <span data-ttu-id="d86db-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d86db-142">System.String</span></span>

### <span data-ttu-id="d86db-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="d86db-143">System.String[]</span></span>

### <span data-ttu-id="d86db-144">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d86db-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="d86db-145">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-145">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d86db-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d86db-146">OUTPUTS</span></span>

### <span data-ttu-id="d86db-147">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d86db-147">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d86db-148">Note</span><span class="sxs-lookup"><span data-stu-id="d86db-148">NOTES</span></span>

## <span data-ttu-id="d86db-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d86db-149">RELATED LINKS</span></span>

[<span data-ttu-id="d86db-150">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d86db-150">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d86db-151">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d86db-151">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d86db-152">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d86db-152">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d86db-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d86db-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d86db-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d86db-154">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

