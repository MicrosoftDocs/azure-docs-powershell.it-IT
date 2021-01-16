---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325396"
---
# <span data-ttu-id="b5302-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5302-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="b5302-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5302-102">SYNOPSIS</span></span>
<span data-ttu-id="b5302-103">Elenca Azure RBAC nega le assegnazioni nell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="b5302-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="b5302-104">Per impostazione predefinita, elenca tutte le assegnazioni di negazione nell'abbonamento Azure selezionato.</span><span class="sxs-lookup"><span data-stu-id="b5302-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="b5302-105">USA i rispettivi parametri per elencare le assegnazioni a un utente specifico oppure per elencare le assegnazioni in un gruppo di risorse o una risorsa specifico.</span><span class="sxs-lookup"><span data-stu-id="b5302-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="b5302-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5302-106">SYNTAX</span></span>

### <span data-ttu-id="b5302-107">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5302-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5302-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5302-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5302-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5302-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5302-125">DESCRIPTION</span></span>
<span data-ttu-id="b5302-126">Usare il comando Get-AzDenyAssignment per elencare tutte le assegnazioni di negazione valide per un ambito.</span><span class="sxs-lookup"><span data-stu-id="b5302-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="b5302-127">Senza parametri, questo comando restituisce tutte le assegnazioni di negazione effettuate sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b5302-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="b5302-128">Questo elenco può essere filtrato usando i parametri di filtro per Principal, nega il nome e l'ambito dell'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="b5302-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="b5302-129">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b5302-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="b5302-130">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b5302-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="b5302-131">Per specificare un'applicazione Azure AD, USA i parametri ServicePrincipalName o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="b5302-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="b5302-132">L'ambito in cui viene negato l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="b5302-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="b5302-133">Il valore predefinito è l'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="b5302-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="b5302-134">L'ambito dell'assegnazione Deny può essere specificato usando una delle combinazioni di parametri seguenti a.</span><span class="sxs-lookup"><span data-stu-id="b5302-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="b5302-135">Ambito: questo è l'ambito completo che inizia con/subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="b5302-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="b5302-136">In questo modo verranno filtrate le assegnazioni che sono effettive in quel particolare ambito, vale a dire tutte le attività negate in tale ambito e successive.</span><span class="sxs-lookup"><span data-stu-id="b5302-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="b5302-137">b.</span><span class="sxs-lookup"><span data-stu-id="b5302-137">b.</span></span>
<span data-ttu-id="b5302-138">ResourceGroupName-nome di un gruppo di risorse sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b5302-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="b5302-139">In questo modo verranno filtrate le assegnazioni effettive al gruppo di risorse specificato, ossia tutte le assegnazioni negate in tale ambito e successive.</span><span class="sxs-lookup"><span data-stu-id="b5302-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="b5302-140">c.</span><span class="sxs-lookup"><span data-stu-id="b5302-140">c.</span></span>
<span data-ttu-id="b5302-141">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource-identifica una determinata risorsa sotto l'abbonamento e filtra le assegnazioni valide per l'ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5302-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="b5302-142">Per determinare l'accesso negato per un determinato utente nell'abbonamento, usare l'opzione ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="b5302-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="b5302-143">Verranno elencate tutte le assegnazioni di negazione assegnate all'utente e i gruppi a cui l'utente fa parte.</span><span class="sxs-lookup"><span data-stu-id="b5302-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="b5302-144">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5302-144">EXAMPLES</span></span>

### <span data-ttu-id="b5302-145">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5302-145">Example 1</span></span>

<span data-ttu-id="b5302-146">Elencare tutte le assegnazioni di negazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="b5302-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b5302-147">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b5302-147">Example 2</span></span>

<span data-ttu-id="b5302-148">Ottiene tutte le assegnazioni di negazione effettuate all'utente nell' john.doe@contoso.com ambito testRG e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b5302-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b5302-149">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b5302-149">Example 3</span></span>

<span data-ttu-id="b5302-150">Ottiene tutte le assegnazioni Deny dell'entità servizio specificata</span><span class="sxs-lookup"><span data-stu-id="b5302-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="b5302-151">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b5302-151">Example 4</span></span>

<span data-ttu-id="b5302-152">Ottiene le assegnazioni di negazione nell'ambito del sito Web "Microsoft1".</span><span class="sxs-lookup"><span data-stu-id="b5302-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="b5302-153">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5302-153">PARAMETERS</span></span>

