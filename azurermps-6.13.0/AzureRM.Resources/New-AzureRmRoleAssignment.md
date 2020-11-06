---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: 130f2ff4c65f282ca03f775500400479d16cc79c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511511"
---
# <span data-ttu-id="6a9a3-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6a9a3-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="6a9a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9a3-103">Assegna il ruolo RBAC specificato all'oggetto Principal specificato, in corrispondenza dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a9a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-104">SYNTAX</span></span>

### <span data-ttu-id="6a9a3-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a9a3-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-106">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-107">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-108">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-109">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a9a3-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9a3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a9a3-116">DESCRIPTION</span></span>
<span data-ttu-id="6a9a3-117">Usare il comando New-AzureRMRoleAssignment per concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="6a9a3-118">L'accesso viene concesso assegnando il ruolo RBAC appropriato all'ambito corretto.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="6a9a3-119">Per concedere l'accesso all'intera sottoscrizione, assegnare un ruolo nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="6a9a3-120">Per concedere l'accesso a un gruppo di risorse specifico all'interno di un abbonamento, assegnare un ruolo nell'ambito del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="6a9a3-121">L'oggetto dell'assegnazione deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="6a9a3-122">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="6a9a3-123">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="6a9a3-124">Per specificare un'applicazione Azure AD, USA i parametri ApplicationId o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="6a9a3-125">Il ruolo che viene assegnato deve essere specificato usando il parametro RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="6a9a3-126">L'ambito in cui viene concesso l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="6a9a3-127">Il valore predefinito è l'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="6a9a3-128">L'ambito dell'assegnazione può essere specificato usando una delle combinazioni di parametri seguenti a.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="6a9a3-129">Ambito: questo è l'ambito completo che inizia con/subscriptions/ \<subscriptionId\> b.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="6a9a3-130">ResourceGroupName-per concedere l'accesso al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="6a9a3-131">c.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-131">c.</span></span>
<span data-ttu-id="6a9a3-132">ResourceName, ResourceType, ResourceGroupName e (facoltativamente) ParentResource-per specificare una determinata risorsa all'interno di un gruppo di risorse a cui concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="6a9a3-133">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-133">EXAMPLES</span></span>

### <span data-ttu-id="6a9a3-134">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a9a3-134">Example 1</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="6a9a3-135">Concedere l'accesso al ruolo di lettore a un utente in un ambito del gruppo di risorse con l'assegnazione di ruolo disponibile per la delega</span><span class="sxs-lookup"><span data-stu-id="6a9a3-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="6a9a3-136">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a9a3-136">Example 2</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="6a9a3-137">Concedere l'accesso a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="6a9a3-137">Grant access to a security group</span></span>

### <span data-ttu-id="6a9a3-138">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6a9a3-138">Example 3</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="6a9a3-139">Concedere l'accesso a un utente in una risorsa (sito Web)</span><span class="sxs-lookup"><span data-stu-id="6a9a3-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="6a9a3-140">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6a9a3-140">Example 4</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="6a9a3-141">Concedere l'accesso a un gruppo in una risorsa annidata (subnet)</span><span class="sxs-lookup"><span data-stu-id="6a9a3-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="6a9a3-142">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="6a9a3-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzureRmADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzureRmRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="6a9a3-143">Concedere l'accesso all'utilità di lettura a un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="6a9a3-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="6a9a3-144">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-144">PARAMETERS</span></span>

