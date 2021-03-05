---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 50dd0f1b4f224b343d827ed3d07457d86352e96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993759"
---
# <span data-ttu-id="f633c-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="f633c-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="f633c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f633c-102">SYNOPSIS</span></span>
<span data-ttu-id="f633c-103">Rimuove un gruppo di regole per i criteri del firewall di Azure in un criterio del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="f633c-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="f633c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f633c-104">SYNTAX</span></span>

### <span data-ttu-id="f633c-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f633c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f633c-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f633c-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f633c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f633c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f633c-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f633c-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f633c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f633c-109">DESCRIPTION</span></span>
<span data-ttu-id="f633c-110">Il cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** rimuove un gruppo di raccolte regole da un criterio firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="f633c-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f633c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f633c-111">EXAMPLES</span></span>

### <span data-ttu-id="f633c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f633c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="f633c-113">Questo esempio rimuove il gruppo di regole dei criteri del firewall denominato "testRcGroup" nell'oggetto criterio firewall $fp</span><span class="sxs-lookup"><span data-stu-id="f633c-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="f633c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f633c-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="f633c-115">Questo esempio rimuove il gruppo di regole dei criteri del firewall denominato "testRcGroup" nel firewall denominato "fpName" frpm i nomi dei gruppi di risorse "testRg"</span><span class="sxs-lookup"><span data-stu-id="f633c-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="f633c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f633c-116">PARAMETERS</span></span>

### <span data-ttu-id="f633c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f633c-117">-AsJob</span></span>
<span data-ttu-id="f633c-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f633c-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f633c-119">-DefaultProfile</span></span>
<span data-ttu-id="f633c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f633c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="f633c-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="f633c-122">Nome del criterio del firewall</span><span class="sxs-lookup"><span data-stu-id="f633c-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f633c-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="f633c-124">Criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="f633c-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f633c-125">-Force</span></span>
<span data-ttu-id="f633c-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f633c-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f633c-127">-InputObject</span></span>
<span data-ttu-id="f633c-128">Oggetto gruppo della raccolta di regole dei criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="f633c-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f633c-129">-Name</span></span>
<span data-ttu-id="f633c-130">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f633c-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f633c-131">-PassThru</span></span>
<span data-ttu-id="f633c-132">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f633c-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f633c-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f633c-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f633c-134">-ResourceGroupName</span></span>
<span data-ttu-id="f633c-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f633c-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f633c-136">-ResourceId</span></span>
<span data-ttu-id="f633c-137">ID risorsa del gruppo di raccolte regole</span><span class="sxs-lookup"><span data-stu-id="f633c-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f633c-138">-Confirm</span></span>
<span data-ttu-id="f633c-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f633c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f633c-140">-WhatIf</span></span>
<span data-ttu-id="f633c-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f633c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f633c-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f633c-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f633c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f633c-143">CommonParameters</span></span>
<span data-ttu-id="f633c-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f633c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f633c-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f633c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f633c-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="f633c-146">INPUTS</span></span>

### <span data-ttu-id="f633c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f633c-147">System.String</span></span>

### <span data-ttu-id="f633c-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f633c-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="f633c-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="f633c-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="f633c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f633c-150">OUTPUTS</span></span>

### <span data-ttu-id="f633c-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f633c-151">System.Boolean</span></span>

## <span data-ttu-id="f633c-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="f633c-152">NOTES</span></span>

## <span data-ttu-id="f633c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f633c-153">RELATED LINKS</span></span>