### <span data-ttu-id="b5302-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5302-154">-DefaultProfile</span></span>
<span data-ttu-id="b5302-155">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5302-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5302-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b5302-156">-DenyAssignmentName</span></span>
<span data-ttu-id="b5302-157">Nome dell'assegnazione di negazione.</span><span class="sxs-lookup"><span data-stu-id="b5302-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5302-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b5302-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="b5302-159">Se specificato, restituisce la negazione delle assegnazioni assegnate direttamente all'utente e ai gruppi di cui l'utente è un membro (transitivamente).</span><span class="sxs-lookup"><span data-stu-id="b5302-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="b5302-160">Supportato solo per un utente principale.</span><span class="sxs-lookup"><span data-stu-id="b5302-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="b5302-161">-ID</span><span class="sxs-lookup"><span data-stu-id="b5302-161">-Id</span></span>
<span data-ttu-id="b5302-162">Nega ID assegnazione.</span><span class="sxs-lookup"><span data-stu-id="b5302-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5302-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b5302-163">-ObjectId</span></span>
<span data-ttu-id="b5302-164">ID Azure AD ObjectId dell'utente, del gruppo o del servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="b5302-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="b5302-165">Filtra tutte le assegnazioni di negazione effettuate all'entità specificata.</span><span class="sxs-lookup"><span data-stu-id="b5302-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5302-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b5302-166">-ParentResource</span></span>
<span data-ttu-id="b5302-167">La risorsa padre nella gerarchia della risorsa specificata usando il parametro resourceName.</span><span class="sxs-lookup"><span data-stu-id="b5302-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="b5302-168">Deve essere usato insieme ai parametri ResourceGroupName, ResourceType e resourceName.</span><span class="sxs-lookup"><span data-stu-id="b5302-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="b5302-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5302-169">-ResourceGroupName</span></span>
<span data-ttu-id="b5302-170">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5302-170">The resource group name.</span></span>
<span data-ttu-id="b5302-171">Gli elenchi negano le assegnazioni valide per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b5302-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="b5302-172">Se usato in combinazione con i parametri resourceName, ResourceType e ParentResource, il comando elenca le assegnazioni valide per le risorse del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="b5302-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="b5302-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b5302-173">-ResourceName</span></span>
<span data-ttu-id="b5302-174">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5302-174">The resource name.</span></span>
<span data-ttu-id="b5302-175">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="b5302-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="b5302-176">Deve essere usato insieme ai parametri di ParentResource di ResourceGroupName, ResourceType e (facoltativamente).</span><span class="sxs-lookup"><span data-stu-id="b5302-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="b5302-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b5302-177">-ResourceType</span></span>
<span data-ttu-id="b5302-178">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5302-178">The resource type.</span></span>
<span data-ttu-id="b5302-179">Ad esempio Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="b5302-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="b5302-180">Deve essere usato insieme ai parametri ResourceGroupName, resourceName e (facoltativamente) ParentResource.</span><span class="sxs-lookup"><span data-stu-id="b5302-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="b5302-181">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b5302-181">-Scope</span></span>
<span data-ttu-id="b5302-182">Ambito dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="b5302-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="b5302-183">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="b5302-183">In the format of relative URI.</span></span>
<span data-ttu-id="b5302-184">Ad esempio/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="b5302-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="b5302-185">Deve iniziare con "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="b5302-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="b5302-186">Il comando Filtra tutte le assegnazioni di negazione valide in tale ambito.</span><span class="sxs-lookup"><span data-stu-id="b5302-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="b5302-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b5302-187">-ServicePrincipalName</span></span>
<span data-ttu-id="b5302-188">ServicePrincipalName dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b5302-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="b5302-189">Filtra tutte le assegnazioni di negazione effettuate all'applicazione Azure AD specificata.</span><span class="sxs-lookup"><span data-stu-id="b5302-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="b5302-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b5302-190">-SignInName</span></span>
<span data-ttu-id="b5302-191">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b5302-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="b5302-192">Filtra tutte le assegnazioni di negazione effettuate all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="b5302-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="b5302-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5302-193">CommonParameters</span></span>
<span data-ttu-id="b5302-194">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5302-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5302-195">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5302-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5302-196">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5302-196">INPUTS</span></span>

### <span data-ttu-id="b5302-197">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b5302-197">System.Guid</span></span>

### <span data-ttu-id="b5302-198">System. String</span><span class="sxs-lookup"><span data-stu-id="b5302-198">System.String</span></span>

## <span data-ttu-id="b5302-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5302-199">OUTPUTS</span></span>

### <span data-ttu-id="b5302-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="b5302-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="b5302-201">Note</span><span class="sxs-lookup"><span data-stu-id="b5302-201">NOTES</span></span>
<span data-ttu-id="b5302-202">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="b5302-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b5302-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5302-203">RELATED LINKS</span></span>
