---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8fbf6c16dce1f8d96dcc9546c801e389493e7bcd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862409"
---
# <span data-ttu-id="68394-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68394-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="68394-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68394-102">SYNOPSIS</span></span>
<span data-ttu-id="68394-103">Rimuove un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="68394-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="68394-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68394-104">SYNTAX</span></span>

### <span data-ttu-id="68394-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68394-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68394-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68394-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68394-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68394-107">DESCRIPTION</span></span>
<span data-ttu-id="68394-108">Il cmdlet **Remove-AzPolicyAssignment** rimuove l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="68394-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="68394-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68394-109">EXAMPLES</span></span>

### <span data-ttu-id="68394-110">Esempio 1: rimuovere l'assegnazione dei criteri per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="68394-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="68394-111">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68394-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="68394-112">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68394-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68394-113">Il secondo comando rimuove l'assegnazione di criteri denominata PolicyAssignment07 assegnata a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68394-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="68394-114">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68394-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="68394-115">Esempio 2: rimuovere l'assegnazione di criteri in base all'ID</span><span class="sxs-lookup"><span data-stu-id="68394-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="68394-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68394-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68394-117">Il secondo comando ottiene l'assegnazione dei criteri a livello di gruppo di risorse e lo archivia nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="68394-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="68394-118">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68394-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="68394-119">Il comando finale rimuove l'assegnazione dei criteri che identifica la proprietà **resourceId** di $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="68394-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="68394-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68394-120">PARAMETERS</span></span>

### <span data-ttu-id="68394-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68394-121">-ApiVersion</span></span>
<span data-ttu-id="68394-122">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="68394-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="68394-123">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="68394-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="68394-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68394-124">-DefaultProfile</span></span>
<span data-ttu-id="68394-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68394-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68394-126">-ID</span><span class="sxs-lookup"><span data-stu-id="68394-126">-Id</span></span>
<span data-ttu-id="68394-127">Specifica l'ID di risorsa completo per l'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68394-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68394-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="68394-128">-InformationAction</span></span>
<span data-ttu-id="68394-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="68394-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="68394-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="68394-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68394-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="68394-131">Continue</span></span>
- <span data-ttu-id="68394-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="68394-132">Ignore</span></span>
- <span data-ttu-id="68394-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="68394-133">Inquire</span></span>
- <span data-ttu-id="68394-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="68394-134">SilentlyContinue</span></span>
- <span data-ttu-id="68394-135">Stop</span><span class="sxs-lookup"><span data-stu-id="68394-135">Stop</span></span>
- <span data-ttu-id="68394-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="68394-136">Suspend</span></span>

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

### <span data-ttu-id="68394-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="68394-137">-InformationVariable</span></span>
<span data-ttu-id="68394-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="68394-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="68394-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="68394-139">-Name</span></span>
<span data-ttu-id="68394-140">Specifica il nome dell'assegnazione dei criteri rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68394-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68394-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="68394-141">-Pre</span></span>
<span data-ttu-id="68394-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="68394-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68394-143">-Ambito</span><span class="sxs-lookup"><span data-stu-id="68394-143">-Scope</span></span>
<span data-ttu-id="68394-144">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="68394-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="68394-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68394-145">-Confirm</span></span>
<span data-ttu-id="68394-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68394-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68394-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68394-147">-WhatIf</span></span>
<span data-ttu-id="68394-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68394-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68394-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68394-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68394-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68394-150">CommonParameters</span></span>
<span data-ttu-id="68394-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68394-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68394-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68394-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68394-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68394-153">INPUTS</span></span>

## <span data-ttu-id="68394-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68394-154">OUTPUTS</span></span>

## <span data-ttu-id="68394-155">Note</span><span class="sxs-lookup"><span data-stu-id="68394-155">NOTES</span></span>

## <span data-ttu-id="68394-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68394-156">RELATED LINKS</span></span>

[<span data-ttu-id="68394-157">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68394-157">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="68394-158">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68394-158">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="68394-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68394-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


