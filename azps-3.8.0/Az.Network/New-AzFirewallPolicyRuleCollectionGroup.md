---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019770"
---
# <span data-ttu-id="b7314-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="b7314-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="b7314-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7314-102">SYNOPSIS</span></span>
<span data-ttu-id="b7314-103">Creare un nuovo gruppo di raccolta regole criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="b7314-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="b7314-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7314-104">SYNTAX</span></span>

### <span data-ttu-id="b7314-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7314-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7314-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7314-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7314-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7314-107">DESCRIPTION</span></span>
<span data-ttu-id="b7314-108">Il cmdlet **New-AzFirewallPolicyRuleCollectionGroup** crea un gruppo di insiemi di regole in un criterio firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7314-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="b7314-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7314-109">EXAMPLES</span></span>

### <span data-ttu-id="b7314-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7314-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="b7314-111">Questo esempio crea un gruppo di insiemi di regole nel criterio firewall $fp</span><span class="sxs-lookup"><span data-stu-id="b7314-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="b7314-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7314-112">PARAMETERS</span></span>

### <span data-ttu-id="b7314-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7314-113">-DefaultProfile</span></span>
<span data-ttu-id="b7314-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7314-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7314-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="b7314-115">-FirewallPolicyName</span></span>
<span data-ttu-id="b7314-116">Nome del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="b7314-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="b7314-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b7314-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="b7314-118">Criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="b7314-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7314-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7314-119">-Name</span></span>
<span data-ttu-id="b7314-120">Nome del gruppo di regole</span><span class="sxs-lookup"><span data-stu-id="b7314-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="b7314-121">-Priorità</span><span class="sxs-lookup"><span data-stu-id="b7314-121">-Priority</span></span>
<span data-ttu-id="b7314-122">Priorità del gruppo di regole</span><span class="sxs-lookup"><span data-stu-id="b7314-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7314-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7314-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7314-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7314-124">The resource group name.</span></span>

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

### <span data-ttu-id="b7314-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="b7314-125">-RuleCollection</span></span>
<span data-ttu-id="b7314-126">Elenco di regole</span><span class="sxs-lookup"><span data-stu-id="b7314-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7314-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7314-127">-Confirm</span></span>
<span data-ttu-id="b7314-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7314-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7314-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7314-129">-WhatIf</span></span>
<span data-ttu-id="b7314-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7314-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7314-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7314-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7314-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7314-132">CommonParameters</span></span>
<span data-ttu-id="b7314-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7314-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7314-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7314-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7314-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7314-135">INPUTS</span></span>

### <span data-ttu-id="b7314-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7314-136">System.String</span></span>

### <span data-ttu-id="b7314-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b7314-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="b7314-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7314-138">OUTPUTS</span></span>

### <span data-ttu-id="b7314-139">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="b7314-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="b7314-140">Note</span><span class="sxs-lookup"><span data-stu-id="b7314-140">NOTES</span></span>

## <span data-ttu-id="b7314-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7314-141">RELATED LINKS</span></span>
