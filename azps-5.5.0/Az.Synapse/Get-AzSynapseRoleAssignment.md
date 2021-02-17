---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182790"
---
# <span data-ttu-id="1139c-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1139c-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="1139c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1139c-102">SYNOPSIS</span></span>
<span data-ttu-id="1139c-103">Ottiene un'assegnazione di ruolo di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1139c-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="1139c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1139c-104">SYNTAX</span></span>

### <span data-ttu-id="1139c-105">GetByWorkspaceNameAndNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1139c-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1139c-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1139c-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1139c-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1139c-115">DESCRIPTION</span></span>
<span data-ttu-id="1139c-116">Il cmdlet **Get-AzSynapseRoleAssignment** ottiene un'assegnazione di ruolo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1139c-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="1139c-117">Se non si specifica una definizione di ruolo o un nome dell'entità utente, questo cmdlet ottiene tutte le assegnazioni di ruolo.</span><span class="sxs-lookup"><span data-stu-id="1139c-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="1139c-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1139c-118">EXAMPLES</span></span>

### <span data-ttu-id="1139c-119">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1139c-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1139c-120">Questo comando recupera tutte le assegnazioni di ruolo in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1139c-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="1139c-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1139c-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="1139c-122">Questo comando recupera tutte le assegnazioni di ruolo nell'area di lavoro ContosoWorkspace con il nome di ruolo ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="1139c-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="1139c-123">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1139c-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="1139c-124">Questo comando ottiene un'assegnazione di ruolo nell'area di lavoro ContosoWorkspace con il nome di ruolo ContosoRole e il nome dell'entità utente ContosoName.</span><span class="sxs-lookup"><span data-stu-id="1139c-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="1139c-125">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1139c-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="1139c-126">Questo comando recupera tutte le assegnazioni di ruolo in un'area di lavoro tramite una pipeline.</span><span class="sxs-lookup"><span data-stu-id="1139c-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="1139c-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1139c-127">PARAMETERS</span></span>

### <span data-ttu-id="1139c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1139c-128">-DefaultProfile</span></span>
<span data-ttu-id="1139c-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1139c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1139c-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1139c-130">-ObjectId</span></span>
<span data-ttu-id="1139c-131">ObjectId di Azure AD dell'utente, del gruppo o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1139c-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="1139c-132">-RoleAssignmentId</span></span>
<span data-ttu-id="1139c-133">ID dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="1139c-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1139c-134">-RoleDefinitionId</span></span>
<span data-ttu-id="1139c-135">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="1139c-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1139c-136">-RoleDefinitionName</span></span>
<span data-ttu-id="1139c-137">Nome del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="1139c-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1139c-138">-ServicePrincipalName</span></span>
<span data-ttu-id="1139c-139">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="1139c-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="1139c-140">-SignInName</span></span>
<span data-ttu-id="1139c-141">Indirizzo di posta elettronica o nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1139c-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1139c-142">-WorkspaceName</span></span>
<span data-ttu-id="1139c-143">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1139c-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1139c-144">-WorkspaceObject</span></span>
<span data-ttu-id="1139c-145">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1139c-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1139c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1139c-146">CommonParameters</span></span>
<span data-ttu-id="1139c-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1139c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1139c-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1139c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1139c-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="1139c-149">INPUTS</span></span>

### <span data-ttu-id="1139c-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1139c-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1139c-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1139c-151">OUTPUTS</span></span>

### <span data-ttu-id="1139c-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="1139c-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="1139c-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="1139c-153">NOTES</span></span>

## <span data-ttu-id="1139c-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1139c-154">RELATED LINKS</span></span>
