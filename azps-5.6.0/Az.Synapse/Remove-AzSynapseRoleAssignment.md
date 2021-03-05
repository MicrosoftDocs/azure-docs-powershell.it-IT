---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 4fbc25b919b7fbb3caa972f4e64467dee1df7116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008238"
---
# <span data-ttu-id="0ffb4-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0ffb4-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="0ffb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ffb4-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffb4-103">Elimina un'assegnazione di ruolo di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="0ffb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ffb4-104">SYNTAX</span></span>

### <span data-ttu-id="0ffb4-105">RemoveByWorkspaceNameAndNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ffb4-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-113">RemoveByWorkspaceObjectAndRoleIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ffb4-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffb4-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ffb4-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ffb4-115">DESCRIPTION</span></span>
<span data-ttu-id="0ffb4-116">Il cmdlet **Remove-AzSynapseRoleAssignment** elimina definitivamente un'assegnazione di ruolo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="0ffb4-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ffb4-117">EXAMPLES</span></span>

### <span data-ttu-id="0ffb4-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ffb4-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="0ffb4-119">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un ID assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="0ffb4-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0ffb4-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="0ffb4-121">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un nome di ruolo e un nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="0ffb4-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0ffb4-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="0ffb4-123">Questo comando elimina un'assegnazione di ruolo di Azure Synapse Analytics con un ID assegnazione di ruolo tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="0ffb4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ffb4-124">PARAMETERS</span></span>

### <span data-ttu-id="0ffb4-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ffb4-125">-AsJob</span></span>
<span data-ttu-id="0ffb4-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0ffb4-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ffb4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb4-127">-DefaultProfile</span></span>
<span data-ttu-id="0ffb4-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ffb4-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ffb4-129">-ObjectId</span></span>
<span data-ttu-id="0ffb4-130">ObjectId di Azure AD dell'utente, del gruppo o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ffb4-131">-PassThru</span></span>
<span data-ttu-id="0ffb4-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0ffb4-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0ffb4-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="0ffb4-134">-RoleAssignmentId</span></span>
<span data-ttu-id="0ffb4-135">ID dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0ffb4-136">-RoleDefinitionId</span></span>
<span data-ttu-id="0ffb4-137">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ffb4-138">-RoleDefinitionName</span></span>
<span data-ttu-id="0ffb4-139">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0ffb4-140">-ServicePrincipalName</span></span>
<span data-ttu-id="0ffb4-141">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0ffb4-142">-SignInName</span></span>
<span data-ttu-id="0ffb4-143">Indirizzo di posta elettronica o nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0ffb4-144">-WorkspaceName</span></span>
<span data-ttu-id="0ffb4-145">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0ffb4-146">-WorkspaceObject</span></span>
<span data-ttu-id="0ffb4-147">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffb4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ffb4-148">-Confirm</span></span>
<span data-ttu-id="0ffb4-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ffb4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ffb4-150">-WhatIf</span></span>
<span data-ttu-id="0ffb4-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ffb4-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ffb4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffb4-153">CommonParameters</span></span>
<span data-ttu-id="0ffb4-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffb4-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ffb4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffb4-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ffb4-156">INPUTS</span></span>

### <span data-ttu-id="0ffb4-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ffb4-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0ffb4-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ffb4-158">OUTPUTS</span></span>

### <span data-ttu-id="0ffb4-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ffb4-159">System.Boolean</span></span>

## <span data-ttu-id="0ffb4-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ffb4-160">NOTES</span></span>

## <span data-ttu-id="0ffb4-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ffb4-161">RELATED LINKS</span></span>
