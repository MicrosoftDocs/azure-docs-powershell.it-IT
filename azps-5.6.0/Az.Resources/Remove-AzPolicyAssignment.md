---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005806"
---
# <span data-ttu-id="3f0e2-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f0e2-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="3f0e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0e2-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="3f0e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f0e2-104">SYNTAX</span></span>

### <span data-ttu-id="3f0e2-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="3f0e2-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f0e2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f0e2-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f0e2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f0e2-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f0e2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f0e2-108">DESCRIPTION</span></span>
<span data-ttu-id="3f0e2-109">Il cmdlet **Remove-AzPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="3f0e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f0e2-110">EXAMPLES</span></span>

### <span data-ttu-id="3f0e2-111">Esempio 1: Rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="3f0e2-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="3f0e2-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3f0e2-113">Il comando archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3f0e2-114">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a un livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="3f0e2-115">La **proprietà ResourceId** dell'$ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3f0e2-116">Esempio 2: Rimuovere l'assegnazione dei criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3f0e2-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="3f0e2-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3f0e2-118">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e quindi la archivia nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3f0e2-119">La **proprietà ResourceId** dell'$ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="3f0e2-120">Il comando finale rimuove l'assegnazione dei criteri identificata dalla proprietà **ResourceId** $PolicyAssignment risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="3f0e2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f0e2-121">PARAMETERS</span></span>

### <span data-ttu-id="3f0e2-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3f0e2-122">-ApiVersion</span></span>
<span data-ttu-id="3f0e2-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3f0e2-124">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0e2-125">-DefaultProfile</span></span>
<span data-ttu-id="3f0e2-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3f0e2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f0e2-127">-Id</span><span class="sxs-lookup"><span data-stu-id="3f0e2-127">-Id</span></span>
<span data-ttu-id="3f0e2-128">Specifica l'ID risorsa completo per l'assegnazione dei criteri rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f0e2-129">-InputObject</span></span>
<span data-ttu-id="3f0e2-130">Oggetto di assegnazione dei criteri per rimuovere l'output da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3f0e2-131">-Name</span></span>
<span data-ttu-id="3f0e2-132">Specifica il nome dell'assegnazione di criteri rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="3f0e2-133">-Pre</span></span>
<span data-ttu-id="3f0e2-134">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3f0e2-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="3f0e2-135">-Scope</span></span>
<span data-ttu-id="3f0e2-136">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f0e2-137">-Confirm</span></span>
<span data-ttu-id="3f0e2-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f0e2-139">-WhatIf</span></span>
<span data-ttu-id="3f0e2-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f0e2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0e2-142">CommonParameters</span></span>
<span data-ttu-id="3f0e2-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0e2-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0e2-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f0e2-145">INPUTS</span></span>

### <span data-ttu-id="3f0e2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3f0e2-146">System.String</span></span>

## <span data-ttu-id="3f0e2-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f0e2-147">OUTPUTS</span></span>

### <span data-ttu-id="3f0e2-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f0e2-148">System.Boolean</span></span>

## <span data-ttu-id="3f0e2-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f0e2-149">NOTES</span></span>

## <span data-ttu-id="3f0e2-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f0e2-150">RELATED LINKS</span></span>

[<span data-ttu-id="3f0e2-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f0e2-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="3f0e2-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f0e2-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="3f0e2-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f0e2-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


