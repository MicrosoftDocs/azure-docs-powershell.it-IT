---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018260"
---
# <span data-ttu-id="ec131-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec131-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="ec131-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec131-102">SYNOPSIS</span></span>
<span data-ttu-id="ec131-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="ec131-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ec131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec131-104">SYNTAX</span></span>

### <span data-ttu-id="ec131-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec131-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec131-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ec131-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec131-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ec131-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec131-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ec131-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec131-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec131-109">DESCRIPTION</span></span>
<span data-ttu-id="ec131-110">Il cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="ec131-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ec131-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec131-111">EXAMPLES</span></span>

### <span data-ttu-id="ec131-112">Esempio 1: rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ec131-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="ec131-113">Questo comando rimuove diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="ec131-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ec131-114">Esempio 2: rimuovere un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="ec131-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="ec131-115">Questo comando rimuove un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="ec131-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="ec131-116">Esempio 3: rimuovere First IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="ec131-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="ec131-117">Questo comando rimuove prima IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec131-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="ec131-118">Esempio 4: rimuovere più VirtualNetworkRules con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="ec131-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="ec131-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="ec131-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="ec131-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec131-120">PARAMETERS</span></span>

### <span data-ttu-id="ec131-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec131-121">-DefaultProfile</span></span>
<span data-ttu-id="ec131-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec131-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec131-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ec131-123">-IpAddressOrRange</span></span>
<span data-ttu-id="ec131-124">Account di servizi cognitivi NetworkRule IpRules IpAddressOrRange in stringa.</span><span class="sxs-lookup"><span data-stu-id="ec131-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="ec131-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ec131-125">-IpRule</span></span>
<span data-ttu-id="ec131-126">Account di servizi cognitivi NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="ec131-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="ec131-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec131-127">-Name</span></span>
<span data-ttu-id="ec131-128">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="ec131-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="ec131-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec131-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec131-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec131-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ec131-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ec131-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ec131-132">Account di servizi cognitivi NetworkRule VirtualNetworkRules VirtualNetworkResourceId in stringa.</span><span class="sxs-lookup"><span data-stu-id="ec131-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="ec131-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec131-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="ec131-134">Account di servizi cognitivi NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="ec131-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="ec131-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec131-135">-Confirm</span></span>
<span data-ttu-id="ec131-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec131-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec131-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec131-137">-WhatIf</span></span>
<span data-ttu-id="ec131-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec131-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec131-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec131-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec131-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec131-140">CommonParameters</span></span>
<span data-ttu-id="ec131-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec131-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec131-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec131-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec131-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec131-143">INPUTS</span></span>

### <span data-ttu-id="ec131-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ec131-144">System.String</span></span>

### <span data-ttu-id="ec131-145">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="ec131-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ec131-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ec131-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ec131-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec131-147">OUTPUTS</span></span>

### <span data-ttu-id="ec131-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec131-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ec131-149">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="ec131-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="ec131-150">Note</span><span class="sxs-lookup"><span data-stu-id="ec131-150">NOTES</span></span>

## <span data-ttu-id="ec131-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec131-151">RELATED LINKS</span></span>
