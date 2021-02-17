---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205019"
---
# <span data-ttu-id="7b17e-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7b17e-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="7b17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b17e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b17e-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="7b17e-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7b17e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b17e-104">SYNTAX</span></span>

### <span data-ttu-id="7b17e-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b17e-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b17e-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="7b17e-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b17e-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7b17e-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b17e-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="7b17e-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b17e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b17e-109">DESCRIPTION</span></span>
<span data-ttu-id="7b17e-110">Il cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="7b17e-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7b17e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b17e-111">EXAMPLES</span></span>

### <span data-ttu-id="7b17e-112">Esempio 1: Rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7b17e-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="7b17e-113">Questo comando rimuove diverse IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="7b17e-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="7b17e-114">Esempio 2: Rimuovere un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="7b17e-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="7b17e-115">Questo comando rimuove un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="7b17e-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="7b17e-116">Esempio 3: Rimuovere la prima regola IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="7b17e-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="7b17e-117">Questo comando rimuove la prima regola IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b17e-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="7b17e-118">Esempio 4: Rimuovere più RegoleRelavoro VirtualNet con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="7b17e-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="7b17e-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="7b17e-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="7b17e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b17e-120">PARAMETERS</span></span>

### <span data-ttu-id="7b17e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b17e-121">-DefaultProfile</span></span>
<span data-ttu-id="7b17e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b17e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b17e-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7b17e-123">-IpAddressOrRange</span></span>
<span data-ttu-id="7b17e-124">Account dei servizi cognitivi NetworkRule IpRules IpAddressOrRange nella stringa.</span><span class="sxs-lookup"><span data-stu-id="7b17e-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="7b17e-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="7b17e-125">-IpRule</span></span>
<span data-ttu-id="7b17e-126">Account di Servizi cognitivi NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="7b17e-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="7b17e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7b17e-127">-Name</span></span>
<span data-ttu-id="7b17e-128">Nome account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7b17e-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="7b17e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b17e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b17e-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b17e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b17e-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="7b17e-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="7b17e-132">Account dei servizi cognitivi NetworkRule VirtualNetworkRules VirtualNetworkResourceId nella stringa.</span><span class="sxs-lookup"><span data-stu-id="7b17e-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="7b17e-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7b17e-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="7b17e-134">Account di Servizi cognitivi NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="7b17e-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="7b17e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b17e-135">-Confirm</span></span>
<span data-ttu-id="7b17e-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b17e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b17e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b17e-137">-WhatIf</span></span>
<span data-ttu-id="7b17e-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b17e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b17e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b17e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b17e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b17e-140">CommonParameters</span></span>
<span data-ttu-id="7b17e-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b17e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b17e-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b17e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b17e-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b17e-143">INPUTS</span></span>

### <span data-ttu-id="7b17e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7b17e-144">System.String</span></span>

### <span data-ttu-id="7b17e-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="7b17e-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="7b17e-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="7b17e-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="7b17e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b17e-147">OUTPUTS</span></span>

### <span data-ttu-id="7b17e-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7b17e-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="7b17e-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="7b17e-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="7b17e-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b17e-150">NOTES</span></span>

## <span data-ttu-id="7b17e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b17e-151">RELATED LINKS</span></span>
