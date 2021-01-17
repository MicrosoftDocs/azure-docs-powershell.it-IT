---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: 2ec39bc66b3b027cb7b5ef9dda09734f8aaf457a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474197"
---
# <span data-ttu-id="9291b-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9291b-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="9291b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9291b-102">SYNOPSIS</span></span>
<span data-ttu-id="9291b-103">Assegna il ruolo RBAC specificato all'oggetto Principal specificato, in corrispondenza dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="9291b-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="9291b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9291b-104">SYNTAX</span></span>

### <span data-ttu-id="9291b-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9291b-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-108">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> [-Description <String>] [-Condition <String>]
 [-ConditionVersion <String>] -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-Description <String>]
 [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-Description <String>] [-Condition <String>] [-ConditionVersion <String>] [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9291b-115">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9291b-115">InputFileParameterSet</span></span>
```
New-AzRoleAssignment -InputFile <String> [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9291b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9291b-116">DESCRIPTION</span></span>
<span data-ttu-id="9291b-117">Usare il comando New-AzRoleAssignment per concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9291b-117">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="9291b-118">L'accesso viene concesso assegnando il ruolo RBAC appropriato all'ambito corretto.</span><span class="sxs-lookup"><span data-stu-id="9291b-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="9291b-119">Per concedere l'accesso all'intera sottoscrizione, assegnare un ruolo nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9291b-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="9291b-120">Per concedere l'accesso a un gruppo di risorse specifico all'interno di un abbonamento, assegnare un ruolo nell'ambito del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9291b-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="9291b-121">L'oggetto dell'assegnazione deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="9291b-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="9291b-122">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="9291b-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="9291b-123">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="9291b-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="9291b-124">Per specificare un'applicazione Azure AD, USA i parametri ApplicationId o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="9291b-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="9291b-125">Il ruolo che viene assegnato deve essere specificato usando il parametro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="9291b-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="9291b-126">L'ambito in cui viene concesso l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="9291b-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="9291b-127">Il valore predefinito è l'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="9291b-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="9291b-128">L'ambito dell'assegnazione può essere specificato usando una delle combinazioni di parametri seguenti a.</span><span class="sxs-lookup"><span data-stu-id="9291b-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="9291b-129">Ambito: questo è l'ambito completo che inizia con/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="9291b-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="9291b-130">ResourceGroupName-per concedere l'accesso al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9291b-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="9291b-131">c.</span><span class="sxs-lookup"><span data-stu-id="9291b-131">c.</span></span>
<span data-ttu-id="9291b-132">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource-per specificare una determinata risorsa all'interno di un gruppo di risorse a cui concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9291b-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="9291b-133">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9291b-133">EXAMPLES</span></span>

### <span data-ttu-id="9291b-134">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9291b-134">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="9291b-135">Concedere l'accesso al ruolo di lettore a un utente in un ambito del gruppo di risorse con l'assegnazione di ruolo disponibile per la delega</span><span class="sxs-lookup"><span data-stu-id="9291b-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="9291b-136">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9291b-136">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="9291b-137">Concedere l'accesso a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="9291b-137">Grant access to a security group</span></span>

### <span data-ttu-id="9291b-138">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9291b-138">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="9291b-139">Concedere l'accesso a un utente in una risorsa (sito Web)</span><span class="sxs-lookup"><span data-stu-id="9291b-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="9291b-140">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9291b-140">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="9291b-141">Concedere l'accesso a un gruppo in una risorsa annidata (subnet)</span><span class="sxs-lookup"><span data-stu-id="9291b-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="9291b-142">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="9291b-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="9291b-143">Concedere l'accesso all'utilità di lettura a un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="9291b-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="9291b-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9291b-144">PARAMETERS</span></span>

### <span data-ttu-id="9291b-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="9291b-145">-AllowDelegation</span></span>
<span data-ttu-id="9291b-146">Contrassegno di delega durante la creazione di un'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="9291b-146">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9291b-147">-ApplicationId</span></span>
<span data-ttu-id="9291b-148">ID applicazione di ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9291b-148">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-149">-Condition</span><span class="sxs-lookup"><span data-stu-id="9291b-149">-Condition</span></span>
<span data-ttu-id="9291b-150">Condizione da applicare a RoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="9291b-150">Condition to be applied to the RoleAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-151">-ConditionVersion</span><span class="sxs-lookup"><span data-stu-id="9291b-151">-ConditionVersion</span></span>
<span data-ttu-id="9291b-152">Versione della condizione.</span><span class="sxs-lookup"><span data-stu-id="9291b-152">Version of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9291b-153">-DefaultProfile</span></span>
<span data-ttu-id="9291b-154">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9291b-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9291b-155">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9291b-155">-Description</span></span>
<span data-ttu-id="9291b-156">Breve descrizione dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="9291b-156">Brief description of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-157">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9291b-157">-InputFile</span></span>
<span data-ttu-id="9291b-158">Percorso del JSON di assegnazione di ruolo</span><span class="sxs-lookup"><span data-stu-id="9291b-158">Path to role assignment json</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-159">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9291b-159">-ObjectId</span></span>
<span data-ttu-id="9291b-160">ObjectId di Azure AD per l'utente, il gruppo o l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="9291b-160">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-161">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="9291b-161">-ParentResource</span></span>
<span data-ttu-id="9291b-162">La risorsa padre nella gerarchia (della risorsa specificata usando il parametro resourceName).</span><span class="sxs-lookup"><span data-stu-id="9291b-162">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="9291b-163">Deve essere usato solo in combinazione con i parametri ResourceGroupName, ResourceType e resourceName per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-163">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9291b-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9291b-164">-ResourceGroupName</span></span>
<span data-ttu-id="9291b-165">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9291b-165">The resource group name.</span></span>
<span data-ttu-id="9291b-166">Crea un'attività efficace nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9291b-166">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="9291b-167">Quando viene usato in combinazione con i parametri resourceName, ResourceType e (facoltativamente) ParentResource, il comando costruisce un ambito gerarchico in forma di URI relativo che identifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-167">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-168">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9291b-168">-ResourceName</span></span>
<span data-ttu-id="9291b-169">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-169">The resource name.</span></span>
<span data-ttu-id="9291b-170">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="9291b-170">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="9291b-171">Deve essere usato solo in combinazione con i parametri ResourceGroupName, ResourceType e (facoltativamente) ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-171">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9291b-172">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9291b-172">-ResourceType</span></span>
<span data-ttu-id="9291b-173">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-173">The resource type.</span></span>
<span data-ttu-id="9291b-174">Ad esempio Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="9291b-174">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="9291b-175">Deve essere usato solo in combinazione con ResourceGroupName, resourceName e (facoltativamente) i parametri ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9291b-175">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="9291b-176">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9291b-176">-RoleDefinitionId</span></span>
<span data-ttu-id="9291b-177">ID del ruolo RBAC che deve essere assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="9291b-177">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="9291b-178">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9291b-178">-RoleDefinitionName</span></span>
<span data-ttu-id="9291b-179">Nome del ruolo RBAC che deve essere assegnato all'amministratore principale, vale a dire Reader, Contributor, Virtual Network Administrator e così via.</span><span class="sxs-lookup"><span data-stu-id="9291b-179">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-180">-Ambito</span><span class="sxs-lookup"><span data-stu-id="9291b-180">-Scope</span></span>
<span data-ttu-id="9291b-181">Ambito dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="9291b-181">The Scope of the role assignment.</span></span>
<span data-ttu-id="9291b-182">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="9291b-182">In the format of relative URI.</span></span>
<span data-ttu-id="9291b-183">Ad esempio "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="9291b-183">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="9291b-184">Se non specificato, creerà l'assegnazione di ruolo a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9291b-184">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="9291b-185">Se specificato, dovrebbe iniziare con "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="9291b-185">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-186">-SignInName</span><span class="sxs-lookup"><span data-stu-id="9291b-186">-SignInName</span></span>
<span data-ttu-id="9291b-187">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9291b-187">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9291b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9291b-188">CommonParameters</span></span>
<span data-ttu-id="9291b-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9291b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9291b-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9291b-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9291b-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9291b-191">INPUTS</span></span>

### <span data-ttu-id="9291b-192">System. String</span><span class="sxs-lookup"><span data-stu-id="9291b-192">System.String</span></span>

### <span data-ttu-id="9291b-193">System. Guid</span><span class="sxs-lookup"><span data-stu-id="9291b-193">System.Guid</span></span>

## <span data-ttu-id="9291b-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9291b-194">OUTPUTS</span></span>

### <span data-ttu-id="9291b-195">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9291b-195">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="9291b-196">Note</span><span class="sxs-lookup"><span data-stu-id="9291b-196">NOTES</span></span>
<span data-ttu-id="9291b-197">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="9291b-197">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9291b-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9291b-198">RELATED LINKS</span></span>

[<span data-ttu-id="9291b-199">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9291b-199">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="9291b-200">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9291b-200">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="9291b-201">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9291b-201">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
