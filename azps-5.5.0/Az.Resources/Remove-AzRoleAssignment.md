---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208402"
---
# <span data-ttu-id="53b16-101">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="53b16-101">Remove-AzRoleAssignment</span></span>

## <span data-ttu-id="53b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b16-102">SYNOPSIS</span></span>
<span data-ttu-id="53b16-103">Rimuove un'assegnazione di ruolo all'entità specificata assegnata a un particolare ruolo in un particolare ambito.</span><span class="sxs-lookup"><span data-stu-id="53b16-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="53b16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53b16-104">SYNTAX</span></span>

### <span data-ttu-id="53b16-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53b16-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b16-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b16-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53b16-117">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53b16-117">DESCRIPTION</span></span>
<span data-ttu-id="53b16-118">Usare il Remove-AzRoleAssignment per revocare l'accesso a un'entità in base all'ambito e al ruolo assegnato.</span><span class="sxs-lookup"><span data-stu-id="53b16-118">Use the Remove-AzRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>
<span data-ttu-id="53b16-119">Oggetto dell'assegnazione, ad esempio l'entità DEVE essere specificata.</span><span class="sxs-lookup"><span data-stu-id="53b16-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="53b16-120">L'entità può essere un utente (usare i parametri SignInName o ObjectId per identificare un utente), un gruppo di sicurezza (usare il parametro ObjectId per identificare un gruppo) o un'entità servizio (usare i parametri ServicePrincipalName o ObjectId per identificare un ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="53b16-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>
<span data-ttu-id="53b16-121">Il ruolo a cui è assegnata l'entità DEVE essere specificato usando il parametro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="53b16-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="53b16-122">L'ambito dell'assegnazione MAY può essere specificato e, se non specificato, viene utilizzato per impostazione predefinita l'ambito di sottoscrizione, ad esempio se si tenta di eliminare un'assegnazione all'entità e al ruolo specificati nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53b16-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="53b16-123">L'ambito dell'assegnazione può essere specificato usando uno dei parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="53b16-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="53b16-124">a.</span><span class="sxs-lookup"><span data-stu-id="53b16-124">a.</span></span>
<span data-ttu-id="53b16-125">Ambito: ambito completo che inizia con \<subscriptionId\> /subscriptions/b.</span><span class="sxs-lookup"><span data-stu-id="53b16-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="53b16-126">ResourceGroupName: nome di qualsiasi gruppo di risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53b16-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="53b16-127">c.</span><span class="sxs-lookup"><span data-stu-id="53b16-127">c.</span></span>
<span data-ttu-id="53b16-128">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource: identifica una particolare risorsa nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53b16-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="53b16-129">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53b16-129">EXAMPLES</span></span>

### <span data-ttu-id="53b16-130">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53b16-130">Example 1</span></span>
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="53b16-131">Rimuove un'assegnazione di ruolo john.doe@contoso.com per gli utenti assegnati al ruolo lettore nell'ambito del gruppo di risorse rg1.</span><span class="sxs-lookup"><span data-stu-id="53b16-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="53b16-132">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53b16-132">Example 2</span></span>
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="53b16-133">Rimuove l'assegnazione di ruolo all'entità gruppo identificata da ObjectId e assegnata al ruolo lettore.</span><span class="sxs-lookup"><span data-stu-id="53b16-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="53b16-134">Per impostazione predefinita, viene utilizzata la sottoscrizione corrente come ambito per trovare l'assegnazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="53b16-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="53b16-135">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="53b16-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="53b16-136">Rimuove il primo oggetto assegnazione di ruolo recuperato dal Get-AzRoleAssignment let.</span><span class="sxs-lookup"><span data-stu-id="53b16-136">Removes the first role assignment object which is fetched from the Get-AzRoleAssignment commandlet.</span></span>

## <span data-ttu-id="53b16-137">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53b16-137">PARAMETERS</span></span>

