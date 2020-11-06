---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 4ca9b3d731c4b4c0029dafa68a1f7e747c62dedb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520400"
---
# <span data-ttu-id="b71b8-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b71b8-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="b71b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b71b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b71b8-103">Rimuove un'assegnazione di ruolo all'entità specificata a cui viene assegnato un determinato ruolo in un determinato ambito.</span><span class="sxs-lookup"><span data-stu-id="b71b8-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b71b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b71b8-104">SYNTAX</span></span>

### <span data-ttu-id="b71b8-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b71b8-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-106">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-107">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b71b8-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b71b8-116">RoleAssignmentParameterSet</span><span class="sxs-lookup"><span data-stu-id="b71b8-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71b8-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b71b8-117">DESCRIPTION</span></span>
<span data-ttu-id="b71b8-118">Usa la Remove-AzureRmRoleAssignment unifiedgroup per revocare l'accesso a qualsiasi entità a un ambito specifico e a un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="b71b8-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>

<span data-ttu-id="b71b8-119">L'oggetto dell'assegnazione vale a dire l'entità deve essere specificata.</span><span class="sxs-lookup"><span data-stu-id="b71b8-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="b71b8-120">L'entità può essere un utente (usare i parametri SignInName o ObjectId per identificare un utente), il gruppo di sicurezza (usare il parametro ObjectId per identificare un gruppo) o l'entità del servizio (usare i parametri ServicePrincipalName o ObjectId per identificare un ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="b71b8-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>

<span data-ttu-id="b71b8-121">Il ruolo a cui è assegnata l'entità deve essere specificato usando il parametro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="b71b8-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="b71b8-122">L'ambito dell'assegnazione può essere specificato e, se non specificato, il valore predefinito è l'ambito dell'abbonamento, ossia cercherà di eliminare un'attività per l'entità e il ruolo specificati nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b71b8-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="b71b8-123">L'ambito dell'assegnazione può essere specificato usando uno dei parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b71b8-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="b71b8-124">un.</span><span class="sxs-lookup"><span data-stu-id="b71b8-124">a.</span></span>
<span data-ttu-id="b71b8-125">Ambito: questo è l'ambito completo che inizia con/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="b71b8-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="b71b8-126">ResourceGroupName-nome di un gruppo di risorse sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b71b8-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="b71b8-127">c.</span><span class="sxs-lookup"><span data-stu-id="b71b8-127">c.</span></span>
<span data-ttu-id="b71b8-128">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource-identifica una determinata risorsa sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b71b8-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="b71b8-129">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b71b8-129">EXAMPLES</span></span>

### <span data-ttu-id="b71b8-130">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b71b8-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="b71b8-131">Rimuove un'assegnazione di ruolo per john.doe@contoso.com gli utenti assegnati al ruolo di Reader nell'ambito ResourceGroup RG1.</span><span class="sxs-lookup"><span data-stu-id="b71b8-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="b71b8-132">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b71b8-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="b71b8-133">Rimuove l'assegnazione di ruolo all'entità del gruppo identificata da ObjectId e assegnata al ruolo di Reader.</span><span class="sxs-lookup"><span data-stu-id="b71b8-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="b71b8-134">Imposta come predefinito l'uso dell'abbonamento corrente come ambito per trovare l'attività da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b71b8-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="b71b8-135">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b71b8-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="b71b8-136">Rimuove il primo oggetto di assegnazione di ruolo recuperato dall'Get-AzureRmRoleAssignment unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="b71b8-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="b71b8-137">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b71b8-137">PARAMETERS</span></span>

### <span data-ttu-id="b71b8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71b8-138">-DefaultProfile</span></span>
<span data-ttu-id="b71b8-139">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b71b8-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b71b8-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b71b8-140">-InputObject</span></span>
<span data-ttu-id="b71b8-141">Oggetto assegnazione ruolo.</span><span class="sxs-lookup"><span data-stu-id="b71b8-141">Role Assignment object.</span></span>

