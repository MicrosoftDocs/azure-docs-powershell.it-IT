---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475702"
---
# <span data-ttu-id="1c30d-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1c30d-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="1c30d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c30d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c30d-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="1c30d-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="1c30d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c30d-104">SYNTAX</span></span>

### <span data-ttu-id="1c30d-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c30d-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c30d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c30d-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c30d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c30d-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c30d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c30d-108">DESCRIPTION</span></span>
<span data-ttu-id="1c30d-109">Il cmdlet **Remove-AzPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="1c30d-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="1c30d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c30d-110">EXAMPLES</span></span>

### <span data-ttu-id="1c30d-111">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="1c30d-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="1c30d-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1c30d-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1c30d-113">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1c30d-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1c30d-114">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c30d-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="1c30d-115">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c30d-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1c30d-116">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="1c30d-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="1c30d-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1c30d-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1c30d-118">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="1c30d-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1c30d-119">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c30d-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="1c30d-120">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="1c30d-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="1c30d-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c30d-121">PARAMETERS</span></span>

### <span data-ttu-id="1c30d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1c30d-122">-ApiVersion</span></span>
<span data-ttu-id="1c30d-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1c30d-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1c30d-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="1c30d-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1c30d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c30d-125">-DefaultProfile</span></span>
<span data-ttu-id="1c30d-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c30d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c30d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="1c30d-127">-Id</span></span>
<span data-ttu-id="1c30d-128">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c30d-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c30d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c30d-129">-InputObject</span></span>
<span data-ttu-id="1c30d-130">L'oggetto assegnazione dei criteri da rimuovere che è stato restituito da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c30d-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="1c30d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c30d-131">-Name</span></span>
<span data-ttu-id="1c30d-132">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c30d-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1c30d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="1c30d-133">-Pre</span></span>
<span data-ttu-id="1c30d-134">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1c30d-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1c30d-135">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1c30d-135">-Scope</span></span>
<span data-ttu-id="1c30d-136">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="1c30d-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="1c30d-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c30d-137">-Confirm</span></span>
<span data-ttu-id="1c30d-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c30d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c30d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c30d-139">-WhatIf</span></span>
<span data-ttu-id="1c30d-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c30d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c30d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c30d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c30d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c30d-142">CommonParameters</span></span>
<span data-ttu-id="1c30d-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c30d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c30d-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c30d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c30d-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c30d-145">INPUTS</span></span>

### <span data-ttu-id="1c30d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1c30d-146">System.String</span></span>

## <span data-ttu-id="1c30d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c30d-147">OUTPUTS</span></span>

### <span data-ttu-id="1c30d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c30d-148">System.Boolean</span></span>

## <span data-ttu-id="1c30d-149">Note</span><span class="sxs-lookup"><span data-stu-id="1c30d-149">NOTES</span></span>

## <span data-ttu-id="1c30d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c30d-150">RELATED LINKS</span></span>

[<span data-ttu-id="1c30d-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1c30d-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1c30d-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1c30d-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="1c30d-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1c30d-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