### <span data-ttu-id="6a9a3-145">-AllowDelegation</span><span class="sxs-lookup"><span data-stu-id="6a9a3-145">-AllowDelegation</span></span>
<span data-ttu-id="6a9a3-146">Contrassegno di delega durante la creazione di un'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="6a9a3-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6a9a3-147">-ApplicationId</span></span>
<span data-ttu-id="6a9a3-148">ID applicazione di ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6a9a3-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="6a9a3-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9a3-149">-DefaultProfile</span></span>
<span data-ttu-id="6a9a3-150">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6a9a3-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a3-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6a9a3-151">-ObjectId</span></span>
<span data-ttu-id="6a9a3-152">ObjectId di Azure AD per l'utente, il gruppo o l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-152">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a3-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="6a9a3-153">-ParentResource</span></span>
<span data-ttu-id="6a9a3-154">La risorsa padre nella gerarchia (della risorsa specificata usando il parametro resourceName).</span><span class="sxs-lookup"><span data-stu-id="6a9a3-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="6a9a3-155">Deve essere usato solo in combinazione con i parametri ResourceGroupName, ResourceType e resourceName per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6a9a3-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-156">-ResourceGroupName</span></span>
<span data-ttu-id="6a9a3-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-157">The resource group name.</span></span>
<span data-ttu-id="6a9a3-158">Crea un'attività efficace nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="6a9a3-159">Quando viene usato in combinazione con i parametri resourceName, ResourceType e (facoltativamente) ParentResource, il comando costruisce un ambito gerarchico in forma di URI relativo che identifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6a9a3-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-160">-ResourceName</span></span>
<span data-ttu-id="6a9a3-161">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-161">The resource name.</span></span>
<span data-ttu-id="6a9a3-162">Ad esempio storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="6a9a3-163">Deve essere usato solo in combinazione con i parametri ResourceGroupName, ResourceType e (facoltativamente) ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6a9a3-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6a9a3-164">-ResourceType</span></span>
<span data-ttu-id="6a9a3-165">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-165">The resource type.</span></span>
<span data-ttu-id="6a9a3-166">Ad esempio Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="6a9a3-167">Deve essere usato solo in combinazione con ResourceGroupName, resourceName e (facoltativamente) i parametri ParentResource per costruire un ambito gerarchico in forma di URI relativo che identifichi una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="6a9a3-168">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6a9a3-168">-RoleDefinitionId</span></span>
<span data-ttu-id="6a9a3-169">ID del ruolo RBAC che deve essere assegnato all'entità.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="6a9a3-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-170">-RoleDefinitionName</span></span>
<span data-ttu-id="6a9a3-171">Nome del ruolo RBAC che deve essere assegnato all'amministratore principale, vale a dire Reader, Contributor, Virtual Network Administrator e così via.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a3-172">-Ambito</span><span class="sxs-lookup"><span data-stu-id="6a9a3-172">-Scope</span></span>
<span data-ttu-id="6a9a3-173">Ambito dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="6a9a3-174">Nel formato dell'URI relativo.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-174">In the format of relative URI.</span></span>
<span data-ttu-id="6a9a3-175">Ad esempio "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span><span class="sxs-lookup"><span data-stu-id="6a9a3-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="6a9a3-176">Se non specificato, creerà l'assegnazione di ruolo a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="6a9a3-177">Se specificato, dovrebbe iniziare con "/subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="6a9a3-177">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a3-178">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-178">-SignInName</span></span>
<span data-ttu-id="6a9a3-179">L'indirizzo di posta elettronica o il nome dell'entità utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-179">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="6a9a3-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9a3-180">CommonParameters</span></span>
<span data-ttu-id="6a9a3-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9a3-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9a3-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9a3-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-183">INPUTS</span></span>

### <span data-ttu-id="6a9a3-184">System. Guid</span><span class="sxs-lookup"><span data-stu-id="6a9a3-184">System.Guid</span></span>

### <span data-ttu-id="6a9a3-185">System. String</span><span class="sxs-lookup"><span data-stu-id="6a9a3-185">System.String</span></span>

## <span data-ttu-id="6a9a3-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a9a3-186">OUTPUTS</span></span>

### <span data-ttu-id="6a9a3-187">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6a9a3-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="6a9a3-188">Note</span><span class="sxs-lookup"><span data-stu-id="6a9a3-188">NOTES</span></span>
<span data-ttu-id="6a9a3-189">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="6a9a3-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6a9a3-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-190">RELATED LINKS</span></span>

[<span data-ttu-id="6a9a3-191">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6a9a3-191">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="6a9a3-192">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6a9a3-192">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="6a9a3-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6a9a3-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
