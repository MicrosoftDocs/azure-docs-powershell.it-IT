---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201847"
---
# <span data-ttu-id="b257e-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b257e-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="b257e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b257e-102">SYNOPSIS</span></span>
<span data-ttu-id="b257e-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b257e-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="b257e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b257e-104">SYNTAX</span></span>

### <span data-ttu-id="b257e-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b257e-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b257e-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b257e-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b257e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b257e-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b257e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b257e-108">DESCRIPTION</span></span>
<span data-ttu-id="b257e-109">Il cmdlet **Remove-AzPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="b257e-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="b257e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b257e-110">EXAMPLES</span></span>

### <span data-ttu-id="b257e-111">Esempio 1: Rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="b257e-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="b257e-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="b257e-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b257e-113">Il comando archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="b257e-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b257e-114">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a un livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b257e-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="b257e-115">La **proprietà ResourceId** dell'$ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b257e-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="b257e-116">Esempio 2: Rimuovere l'assegnazione dei criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b257e-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="b257e-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $ResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="b257e-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b257e-118">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e quindi la archivia nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="b257e-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b257e-119">La **proprietà ResourceId** dell'$ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b257e-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="b257e-120">Il comando finale rimuove l'assegnazione dei criteri identificata dalla proprietà **ResourceId** $PolicyAssignment risorsa.</span><span class="sxs-lookup"><span data-stu-id="b257e-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="b257e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b257e-121">PARAMETERS</span></span>

### <span data-ttu-id="b257e-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b257e-122">-ApiVersion</span></span>
<span data-ttu-id="b257e-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b257e-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b257e-124">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="b257e-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b257e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b257e-125">-DefaultProfile</span></span>
<span data-ttu-id="b257e-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b257e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b257e-127">-Id</span><span class="sxs-lookup"><span data-stu-id="b257e-127">-Id</span></span>
<span data-ttu-id="b257e-128">Specifica l'ID risorsa completo per l'assegnazione dei criteri rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b257e-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b257e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b257e-129">-InputObject</span></span>
<span data-ttu-id="b257e-130">Oggetto di assegnazione dei criteri per rimuovere l'output da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b257e-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="b257e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b257e-131">-Name</span></span>
<span data-ttu-id="b257e-132">Specifica il nome dell'assegnazione di criteri rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b257e-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b257e-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="b257e-133">-Pre</span></span>
<span data-ttu-id="b257e-134">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b257e-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b257e-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="b257e-135">-Scope</span></span>
<span data-ttu-id="b257e-136">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="b257e-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="b257e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b257e-137">-Confirm</span></span>
<span data-ttu-id="b257e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b257e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b257e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b257e-139">-WhatIf</span></span>
<span data-ttu-id="b257e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b257e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b257e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b257e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b257e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b257e-142">CommonParameters</span></span>
<span data-ttu-id="b257e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b257e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b257e-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b257e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b257e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="b257e-145">INPUTS</span></span>

### <span data-ttu-id="b257e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b257e-146">System.String</span></span>

## <span data-ttu-id="b257e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b257e-147">OUTPUTS</span></span>

### <span data-ttu-id="b257e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b257e-148">System.Boolean</span></span>

## <span data-ttu-id="b257e-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="b257e-149">NOTES</span></span>

## <span data-ttu-id="b257e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b257e-150">RELATED LINKS</span></span>

[<span data-ttu-id="b257e-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b257e-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b257e-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b257e-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="b257e-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b257e-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


