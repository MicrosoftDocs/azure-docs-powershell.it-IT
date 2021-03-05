---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011134"
---
# <span data-ttu-id="f84cd-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="f84cd-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="f84cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f84cd-103">Crea un ambiente del servizio app che include la tabella di route consigliata e il gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="f84cd-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="f84cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f84cd-104">SYNTAX</span></span>

### <span data-ttu-id="f84cd-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84cd-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84cd-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84cd-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84cd-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84cd-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84cd-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84cd-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84cd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f84cd-109">DESCRIPTION</span></span>
<span data-ttu-id="f84cd-110">Il cmdlet **New-AzAppServiceEnvironment** crea un ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="f84cd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f84cd-111">EXAMPLES</span></span>

### <span data-ttu-id="f84cd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f84cd-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="f84cd-113">Creare un ambiente del servizio app denominato MyAseV2 che include la tabella di route consigliata e il gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="f84cd-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="f84cd-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f84cd-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="f84cd-115">Creare un ambiente del servizio app denominato MyAseV2 senza la tabella di route consigliata e il gruppo di sicurezza di rete consigliati.</span><span class="sxs-lookup"><span data-stu-id="f84cd-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="f84cd-116">Devono essere create prima o subito dopo il provisioning dell'ambiente del servizio app per garantire un'istanza funzionale.</span><span class="sxs-lookup"><span data-stu-id="f84cd-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="f84cd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84cd-117">PARAMETERS</span></span>

### <span data-ttu-id="f84cd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f84cd-118">-AsJob</span></span>
<span data-ttu-id="f84cd-119">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f84cd-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f84cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84cd-120">-DefaultProfile</span></span>
<span data-ttu-id="f84cd-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f84cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84cd-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="f84cd-122">-Kind</span></span>
<span data-ttu-id="f84cd-123">Versione dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="f84cd-124">-LoadBalancerMode</span></span>
<span data-ttu-id="f84cd-125">Modalità di bilanciamento del carico dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f84cd-126">-Location</span></span>
<span data-ttu-id="f84cd-127">Posizione dell'ambiente del servizio app, ad esempio Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="f84cd-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f84cd-128">-Name</span></span>
<span data-ttu-id="f84cd-129">Nome dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f84cd-130">-PassThru</span></span>
<span data-ttu-id="f84cd-131">Restituire l'oggetto ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="f84cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="f84cd-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f84cd-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f84cd-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="f84cd-135">Non creare il gruppo di sicurezza di rete consigliato come parte dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="f84cd-136">-SkipRouteTable</span></span>
<span data-ttu-id="f84cd-137">Non creare la tabella di route consigliata come parte dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="f84cd-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f84cd-138">-SubnetId</span></span>
<span data-ttu-id="f84cd-139">ID subnet.</span><span class="sxs-lookup"><span data-stu-id="f84cd-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f84cd-140">-SubnetName</span></span>
<span data-ttu-id="f84cd-141">Il nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="f84cd-141">The subnet name.</span></span> <span data-ttu-id="f84cd-142">Usato in combinazione con -VirtualNetworkName e deve essere nello stesso gruppo di risorse di ASE.</span><span class="sxs-lookup"><span data-stu-id="f84cd-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="f84cd-143">In caso contrario, usa -SubnetId</span><span class="sxs-lookup"><span data-stu-id="f84cd-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f84cd-144">-VirtualNetworkName</span></span>
<span data-ttu-id="f84cd-145">Il nome vNet.</span><span class="sxs-lookup"><span data-stu-id="f84cd-145">The vNet name.</span></span> <span data-ttu-id="f84cd-146">Usato in combinazione con -SubnetName e deve essere nello stesso gruppo di risorse di ASE.</span><span class="sxs-lookup"><span data-stu-id="f84cd-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="f84cd-147">In caso contrario, usa -SubnetId</span><span class="sxs-lookup"><span data-stu-id="f84cd-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84cd-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84cd-148">-Confirm</span></span>
<span data-ttu-id="f84cd-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f84cd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84cd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84cd-150">-WhatIf</span></span>
<span data-ttu-id="f84cd-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f84cd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84cd-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f84cd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84cd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84cd-153">CommonParameters</span></span>
<span data-ttu-id="f84cd-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84cd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84cd-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f84cd-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84cd-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="f84cd-156">INPUTS</span></span>

### <span data-ttu-id="f84cd-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f84cd-157">None</span></span>

## <span data-ttu-id="f84cd-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f84cd-158">OUTPUTS</span></span>

### <span data-ttu-id="f84cd-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="f84cd-159">System.Object</span></span>
## <span data-ttu-id="f84cd-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="f84cd-160">NOTES</span></span>

## <span data-ttu-id="f84cd-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f84cd-161">RELATED LINKS</span></span>

[<span data-ttu-id="f84cd-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="f84cd-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="f84cd-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="f84cd-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="f84cd-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="f84cd-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
