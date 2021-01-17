---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleAssignment.md
ms.openlocfilehash: 1b96617ce162f3b024cc8a5bd7df2d66c3820c38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365886"
---
# <span data-ttu-id="31c5e-101">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c5e-101">Get-AzRoleAssignment</span></span>

## <span data-ttu-id="31c5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="31c5e-103">Elenca le assegnazioni di ruolo di Azure RBAC nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="31c5e-104">Per impostazione predefinita, elenca tutte le assegnazioni di ruolo nell'abbonamento Azure selezionato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="31c5e-105">Usare i rispettivi parametri per elencare le assegnazioni a un utente specifico oppure per elencare le assegnazioni in una risorsa o un gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="31c5e-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="31c5e-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31c5e-106">SYNTAX</span></span>

### <span data-ttu-id="31c5e-107">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31c5e-107">EmptyParameterSet (Default)</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-108">ObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment -ObjectId <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzRoleAssignment [-ObjectId <String>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-116">SignInNameParameterSet</span></span>
```
Get-AzRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-120">SPNParameterSet</span></span>
```
Get-AzRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-121">ResourceGroupParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-122">ResourceParameterSet</span></span>
```
Get-AzRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31c5e-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="31c5e-123">ScopeParameterSet</span></span>
```
Get-AzRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31c5e-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31c5e-124">DESCRIPTION</span></span>
<span data-ttu-id="31c5e-125">Usare il comando Get-AzRoleAssignment per elencare tutte le assegnazioni di ruolo effettive in un ambito.</span><span class="sxs-lookup"><span data-stu-id="31c5e-125">Use the Get-AzRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="31c5e-126">Senza parametri, questo comando restituisce tutte le assegnazioni di ruolo effettuate sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="31c5e-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="31c5e-127">Questo elenco può essere filtrato usando i parametri di filtro per Principal, Role e scope.</span><span class="sxs-lookup"><span data-stu-id="31c5e-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="31c5e-128">L'oggetto dell'assegnazione deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="31c5e-129">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="31c5e-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="31c5e-130">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="31c5e-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="31c5e-131">Per specificare un'applicazione Azure AD, USA i parametri ServicePrincipalName o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="31c5e-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="31c5e-132">Il ruolo che viene assegnato deve essere specificato usando il parametro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="31c5e-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="31c5e-133">L'ambito in cui viene concesso l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="31c5e-134">Il valore predefinito è l'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="31c5e-135">L'ambito dell'assegnazione può essere specificato usando una delle combinazioni di parametri seguenti a.</span><span class="sxs-lookup"><span data-stu-id="31c5e-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="31c5e-136">Ambito: questo è l'ambito completo che inizia con/subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="31c5e-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="31c5e-137">In questo modo verranno filtrate le assegnazioni che sono effettive in quel particolare ambito, ossia tutte le assegnazioni in tale ambito e successive.</span><span class="sxs-lookup"><span data-stu-id="31c5e-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="31c5e-138">b.</span><span class="sxs-lookup"><span data-stu-id="31c5e-138">b.</span></span>
<span data-ttu-id="31c5e-139">ResourceGroupName-nome di un gruppo di risorse sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="31c5e-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="31c5e-140">In questo modo verranno filtrate le assegnazioni valide nel gruppo di risorse specificato c.</span><span class="sxs-lookup"><span data-stu-id="31c5e-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="31c5e-141">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource-identifica una determinata risorsa sotto l'abbonamento e filtra le assegnazioni effettive nell'ambito di tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="31c5e-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="31c5e-142">Per determinare l'accesso a un determinato utente nell'abbonamento, usare l'opzione ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="31c5e-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="31c5e-143">Verranno elencati tutti i ruoli assegnati all'utente e i gruppi a cui l'utente fa parte.</span><span class="sxs-lookup"><span data-stu-id="31c5e-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="31c5e-144">Usare l'opzione IncludeClassicAdministrators per visualizzare anche gli amministratori della sottoscrizione e i co-amministratori.</span><span class="sxs-lookup"><span data-stu-id="31c5e-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="31c5e-145">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31c5e-145">EXAMPLES</span></span>

### <span data-ttu-id="31c5e-146">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31c5e-146">Example 1</span></span>
```
PS C:\> Get-AzRoleAssignment
```

