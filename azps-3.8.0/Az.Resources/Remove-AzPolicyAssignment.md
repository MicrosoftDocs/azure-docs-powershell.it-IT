---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8c7aa559ad6fde29c32f1958a4a0e2a6406ad42d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019719"
---
# <span data-ttu-id="8ab27-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ab27-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="8ab27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ab27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab27-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="8ab27-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="8ab27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ab27-104">SYNTAX</span></span>

### <span data-ttu-id="8ab27-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ab27-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab27-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab27-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ab27-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab27-108">Il cmdlet **Remove-AzPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="8ab27-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="8ab27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ab27-109">EXAMPLES</span></span>

### <span data-ttu-id="8ab27-110">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="8ab27-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="8ab27-111">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ab27-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8ab27-112">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ab27-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8ab27-113">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ab27-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="8ab27-114">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ab27-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="8ab27-115">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="8ab27-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="8ab27-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ab27-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8ab27-117">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ab27-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8ab27-118">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ab27-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="8ab27-119">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ab27-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="8ab27-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ab27-120">PARAMETERS</span></span>

### <span data-ttu-id="8ab27-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ab27-121">-ApiVersion</span></span>
<span data-ttu-id="8ab27-122">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="8ab27-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ab27-123">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="8ab27-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8ab27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab27-124">-DefaultProfile</span></span>
<span data-ttu-id="8ab27-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ab27-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ab27-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8ab27-126">-Id</span></span>
<span data-ttu-id="8ab27-127">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab27-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ab27-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ab27-128">-Name</span></span>
<span data-ttu-id="8ab27-129">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab27-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8ab27-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ab27-130">-Pre</span></span>
<span data-ttu-id="8ab27-131">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="8ab27-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8ab27-132">-Ambito</span><span class="sxs-lookup"><span data-stu-id="8ab27-132">-Scope</span></span>
<span data-ttu-id="8ab27-133">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="8ab27-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="8ab27-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ab27-134">-Confirm</span></span>
<span data-ttu-id="8ab27-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab27-136">-WhatIf</span></span>
<span data-ttu-id="8ab27-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ab27-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab27-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ab27-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab27-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab27-139">CommonParameters</span></span>
<span data-ttu-id="8ab27-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab27-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab27-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ab27-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab27-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ab27-142">INPUTS</span></span>

### <span data-ttu-id="8ab27-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8ab27-143">System.String</span></span>

## <span data-ttu-id="8ab27-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ab27-144">OUTPUTS</span></span>

### <span data-ttu-id="8ab27-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ab27-145">System.Boolean</span></span>

## <span data-ttu-id="8ab27-146">Note</span><span class="sxs-lookup"><span data-stu-id="8ab27-146">NOTES</span></span>

## <span data-ttu-id="8ab27-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ab27-147">RELATED LINKS</span></span>

[<span data-ttu-id="8ab27-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ab27-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="8ab27-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ab27-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="8ab27-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ab27-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