```yaml
Type: PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-142">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b71b8-142">-ObjectId</span></span>
<span data-ttu-id="b71b8-143">ObjectId di Azure AD per l'utente, il gruppo o l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="b71b8-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b71b8-144">-ParentResource</span></span>
<span data-ttu-id="b71b8-145">La risorsa padre nella gerarchia (della risorsa specificata usando il parametro resourceName), se disponibile.</span><span class="sxs-lookup"><span data-stu-id="b71b8-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="b71b8-146">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e resourceName per costruire un ambito gerarchico in forma di URI relativo che identifichi la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b71b8-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b71b8-147">-PassThru</span></span>
<span data-ttu-id="b71b8-148">Se specificato, Visualizza l'assegnazione di ruolo eliminata</span><span class="sxs-lookup"><span data-stu-id="b71b8-148">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="b71b8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71b8-149">-ResourceGroupName</span></span>
<span data-ttu-id="b71b8-150">Il nome del gruppo di risorse a cui è assegnato il ruolo.</span><span class="sxs-lookup"><span data-stu-id="b71b8-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="b71b8-151">Tenta di eliminare un'assegnazione nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b71b8-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="b71b8-152">Quando viene usato in combinazione con i parametri resourceName, ResourceType e (facoltativamente) ParentResource, il comando costruisce un ambito gerarchico in forma di URI relativo che identifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b71b8-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b71b8-153">-ResourceName</span></span>
<span data-ttu-id="b71b8-154">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b71b8-154">The resource name.</span></span>
<span data-ttu-id="b71b8-155">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="b71b8-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b71b8-156">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e (facoltativamente) ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi la risorsa ed elimini un'attività in tale ambito.</span><span class="sxs-lookup"><span data-stu-id="b71b8-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b71b8-157">-ResourceType</span></span>
<span data-ttu-id="b71b8-158">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b71b8-158">The resource type.</span></span>
<span data-ttu-id="b71b8-159">Ad esempio Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="b71b8-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b71b8-160">Deve essere usato in combinazione con ResourceGroupName, resourceName e (facoltativamente) i parametri ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi la risorsa ed elimini un'attività nell'ambito di tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="b71b8-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-161">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b71b8-161">-RoleDefinitionId</span></span>
<span data-ttu-id="b71b8-162">ID del ruolo RBAC per cui l'assegnazione deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="b71b8-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b71b8-163">-RoleDefinitionName</span></span>
<span data-ttu-id="b71b8-164">Nome del ruolo RBAC per cui l'assegnazione deve essere eliminata, ad esempio lettore, collaboratore, amministratore di rete virtuale e così via.</span><span class="sxs-lookup"><span data-stu-id="b71b8-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-165">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b71b8-165">-Scope</span></span>
<span data-ttu-id="b71b8-166">Ambito dell'assegnazione di ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b71b8-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="b71b8-167">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="b71b8-167">In the format of relative URI.</span></span>
<span data-ttu-id="b71b8-168">Ad esempio "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="b71b8-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="b71b8-169">Se non specificato, tenterà di eliminare il ruolo a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b71b8-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="b71b8-170">Se specificato, dovrebbe iniziare con "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="b71b8-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b71b8-171">-ServicePrincipalName</span></span>
<span data-ttu-id="b71b8-172">ServicePrincipalName dell'applicazione Azure AD</span><span class="sxs-lookup"><span data-stu-id="b71b8-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-173">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b71b8-173">-SignInName</span></span>
<span data-ttu-id="b71b8-174">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b71b8-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b71b8-175">-Confirm</span></span>
<span data-ttu-id="b71b8-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71b8-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71b8-177">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71b8-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71b8-178">CommonParameters</span></span>
<span data-ttu-id="b71b8-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71b8-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71b8-180">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71b8-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71b8-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b71b8-181">INPUTS</span></span>

### <span data-ttu-id="b71b8-182">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b71b8-182">None</span></span>
<span data-ttu-id="b71b8-183">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b71b8-183">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b71b8-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b71b8-184">OUTPUTS</span></span>

### <span data-ttu-id="b71b8-185">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="b71b8-185">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="b71b8-186">Note</span><span class="sxs-lookup"><span data-stu-id="b71b8-186">NOTES</span></span>
<span data-ttu-id="b71b8-187">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="b71b8-187">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b71b8-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b71b8-188">RELATED LINKS</span></span>

[<span data-ttu-id="b71b8-189">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b71b8-189">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="b71b8-190">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b71b8-190">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="b71b8-191">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b71b8-191">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

