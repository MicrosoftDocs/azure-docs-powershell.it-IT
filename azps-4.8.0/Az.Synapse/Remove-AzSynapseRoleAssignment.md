---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033596"
---
# <span data-ttu-id="eebd1-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="eebd1-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="eebd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eebd1-102">SYNOPSIS</span></span>
<span data-ttu-id="eebd1-103">Elimina un'assegnazione di ruolo di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="eebd1-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="eebd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eebd1-104">SYNTAX</span></span>

### <span data-ttu-id="eebd1-105">RemoveByWorkspaceNameAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eebd1-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebd1-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eebd1-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eebd1-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eebd1-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebd1-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eebd1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eebd1-115">DESCRIPTION</span></span>
<span data-ttu-id="eebd1-116">Il cmdlet **Remove-AzSynapseRoleAssignment** Elimina definitivamente un'assegnazione di ruolo di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="eebd1-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="eebd1-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eebd1-117">EXAMPLES</span></span>

### <span data-ttu-id="eebd1-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eebd1-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="eebd1-119">Questo comando Elimina un'assegnazione di ruolo di analisi di Azure sinapsi con un ID assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="eebd1-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="eebd1-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="eebd1-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="eebd1-121">Questo comando Elimina un'assegnazione di ruolo di analisi di Azure sinapsi con il nome di un ruolo e il nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="eebd1-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="eebd1-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="eebd1-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="eebd1-123">Questo comando Elimina un'assegnazione di ruolo di analisi di Azure sinapsi con un ID assegnazione di ruolo tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="eebd1-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="eebd1-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eebd1-124">PARAMETERS</span></span>

### <span data-ttu-id="eebd1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eebd1-125">-AsJob</span></span>
<span data-ttu-id="eebd1-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eebd1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eebd1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebd1-127">-DefaultProfile</span></span>
<span data-ttu-id="eebd1-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eebd1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eebd1-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="eebd1-129">-ObjectId</span></span>
<span data-ttu-id="eebd1-130">ID Azure AD ObjectId dell'utente, del gruppo o del servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="eebd1-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="eebd1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eebd1-131">-PassThru</span></span>
<span data-ttu-id="eebd1-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="eebd1-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="eebd1-133">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="eebd1-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eebd1-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="eebd1-134">-RoleAssignmentId</span></span>
<span data-ttu-id="eebd1-135">ID dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="eebd1-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="eebd1-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="eebd1-136">-RoleDefinitionId</span></span>
<span data-ttu-id="eebd1-137">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="eebd1-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="eebd1-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="eebd1-138">-RoleDefinitionName</span></span>
<span data-ttu-id="eebd1-139">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="eebd1-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="eebd1-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="eebd1-140">-ServicePrincipalName</span></span>
<span data-ttu-id="eebd1-141">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="eebd1-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="eebd1-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="eebd1-142">-SignInName</span></span>
<span data-ttu-id="eebd1-143">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eebd1-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="eebd1-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eebd1-144">-WorkspaceName</span></span>
<span data-ttu-id="eebd1-145">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="eebd1-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eebd1-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="eebd1-146">-WorkspaceObject</span></span>
<span data-ttu-id="eebd1-147">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="eebd1-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eebd1-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eebd1-148">-Confirm</span></span>
<span data-ttu-id="eebd1-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eebd1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebd1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebd1-150">-WhatIf</span></span>
<span data-ttu-id="eebd1-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eebd1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebd1-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eebd1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebd1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebd1-153">CommonParameters</span></span>
<span data-ttu-id="eebd1-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebd1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebd1-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eebd1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebd1-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eebd1-156">INPUTS</span></span>

### <span data-ttu-id="eebd1-157">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eebd1-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="eebd1-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eebd1-158">OUTPUTS</span></span>

### <span data-ttu-id="eebd1-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eebd1-159">System.Boolean</span></span>

## <span data-ttu-id="eebd1-160">Note</span><span class="sxs-lookup"><span data-stu-id="eebd1-160">NOTES</span></span>

## <span data-ttu-id="eebd1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eebd1-161">RELATED LINKS</span></span>
