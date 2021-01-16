---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363523"
---
# <span data-ttu-id="cd96f-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="cd96f-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="cd96f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd96f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd96f-103">Rimuove un gruppo di insiemi di regole dei criteri di Azure firewall in un criterio firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="cd96f-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="cd96f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd96f-104">SYNTAX</span></span>

### <span data-ttu-id="cd96f-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd96f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd96f-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd96f-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd96f-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd96f-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd96f-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd96f-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd96f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd96f-109">DESCRIPTION</span></span>
<span data-ttu-id="cd96f-110">Il cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** rimuove un gruppo di insiemi di regole da un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="cd96f-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="cd96f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd96f-111">EXAMPLES</span></span>

### <span data-ttu-id="cd96f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd96f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="cd96f-113">In questo esempio viene rimosso il gruppo di regole dei criteri Colelction denominato "testRcGroup" nell'oggetto criteri firewall $fp</span><span class="sxs-lookup"><span data-stu-id="cd96f-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="cd96f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cd96f-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="cd96f-115">In questo esempio viene rimosso il gruppo Colelction Rule Policy del firewall denominato "testRcGroup" nel firewall denominato "fpName" frpm i nomi ResourceGroup "testRg"</span><span class="sxs-lookup"><span data-stu-id="cd96f-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="cd96f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd96f-116">PARAMETERS</span></span>

### <span data-ttu-id="cd96f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd96f-117">-AsJob</span></span>
<span data-ttu-id="cd96f-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd96f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd96f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd96f-119">-DefaultProfile</span></span>
<span data-ttu-id="cd96f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd96f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd96f-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="cd96f-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="cd96f-122">Nome del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="cd96f-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="cd96f-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cd96f-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="cd96f-124">Criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="cd96f-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="cd96f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cd96f-125">-Force</span></span>
<span data-ttu-id="cd96f-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cd96f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cd96f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd96f-127">-InputObject</span></span>
<span data-ttu-id="cd96f-128">Oggetto gruppo raccolta regole criteri firewall</span><span class="sxs-lookup"><span data-stu-id="cd96f-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="cd96f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd96f-129">-Name</span></span>
<span data-ttu-id="cd96f-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd96f-130">The resource name.</span></span>

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

### <span data-ttu-id="cd96f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd96f-131">-PassThru</span></span>
<span data-ttu-id="cd96f-132">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cd96f-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd96f-133">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cd96f-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd96f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd96f-134">-ResourceGroupName</span></span>
<span data-ttu-id="cd96f-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd96f-135">The resource group name.</span></span>

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

### <span data-ttu-id="cd96f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd96f-136">-ResourceId</span></span>
<span data-ttu-id="cd96f-137">ID risorsa del gruppo raccolta regole</span><span class="sxs-lookup"><span data-stu-id="cd96f-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="cd96f-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd96f-138">-Confirm</span></span>
<span data-ttu-id="cd96f-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd96f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd96f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd96f-140">-WhatIf</span></span>
<span data-ttu-id="cd96f-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd96f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd96f-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd96f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd96f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd96f-143">CommonParameters</span></span>
<span data-ttu-id="cd96f-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd96f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd96f-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd96f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd96f-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd96f-146">INPUTS</span></span>

### <span data-ttu-id="cd96f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="cd96f-147">System.String</span></span>

### <span data-ttu-id="cd96f-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cd96f-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="cd96f-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="cd96f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="cd96f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd96f-150">OUTPUTS</span></span>

### <span data-ttu-id="cd96f-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd96f-151">System.Boolean</span></span>

## <span data-ttu-id="cd96f-152">Note</span><span class="sxs-lookup"><span data-stu-id="cd96f-152">NOTES</span></span>

## <span data-ttu-id="cd96f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd96f-153">RELATED LINKS</span></span>
