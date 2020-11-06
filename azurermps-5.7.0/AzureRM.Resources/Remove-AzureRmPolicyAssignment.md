---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514119"
---
# <span data-ttu-id="b5b4b-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5b4b-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b5b4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b4b-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5b4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b4b-104">SYNTAX</span></span>

### <span data-ttu-id="b5b4b-105">RemoveByPolicyAssignmentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5b4b-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b4b-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="b5b4b-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b4b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5b4b-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b4b-108">Il cmdlet **Remove-AzureRmPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="b5b4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b4b-109">EXAMPLES</span></span>

### <span data-ttu-id="b5b4b-110">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="b5b4b-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="b5b4b-111">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b5b4b-112">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="b5b4b-113">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="b5b4b-114">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="b5b4b-115">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b5b4b-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="b5b4b-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="b5b4b-117">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b5b4b-118">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="b5b4b-119">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="b5b4b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5b4b-120">PARAMETERS</span></span>

### <span data-ttu-id="b5b4b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5b4b-121">-ApiVersion</span></span>
<span data-ttu-id="b5b4b-122">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b5b4b-123">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b4b-124">-DefaultProfile</span></span>
<span data-ttu-id="b5b4b-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5b4b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b5b4b-126">-Id</span></span>
<span data-ttu-id="b5b4b-127">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5b4b-128">-InformationAction</span></span>
<span data-ttu-id="b5b4b-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5b4b-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5b4b-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5b4b-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="b5b4b-131">Continue</span></span>
- <span data-ttu-id="b5b4b-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="b5b4b-132">Ignore</span></span>
- <span data-ttu-id="b5b4b-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b5b4b-133">Inquire</span></span>
- <span data-ttu-id="b5b4b-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5b4b-134">SilentlyContinue</span></span>
- <span data-ttu-id="b5b4b-135">Stop</span><span class="sxs-lookup"><span data-stu-id="b5b4b-135">Stop</span></span>
- <span data-ttu-id="b5b4b-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b5b4b-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5b4b-137">-InformationVariable</span></span>
<span data-ttu-id="b5b4b-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5b4b-139">-Name</span></span>
<span data-ttu-id="b5b4b-140">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="b5b4b-141">-Pre</span></span>
<span data-ttu-id="b5b4b-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b5b4b-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b5b4b-143">-Scope</span></span>
<span data-ttu-id="b5b4b-144">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5b4b-145">-Confirm</span></span>
<span data-ttu-id="b5b4b-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b4b-147">-WhatIf</span></span>
<span data-ttu-id="b5b4b-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b4b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b4b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b4b-150">CommonParameters</span></span>
<span data-ttu-id="b5b4b-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b4b-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b4b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b4b-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5b4b-153">INPUTS</span></span>

### <span data-ttu-id="b5b4b-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b5b4b-154">None</span></span>
<span data-ttu-id="b5b4b-155">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b5b4b-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5b4b-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b4b-156">OUTPUTS</span></span>

### <span data-ttu-id="b5b4b-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5b4b-157">System.Boolean</span></span>

## <span data-ttu-id="b5b4b-158">Note</span><span class="sxs-lookup"><span data-stu-id="b5b4b-158">NOTES</span></span>

## <span data-ttu-id="b5b4b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b4b-159">RELATED LINKS</span></span>

[<span data-ttu-id="b5b4b-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5b4b-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b5b4b-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5b4b-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b5b4b-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5b4b-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


