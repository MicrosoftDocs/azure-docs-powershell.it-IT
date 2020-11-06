---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 63b88096200c5db55f9c40a4ba839ffbf25c681d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514827"
---
# <span data-ttu-id="fc4a3-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fc4a3-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="fc4a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4a3-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc4a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc4a3-104">SYNTAX</span></span>

### <span data-ttu-id="fc4a3-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc4a3-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a3-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc4a3-107">DESCRIPTION</span></span>
<span data-ttu-id="fc4a3-108">Il cmdlet **Remove-AzureRmPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="fc4a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc4a3-109">EXAMPLES</span></span>

### <span data-ttu-id="fc4a3-110">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="fc4a3-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="fc4a3-111">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="fc4a3-112">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fc4a3-113">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="fc4a3-114">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="fc4a3-115">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="fc4a3-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="fc4a3-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fc4a3-117">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fc4a3-118">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="fc4a3-119">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="fc4a3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc4a3-120">PARAMETERS</span></span>

### <span data-ttu-id="fc4a3-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc4a3-121">-ApiVersion</span></span>
<span data-ttu-id="fc4a3-122">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc4a3-123">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fc4a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4a3-124">-DefaultProfile</span></span>
<span data-ttu-id="fc4a3-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fc4a3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc4a3-126">-ID</span><span class="sxs-lookup"><span data-stu-id="fc4a3-126">-Id</span></span>
<span data-ttu-id="fc4a3-127">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc4a3-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fc4a3-128">-InformationAction</span></span>
<span data-ttu-id="fc4a3-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="fc4a3-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc4a3-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc4a3-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="fc4a3-131">Continue</span></span>
- <span data-ttu-id="fc4a3-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="fc4a3-132">Ignore</span></span>
- <span data-ttu-id="fc4a3-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fc4a3-133">Inquire</span></span>
- <span data-ttu-id="fc4a3-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fc4a3-134">SilentlyContinue</span></span>
- <span data-ttu-id="fc4a3-135">Stop</span><span class="sxs-lookup"><span data-stu-id="fc4a3-135">Stop</span></span>
- <span data-ttu-id="fc4a3-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fc4a3-136">Suspend</span></span>

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

### <span data-ttu-id="fc4a3-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fc4a3-137">-InformationVariable</span></span>
<span data-ttu-id="fc4a3-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fc4a3-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc4a3-139">-Name</span></span>
<span data-ttu-id="fc4a3-140">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc4a3-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc4a3-141">-Pre</span></span>
<span data-ttu-id="fc4a3-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fc4a3-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="fc4a3-143">-Scope</span></span>
<span data-ttu-id="fc4a3-144">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="fc4a3-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc4a3-145">-Confirm</span></span>
<span data-ttu-id="fc4a3-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4a3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4a3-147">-WhatIf</span></span>
<span data-ttu-id="fc4a3-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4a3-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4a3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4a3-150">CommonParameters</span></span>
<span data-ttu-id="fc4a3-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4a3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4a3-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4a3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4a3-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc4a3-153">INPUTS</span></span>

## <span data-ttu-id="fc4a3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc4a3-154">OUTPUTS</span></span>

## <span data-ttu-id="fc4a3-155">Note</span><span class="sxs-lookup"><span data-stu-id="fc4a3-155">NOTES</span></span>

## <span data-ttu-id="fc4a3-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc4a3-156">RELATED LINKS</span></span>

[<span data-ttu-id="fc4a3-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fc4a3-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fc4a3-158">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fc4a3-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fc4a3-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fc4a3-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