<span data-ttu-id="31c5e-147">Elencare tutte le assegnazioni di ruolo nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="31c5e-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="31c5e-148">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31c5e-148">Example 2</span></span>
```
PS C:\> Get-AzRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="31c5e-149">Ottiene tutte le assegnazioni di ruolo effettuate all'utente john.doe@contoso.com e i gruppi di cui è membro, in ambito testRG o superiore.</span><span class="sxs-lookup"><span data-stu-id="31c5e-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="31c5e-150">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="31c5e-150">Example 3</span></span>
```
PS C:\> Get-AzRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="31c5e-151">Ottiene tutte le assegnazioni di ruolo dell'entità servizio specificata</span><span class="sxs-lookup"><span data-stu-id="31c5e-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="31c5e-152">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="31c5e-152">Example 4</span></span>
```
PS C:\> Get-AzRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="31c5e-153">Ottiene le assegnazioni di ruolo nell'ambito del sito Web "Microsoft1".</span><span class="sxs-lookup"><span data-stu-id="31c5e-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="31c5e-154">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31c5e-154">PARAMETERS</span></span>

### <span data-ttu-id="31c5e-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c5e-155">-DefaultProfile</span></span>
<span data-ttu-id="31c5e-156">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="31c5e-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31c5e-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="31c5e-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="31c5e-158">Se specificato, restituisce i ruoli assegnati direttamente all'utente e ai gruppi di cui l'utente è un membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="31c5e-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="31c5e-159">Supportato solo per un utente principale.</span><span class="sxs-lookup"><span data-stu-id="31c5e-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="31c5e-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="31c5e-161">Se specificato, elenca anche gli amministratori classici della sottoscrizione (co-amministratori, amministratori del servizio e così via) assegnazioni di ruolo.</span><span class="sxs-lookup"><span data-stu-id="31c5e-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="31c5e-162">-ObjectId</span></span>
<span data-ttu-id="31c5e-163">ID Azure AD ObjectId dell'utente, del gruppo o del servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="31c5e-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="31c5e-164">Filtra tutte le assegnazioni effettuate all'entità specificata.</span><span class="sxs-lookup"><span data-stu-id="31c5e-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="31c5e-165">-ParentResource</span></span>
<span data-ttu-id="31c5e-166">La risorsa padre nella gerarchia della risorsa specificata usando il parametro resourceName.</span><span class="sxs-lookup"><span data-stu-id="31c5e-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="31c5e-167">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e resourceName.</span><span class="sxs-lookup"><span data-stu-id="31c5e-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c5e-168">-ResourceGroupName</span></span>
<span data-ttu-id="31c5e-169">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31c5e-169">The resource group name.</span></span>
<span data-ttu-id="31c5e-170">Elenca le assegnazioni di ruolo valide per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="31c5e-171">Se usato in combinazione con i parametri resourceName, ResourceType e ParentResource, il comando elenca le assegnazioni effettive presso le risorse del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="31c5e-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="31c5e-172">-ResourceName</span></span>
<span data-ttu-id="31c5e-173">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31c5e-173">The resource name.</span></span>
<span data-ttu-id="31c5e-174">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="31c5e-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="31c5e-175">Deve essere usato insieme ai parametri di ParentResource di ResourceGroupName, ResourceType e (facoltativamente).</span><span class="sxs-lookup"><span data-stu-id="31c5e-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="31c5e-176">-ResourceType</span></span>
<span data-ttu-id="31c5e-177">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="31c5e-177">The resource type.</span></span>
<span data-ttu-id="31c5e-178">Ad esempio Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="31c5e-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="31c5e-179">Deve essere usato insieme ai parametri ResourceGroupName, resourceName e (facoltativamente) ParentResource.</span><span class="sxs-lookup"><span data-stu-id="31c5e-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="31c5e-180">-RoleDefinitionId</span></span>
<span data-ttu-id="31c5e-181">ID del ruolo assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="31c5e-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="31c5e-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="31c5e-182">-RoleDefinitionName</span></span>
<span data-ttu-id="31c5e-183">Ruolo assegnato all'amministratore principale, vale a dire Reader, Contributor, Virtual Network Administrator e così via.</span><span class="sxs-lookup"><span data-stu-id="31c5e-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-184">-Ambito</span><span class="sxs-lookup"><span data-stu-id="31c5e-184">-Scope</span></span>
<span data-ttu-id="31c5e-185">Ambito dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="31c5e-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="31c5e-186">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="31c5e-186">In the format of relative URI.</span></span>
<span data-ttu-id="31c5e-187">Ad esempio/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="31c5e-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="31c5e-188">Deve iniziare con "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="31c5e-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="31c5e-189">Il comando Filtra tutte le assegnazioni effettive in tale ambito.</span><span class="sxs-lookup"><span data-stu-id="31c5e-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="31c5e-190">-ServicePrincipalName</span></span>
<span data-ttu-id="31c5e-191">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="31c5e-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="31c5e-192">Filtra tutte le assegnazioni effettuate all'applicazione Azure AD specificata.</span><span class="sxs-lookup"><span data-stu-id="31c5e-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="31c5e-193">-SignInName</span></span>
<span data-ttu-id="31c5e-194">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="31c5e-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="31c5e-195">Filtra tutte le assegnazioni effettuate all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="31c5e-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c5e-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c5e-196">CommonParameters</span></span>
<span data-ttu-id="31c5e-197">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c5e-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c5e-198">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31c5e-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c5e-199">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31c5e-199">INPUTS</span></span>

### <span data-ttu-id="31c5e-200">System. String</span><span class="sxs-lookup"><span data-stu-id="31c5e-200">System.String</span></span>

### <span data-ttu-id="31c5e-201">System. Guid</span><span class="sxs-lookup"><span data-stu-id="31c5e-201">System.Guid</span></span>

## <span data-ttu-id="31c5e-202">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31c5e-202">OUTPUTS</span></span>

### <span data-ttu-id="31c5e-203">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c5e-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="31c5e-204">Note</span><span class="sxs-lookup"><span data-stu-id="31c5e-204">NOTES</span></span>
<span data-ttu-id="31c5e-205">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="31c5e-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="31c5e-206">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31c5e-206">RELATED LINKS</span></span>

[<span data-ttu-id="31c5e-207">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c5e-207">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="31c5e-208">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31c5e-208">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="31c5e-209">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="31c5e-209">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

