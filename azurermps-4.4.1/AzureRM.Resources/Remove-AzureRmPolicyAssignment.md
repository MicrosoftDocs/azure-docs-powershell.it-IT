---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687704"
---
# <span data-ttu-id="ba383-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ba383-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="ba383-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba383-102">SYNOPSIS</span></span>
<span data-ttu-id="ba383-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="ba383-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba383-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba383-104">SYNTAX</span></span>

### <span data-ttu-id="ba383-105">Set di parametri nome assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="ba383-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="ba383-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="ba383-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba383-107">Set di parametri ID assegnazione criteri.</span><span class="sxs-lookup"><span data-stu-id="ba383-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba383-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba383-108">DESCRIPTION</span></span>
<span data-ttu-id="ba383-109">Il cmdlet **Remove-AzureRmPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="ba383-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="ba383-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba383-110">EXAMPLES</span></span>

### <span data-ttu-id="ba383-111">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="ba383-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="ba383-112">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba383-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="ba383-113">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba383-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ba383-114">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba383-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="ba383-115">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba383-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ba383-116">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="ba383-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="ba383-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba383-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="ba383-118">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="ba383-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ba383-119">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba383-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="ba383-120">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="ba383-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="ba383-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba383-121">PARAMETERS</span></span>

### <span data-ttu-id="ba383-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ba383-122">-ApiVersion</span></span>
<span data-ttu-id="ba383-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ba383-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ba383-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="ba383-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ba383-125">-ID</span><span class="sxs-lookup"><span data-stu-id="ba383-125">-Id</span></span>
<span data-ttu-id="ba383-126">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba383-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ba383-127">-InformationAction</span></span>
<span data-ttu-id="ba383-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ba383-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba383-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba383-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba383-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="ba383-130">Continue</span></span>
- <span data-ttu-id="ba383-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="ba383-131">Ignore</span></span>
- <span data-ttu-id="ba383-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ba383-132">Inquire</span></span>
- <span data-ttu-id="ba383-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba383-133">SilentlyContinue</span></span>
- <span data-ttu-id="ba383-134">Stop</span><span class="sxs-lookup"><span data-stu-id="ba383-134">Stop</span></span>
- <span data-ttu-id="ba383-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ba383-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba383-136">-InformationVariable</span></span>
<span data-ttu-id="ba383-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ba383-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba383-138">-Name</span></span>
<span data-ttu-id="ba383-139">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba383-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="ba383-140">-Pre</span></span>
<span data-ttu-id="ba383-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ba383-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ba383-142">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ba383-142">-Scope</span></span>
<span data-ttu-id="ba383-143">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="ba383-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba383-144">-Confirm</span></span>
<span data-ttu-id="ba383-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba383-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba383-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba383-146">-WhatIf</span></span>
<span data-ttu-id="ba383-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba383-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba383-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba383-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba383-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba383-149">-DefaultProfile</span></span>
<span data-ttu-id="ba383-150">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba383-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba383-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba383-151">CommonParameters</span></span>
<span data-ttu-id="ba383-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba383-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba383-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba383-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba383-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba383-154">INPUTS</span></span>

## <span data-ttu-id="ba383-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba383-155">OUTPUTS</span></span>

### <span data-ttu-id="ba383-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba383-156">System.Boolean</span></span>

## <span data-ttu-id="ba383-157">Note</span><span class="sxs-lookup"><span data-stu-id="ba383-157">NOTES</span></span>

## <span data-ttu-id="ba383-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba383-158">RELATED LINKS</span></span>

[<span data-ttu-id="ba383-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ba383-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ba383-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ba383-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="ba383-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ba383-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


