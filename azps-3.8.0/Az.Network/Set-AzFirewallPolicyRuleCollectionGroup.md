---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020467"
---
# <span data-ttu-id="d5d26-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d5d26-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d5d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5d26-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d26-103">Salva un gruppo di raccolta regole criteri di Azure firewall modificato</span><span class="sxs-lookup"><span data-stu-id="d5d26-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="d5d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5d26-104">SYNTAX</span></span>

### <span data-ttu-id="d5d26-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d26-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d26-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d26-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d26-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d26-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d26-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d26-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d26-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d26-109">DESCRIPTION</span></span>
<span data-ttu-id="d5d26-110">Il cmdlet **set-AzFirewallPolicyRuleCollectionGroup** aggiorna i gruppi di insiemi di regole in un criterio firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d26-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d5d26-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5d26-111">EXAMPLES</span></span>

### <span data-ttu-id="d5d26-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5d26-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="d5d26-113">Questo esempio aggiorna un gruppo di insiemi di regole nel criterio firewall $fp</span><span class="sxs-lookup"><span data-stu-id="d5d26-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="d5d26-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5d26-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d26-115">-DefaultProfile</span></span>
<span data-ttu-id="d5d26-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d26-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="d5d26-117">-FirewallPolicyName</span></span>
<span data-ttu-id="d5d26-118">Nome del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="d5d26-118">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d5d26-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="d5d26-120">Criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="d5d26-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d26-121">-InputObject</span></span>
<span data-ttu-id="d5d26-122">Elenco di regole</span><span class="sxs-lookup"><span data-stu-id="d5d26-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5d26-123">-Name</span></span>
<span data-ttu-id="d5d26-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d5d26-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-125">-Priorità</span><span class="sxs-lookup"><span data-stu-id="d5d26-125">-Priority</span></span>
<span data-ttu-id="d5d26-126">Priorità del gruppo di regole</span><span class="sxs-lookup"><span data-stu-id="d5d26-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d26-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5d26-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5d26-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d26-129">-ResourceId</span></span>
<span data-ttu-id="d5d26-130">ID risorsa del gruppo raccolta regole</span><span class="sxs-lookup"><span data-stu-id="d5d26-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="d5d26-131">-RuleCollection</span></span>
<span data-ttu-id="d5d26-132">Elenco delle raccolte di regole</span><span class="sxs-lookup"><span data-stu-id="d5d26-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d26-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5d26-133">-Confirm</span></span>
<span data-ttu-id="d5d26-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d26-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d26-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d26-135">-WhatIf</span></span>
<span data-ttu-id="d5d26-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5d26-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d26-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5d26-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d26-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d26-138">CommonParameters</span></span>
<span data-ttu-id="d5d26-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d26-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d26-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5d26-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d26-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5d26-141">INPUTS</span></span>

### <span data-ttu-id="d5d26-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d26-142">System.String</span></span>

### <span data-ttu-id="d5d26-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d26-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="d5d26-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5d26-144">OUTPUTS</span></span>

### <span data-ttu-id="d5d26-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d5d26-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d5d26-146">Note</span><span class="sxs-lookup"><span data-stu-id="d5d26-146">NOTES</span></span>

## <span data-ttu-id="d5d26-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5d26-147">RELATED LINKS</span></span>
