---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177806"
---
# <span data-ttu-id="ed646-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed646-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="ed646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed646-102">SYNOPSIS</span></span>
<span data-ttu-id="ed646-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="ed646-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ed646-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed646-104">SYNTAX</span></span>

### <span data-ttu-id="ed646-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed646-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed646-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed646-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed646-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed646-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed646-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ed646-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed646-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed646-109">DESCRIPTION</span></span>
<span data-ttu-id="ed646-110">Il cmdlet **Add-AzCognitiveServicesAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="ed646-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ed646-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed646-111">EXAMPLES</span></span>

### <span data-ttu-id="ed646-112">Esempio 1: Aggiungere più IpRules con IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ed646-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="ed646-113">Questo comando aggiunge più IpRules con IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="ed646-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="ed646-114">Esempio 2: Aggiungere una regola VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="ed646-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="ed646-115">Questo comando aggiunge virtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="ed646-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="ed646-116">Esempio 3: Aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="ed646-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="ed646-117">Questo comando aggiunge VirtualNetworkRules con gli oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="ed646-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="ed646-118">Esempio 4: Aggiungere più oggetti IpRule con IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="ed646-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="ed646-119">Questo comando aggiunge diversi oggetti IpRule con oggetti IpRule, input con JSON.</span><span class="sxs-lookup"><span data-stu-id="ed646-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="ed646-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed646-120">PARAMETERS</span></span>

### <span data-ttu-id="ed646-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed646-121">-DefaultProfile</span></span>
<span data-ttu-id="ed646-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed646-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed646-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ed646-123">-IpAddressOrRange</span></span>
<span data-ttu-id="ed646-124">Account dei servizi cognitivi NetworkRule IpRules IpAddressOrRange nella stringa.</span><span class="sxs-lookup"><span data-stu-id="ed646-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ed646-125">-IpRule</span></span>
<span data-ttu-id="ed646-126">Account di Servizi cognitivi NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="ed646-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ed646-127">-Name</span></span>
<span data-ttu-id="ed646-128">Nome account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="ed646-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed646-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed646-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed646-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ed646-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ed646-132">Account dei servizi cognitivi NetworkRule VirtualNetworkRules VirtualNetworkResourceId nella stringa.</span><span class="sxs-lookup"><span data-stu-id="ed646-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed646-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="ed646-134">Account di Servizi cognitivi NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="ed646-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed646-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed646-135">-Confirm</span></span>
<span data-ttu-id="ed646-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed646-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed646-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed646-137">-WhatIf</span></span>
<span data-ttu-id="ed646-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed646-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed646-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed646-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed646-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed646-140">CommonParameters</span></span>
<span data-ttu-id="ed646-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed646-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed646-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed646-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed646-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed646-143">INPUTS</span></span>

### <span data-ttu-id="ed646-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ed646-144">System.String</span></span>

### <span data-ttu-id="ed646-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="ed646-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ed646-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="ed646-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ed646-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed646-147">OUTPUTS</span></span>

### <span data-ttu-id="ed646-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed646-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ed646-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="ed646-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="ed646-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed646-150">NOTES</span></span>

## <span data-ttu-id="ed646-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed646-151">RELATED LINKS</span></span>
