---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187470"
---
# <span data-ttu-id="c2a8c-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="c2a8c-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="c2a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a8c-103">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="c2a8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2a8c-104">SYNTAX</span></span>

### <span data-ttu-id="c2a8c-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2a8c-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2a8c-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="c2a8c-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a8c-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="c2a8c-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a8c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2a8c-108">DESCRIPTION</span></span>
<span data-ttu-id="c2a8c-109">Crea o aggiorna una definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="c2a8c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2a8c-110">EXAMPLES</span></span>

### <span data-ttu-id="c2a8c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2a8c-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="c2a8c-112">Crea una definizione di registrazione per i valori roleDefinitionId e principalId specificati direttamente.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="c2a8c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2a8c-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="c2a8c-114">Crea o aggiorna una definizione di registrazione con i dettagli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="c2a8c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c2a8c-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="c2a8c-116">Aggiorna una definizione di registrazione con i dettagli di autorizzazione e il nome della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="c2a8c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a8c-117">PARAMETERS</span></span>

### <span data-ttu-id="c2a8c-118">-Authorization</span><span class="sxs-lookup"><span data-stu-id="c2a8c-118">-Authorization</span></span>
<span data-ttu-id="c2a8c-119">Elenco di mapping delle autorizzazioni con principalId - roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a8c-120">-DefaultProfile</span></span>
<span data-ttu-id="c2a8c-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a8c-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2a8c-122">-Description</span></span>
<span data-ttu-id="c2a8c-123">Descrizione della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2a8c-124">-DisplayName</span></span>
<span data-ttu-id="c2a8c-125">Nome visualizzato della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="c2a8c-126">-ManagedByTenantId</span></span>
<span data-ttu-id="c2a8c-127">Identificatore del tenant ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c2a8c-128">-Name</span></span>
<span data-ttu-id="c2a8c-129">Nome univoco della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c2a8c-130">-PlanName</span></span>
<span data-ttu-id="c2a8c-131">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c2a8c-132">-PlanProduct</span></span>
<span data-ttu-id="c2a8c-133">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c2a8c-134">-PlanPublisher</span></span>
<span data-ttu-id="c2a8c-135">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="c2a8c-136">-PlanVersion</span></span>
<span data-ttu-id="c2a8c-137">Numero di versione del piano.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="c2a8c-138">-PrincipalId</span></span>
<span data-ttu-id="c2a8c-139">Identificatore dell'entità ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c2a8c-140">-RoleDefinitionId</span></span>
<span data-ttu-id="c2a8c-141">L'identificatore della definizione di ruolo per concedere le autorizzazioni all'identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2a8c-142">-AsJob</span></span>
<span data-ttu-id="c2a8c-143">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c2a8c-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2a8c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2a8c-144">-Confirm</span></span>
<span data-ttu-id="c2a8c-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a8c-146">-WhatIf</span></span>
<span data-ttu-id="c2a8c-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a8c-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a8c-149">CommonParameters</span></span>
<span data-ttu-id="c2a8c-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a8c-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2a8c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a8c-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2a8c-152">INPUTS</span></span>

### <span data-ttu-id="c2a8c-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c2a8c-153">None</span></span>
## <span data-ttu-id="c2a8c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2a8c-154">OUTPUTS</span></span>

### <span data-ttu-id="c2a8c-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="c2a8c-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="c2a8c-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2a8c-156">NOTES</span></span>

## <span data-ttu-id="c2a8c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2a8c-157">RELATED LINKS</span></span>
