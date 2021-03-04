---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 0b50a6b7d7dd3b762f00b292e421f981dddd3740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969597"
---
# <span data-ttu-id="23f27-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="23f27-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="23f27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f27-102">SYNOPSIS</span></span>
<span data-ttu-id="23f27-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="23f27-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="23f27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23f27-104">SYNTAX</span></span>

### <span data-ttu-id="23f27-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23f27-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23f27-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="23f27-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f27-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="23f27-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23f27-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="23f27-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23f27-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="23f27-109">DESCRIPTION</span></span>
<span data-ttu-id="23f27-110">Il cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="23f27-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="23f27-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23f27-111">EXAMPLES</span></span>

### <span data-ttu-id="23f27-112">Esempio 1: Rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="23f27-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="23f27-113">Questo comando rimuove diverse IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="23f27-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="23f27-114">Esempio 2: Rimuovere un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="23f27-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="23f27-115">Questo comando rimuove un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="23f27-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="23f27-116">Esempio 3: Rimuovere la prima regola IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="23f27-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="23f27-117">Questo comando rimuove la prima regola IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="23f27-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="23f27-118">Esempio 4: Rimuovere più RegoleRelavoro VirtualNet con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="23f27-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="23f27-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="23f27-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="23f27-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23f27-120">PARAMETERS</span></span>

### <span data-ttu-id="23f27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f27-121">-DefaultProfile</span></span>
<span data-ttu-id="23f27-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23f27-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f27-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="23f27-123">-IpAddressOrRange</span></span>
<span data-ttu-id="23f27-124">Account dei servizi cognitivi NetworkRule IpRules IpAddressOrRange nella stringa.</span><span class="sxs-lookup"><span data-stu-id="23f27-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="23f27-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="23f27-125">-IpRule</span></span>
<span data-ttu-id="23f27-126">Account dei servizi cognitivi NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="23f27-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="23f27-127">-Name</span><span class="sxs-lookup"><span data-stu-id="23f27-127">-Name</span></span>
<span data-ttu-id="23f27-128">Nome account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="23f27-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="23f27-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f27-129">-ResourceGroupName</span></span>
<span data-ttu-id="23f27-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23f27-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="23f27-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="23f27-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="23f27-132">Account dei servizi cognitivi NetworkRule VirtualNetworkRules VirtualNetworkResourceId nella stringa.</span><span class="sxs-lookup"><span data-stu-id="23f27-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="23f27-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="23f27-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="23f27-134">Account di Servizi cognitivi NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="23f27-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="23f27-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23f27-135">-Confirm</span></span>
<span data-ttu-id="23f27-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f27-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f27-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f27-137">-WhatIf</span></span>
<span data-ttu-id="23f27-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f27-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f27-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f27-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f27-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f27-140">CommonParameters</span></span>
<span data-ttu-id="23f27-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f27-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f27-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23f27-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f27-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="23f27-143">INPUTS</span></span>

### <span data-ttu-id="23f27-144">System.String</span><span class="sxs-lookup"><span data-stu-id="23f27-144">System.String</span></span>

### <span data-ttu-id="23f27-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="23f27-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="23f27-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="23f27-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="23f27-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f27-147">OUTPUTS</span></span>

### <span data-ttu-id="23f27-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="23f27-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="23f27-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="23f27-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="23f27-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="23f27-150">NOTES</span></span>

## <span data-ttu-id="23f27-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23f27-151">RELATED LINKS</span></span>