### <span data-ttu-id="53b16-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b16-138">-DefaultProfile</span></span>
<span data-ttu-id="53b16-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="53b16-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53b16-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53b16-140">-InputObject</span></span>
<span data-ttu-id="53b16-141">Oggetto Assegnazione ruolo.</span><span class="sxs-lookup"><span data-stu-id="53b16-141">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="53b16-142">-ObjectId</span></span>
<span data-ttu-id="53b16-143">ObjectId di Azure AD dell'utente, del gruppo o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="53b16-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="53b16-144">-ParentResource</span></span>
<span data-ttu-id="53b16-145">La risorsa padre nella gerarchia (della risorsa specificata con il parametro ResourceName), se presente.</span><span class="sxs-lookup"><span data-stu-id="53b16-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="53b16-146">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e ResourceName per creare un ambito gerarchico in forma di URI relativo che identifichi la risorsa.</span><span class="sxs-lookup"><span data-stu-id="53b16-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53b16-147">-PassThru</span></span>
<span data-ttu-id="53b16-148">Se specificato, visualizza l'assegnazione di ruolo eliminata</span><span class="sxs-lookup"><span data-stu-id="53b16-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="53b16-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53b16-149">-ResourceGroupName</span></span>
<span data-ttu-id="53b16-150">Nome del gruppo di risorse a cui è assegnato il ruolo.</span><span class="sxs-lookup"><span data-stu-id="53b16-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="53b16-151">Cerca di eliminare un'assegnazione nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="53b16-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="53b16-152">Se usato insieme ai parametri ResourceName, ResourceType e (facoltativamente) ParentResource, il comando crea un ambito gerarchico sotto forma di URI relativo che identifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="53b16-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="53b16-153">-ResourceName</span></span>
<span data-ttu-id="53b16-154">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="53b16-154">The resource name.</span></span>
<span data-ttu-id="53b16-155">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="53b16-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="53b16-156">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e (facoltativamente) ParentResource per creare un ambito gerarchico in forma di URI relativo che identifichi la risorsa ed elimini un'assegnazione in tale ambito.</span><span class="sxs-lookup"><span data-stu-id="53b16-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="53b16-157">-ResourceType</span></span>
<span data-ttu-id="53b16-158">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="53b16-158">The resource type.</span></span>
<span data-ttu-id="53b16-159">Ad esempio, Microsoft.Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="53b16-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="53b16-160">Deve essere usato insieme ai parametri ResourceGroupName, ResourceName e (facoltativamente) ParentResource per creare un ambito gerarchico sotto forma di URI relativo che identifichi la risorsa ed elimini un'assegnazione in tale ambito.</span><span class="sxs-lookup"><span data-stu-id="53b16-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="53b16-161">-RoleDefinitionId</span></span>
<span data-ttu-id="53b16-162">ID del ruolo RBAC per cui è necessario eliminare l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="53b16-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="53b16-163">-RoleDefinitionName</span></span>
<span data-ttu-id="53b16-164">Nome del ruolo RBAC per cui è necessario eliminare l'assegnazione, ad esempio Lettore, Collaboratore, Amministratore rete virtuale e così via.</span><span class="sxs-lookup"><span data-stu-id="53b16-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="53b16-165">-Scope</span></span>
<span data-ttu-id="53b16-166">Ambito dell'assegnazione di ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="53b16-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="53b16-167">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="53b16-167">In the format of relative URI.</span></span>
<span data-ttu-id="53b16-168">Ad esempio, "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="53b16-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="53b16-169">Se non è specificato, tenterà di eliminare il ruolo a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="53b16-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="53b16-170">Se specificato, dovrebbe iniziare con "/subscriptions/{id}".</span><span class="sxs-lookup"><span data-stu-id="53b16-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="53b16-171">-ServicePrincipalName</span></span>
<span data-ttu-id="53b16-172">ServicePrincipalName dell'applicazione Azure AD</span><span class="sxs-lookup"><span data-stu-id="53b16-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="53b16-173">-SignInName</span></span>
<span data-ttu-id="53b16-174">Indirizzo di posta elettronica o nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="53b16-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53b16-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53b16-175">-Confirm</span></span>
<span data-ttu-id="53b16-176">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53b16-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b16-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b16-177">-WhatIf</span></span>
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

### <span data-ttu-id="53b16-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b16-178">CommonParameters</span></span>
<span data-ttu-id="53b16-179">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b16-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b16-180">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53b16-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b16-181">INPUT</span><span class="sxs-lookup"><span data-stu-id="53b16-181">INPUTS</span></span>

### <span data-ttu-id="53b16-182">System.String</span><span class="sxs-lookup"><span data-stu-id="53b16-182">System.String</span></span>

### <span data-ttu-id="53b16-183">System.Guid</span><span class="sxs-lookup"><span data-stu-id="53b16-183">System.Guid</span></span>

### <span data-ttu-id="53b16-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="53b16-184">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="53b16-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53b16-185">OUTPUTS</span></span>

### <span data-ttu-id="53b16-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="53b16-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="53b16-187">NOTE</span><span class="sxs-lookup"><span data-stu-id="53b16-187">NOTES</span></span>
<span data-ttu-id="53b16-188">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="53b16-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="53b16-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53b16-189">RELATED LINKS</span></span>

[<span data-ttu-id="53b16-190">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="53b16-190">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="53b16-191">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="53b16-191">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="53b16-192">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="53b16-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

