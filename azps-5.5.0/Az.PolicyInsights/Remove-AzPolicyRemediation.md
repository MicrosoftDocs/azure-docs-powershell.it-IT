---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206259"
---
# <span data-ttu-id="ac56c-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ac56c-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="ac56c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac56c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac56c-103">Elimina una correzione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ac56c-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="ac56c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac56c-104">SYNTAX</span></span>

### <span data-ttu-id="ac56c-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac56c-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac56c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac56c-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac56c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac56c-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac56c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac56c-108">DESCRIPTION</span></span>
<span data-ttu-id="ac56c-109">Il cmdlet **Remove-AzPolicyRemediation** elimina una correzione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ac56c-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="ac56c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac56c-110">EXAMPLES</span></span>

### <span data-ttu-id="ac56c-111">Esempio 1: Eliminare la correzione di un criterio nell'ambito del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ac56c-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="ac56c-112">Questo comando elimina la correzione denominata 'remediation1' nel gruppo di risorse 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="ac56c-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="ac56c-113">Esempio 2: Eliminare la correzione di un gruppo di gestione tramite piping</span><span class="sxs-lookup"><span data-stu-id="ac56c-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="ac56c-114">Questo comando elimina la correzione denominata 'remediation1' dal gruppo di gestione 'mg1'.</span><span class="sxs-lookup"><span data-stu-id="ac56c-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="ac56c-115">Prima di eliminare la risorsa verrà visualizzata una richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="ac56c-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="ac56c-116">Esempio 3: Annullare ed eliminare una correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="ac56c-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="ac56c-117">Questo comando elimina la correzione denominata 'remediation1' nel gruppo di risorse 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="ac56c-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="ac56c-118">Se la correzione è in corso, verrà annullata prima di essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="ac56c-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="ac56c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac56c-119">PARAMETERS</span></span>

### <span data-ttu-id="ac56c-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="ac56c-120">-AllowStop</span></span>
<span data-ttu-id="ac56c-121">Consentire l'annullamento della correzione se è in corso.</span><span class="sxs-lookup"><span data-stu-id="ac56c-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="ac56c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac56c-122">-AsJob</span></span>
<span data-ttu-id="ac56c-123">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="ac56c-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ac56c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac56c-124">-DefaultProfile</span></span>
<span data-ttu-id="ac56c-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac56c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac56c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac56c-126">-InputObject</span></span>
<span data-ttu-id="ac56c-127">Oggetto Remediation.</span><span class="sxs-lookup"><span data-stu-id="ac56c-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ac56c-128">-ManagementGroupName</span></span>
<span data-ttu-id="ac56c-129">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ac56c-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ac56c-130">-Name</span></span>
<span data-ttu-id="ac56c-131">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac56c-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac56c-132">-PassThru</span></span>
<span data-ttu-id="ac56c-133">Restituisce True se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ac56c-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="ac56c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac56c-134">-ResourceGroupName</span></span>
<span data-ttu-id="ac56c-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac56c-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac56c-136">-ResourceId</span></span>
<span data-ttu-id="ac56c-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac56c-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="ac56c-138">-Scope</span></span>
<span data-ttu-id="ac56c-139">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac56c-139">Scope of the resource.</span></span>
<span data-ttu-id="ac56c-140">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="ac56c-140">E.g.</span></span>
<span data-ttu-id="ac56c-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="ac56c-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac56c-142">-Confirm</span></span>
<span data-ttu-id="ac56c-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac56c-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac56c-144">-WhatIf</span></span>
<span data-ttu-id="ac56c-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac56c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac56c-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac56c-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac56c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac56c-147">CommonParameters</span></span>
<span data-ttu-id="ac56c-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac56c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac56c-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac56c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac56c-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac56c-150">INPUTS</span></span>

### <span data-ttu-id="ac56c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="ac56c-151">System.String</span></span>

### <span data-ttu-id="ac56c-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="ac56c-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="ac56c-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac56c-153">OUTPUTS</span></span>

### <span data-ttu-id="ac56c-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac56c-154">System.Boolean</span></span>

## <span data-ttu-id="ac56c-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac56c-155">NOTES</span></span>

## <span data-ttu-id="ac56c-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac56c-156">RELATED LINKS</span></span>
