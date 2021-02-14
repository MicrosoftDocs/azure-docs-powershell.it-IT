---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181950"
---
# <span data-ttu-id="61e4f-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="61e4f-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="61e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="61e4f-103">Assegnare una definizione di progetto a una sottoscrizione o a un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="61e4f-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="61e4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61e4f-104">SYNTAX</span></span>

### <span data-ttu-id="61e4f-105">CreateBlueprintAssignment (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61e4f-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e4f-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="61e4f-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e4f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="61e4f-108">Assegnare una definizione di progetto a una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="61e4f-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="61e4f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="61e4f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61e4f-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="61e4f-111">Creare una nuova assegnazione della progetto della definizione del progetto all'interno della sottoscrizione specificata usando il parametro definito e `$blueprintObject` il dizionario del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61e4f-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="61e4f-112">Usa le identità assegnate dal sistema.</span><span class="sxs-lookup"><span data-stu-id="61e4f-112">Uses system-assigned identity.</span></span> <span data-ttu-id="61e4f-113">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="61e4f-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="61e4f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="61e4f-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="61e4f-115">Creare una nuova assegnazione della progetto della definizione del progetto all'interno della sottoscrizione specificata usando il dizionario del parametro definito e del gruppo di risorse e configurando il blocco delle risorse su `$blueprintObject` **AllResources.**</span><span class="sxs-lookup"><span data-stu-id="61e4f-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="61e4f-116">Per impostazione predefinita, viene utilizzato l'uso delle identità assegnate dal sistema.</span><span class="sxs-lookup"><span data-stu-id="61e4f-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="61e4f-117">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="61e4f-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="61e4f-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="61e4f-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="61e4f-119">Creare una nuova assegnazione della progetto della definizione di progetto all'interno della sottoscrizione specificata usando il parametro definito e il dizionario del gruppo di risorse usando l'ID di identità `$blueprintObject` assegnato dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="61e4f-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="61e4f-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="61e4f-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="61e4f-121">Creare un'attività di progetto tramite un file di attività.</span><span class="sxs-lookup"><span data-stu-id="61e4f-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="61e4f-122">Il formato del file di assegnazione è disponibile negli esempi di richiesta/risposta all'indirizzo: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="61e4f-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="61e4f-123">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="61e4f-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="61e4f-124">Creare una nuova assegnazione della progetto della definizione di progetto mirata alla sottoscrizione specificata all'interno del gruppo di `$blueprintObject` gestione specificato usando il parametro definito.</span><span class="sxs-lookup"><span data-stu-id="61e4f-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="61e4f-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61e4f-125">PARAMETERS</span></span>

### <span data-ttu-id="61e4f-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="61e4f-126">-AssignmentFile</span></span>
<span data-ttu-id="61e4f-127">Posizione del file dell'assegnazione in formato JSON sul disco.</span><span class="sxs-lookup"><span data-stu-id="61e4f-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-128">-Progetto</span><span class="sxs-lookup"><span data-stu-id="61e4f-128">-Blueprint</span></span>
<span data-ttu-id="61e4f-129">Oggetto definizione progetto.</span><span class="sxs-lookup"><span data-stu-id="61e4f-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e4f-130">-DefaultProfile</span></span>
<span data-ttu-id="61e4f-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61e4f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e4f-132">-Location</span><span class="sxs-lookup"><span data-stu-id="61e4f-132">-Location</span></span>
<span data-ttu-id="61e4f-133">Area geografica in cui creare le identità gestite.</span><span class="sxs-lookup"><span data-stu-id="61e4f-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="61e4f-134">Scopri di più su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="61e4f-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="61e4f-135">-Lock</span></span>
<span data-ttu-id="61e4f-136">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="61e4f-136">Lock resources.</span></span>
<span data-ttu-id="61e4f-137">Scopri di più su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="61e4f-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="61e4f-138">-ManagementGroupId</span></span>
<span data-ttu-id="61e4f-139">ID del gruppo di gestione in cui verranno salvate le assegnazioni del progetto.</span><span class="sxs-lookup"><span data-stu-id="61e4f-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="61e4f-140">-Name</span></span>
<span data-ttu-id="61e4f-141">Nome dell'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="61e4f-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="61e4f-142">-Parameter</span></span>
<span data-ttu-id="61e4f-143">Parametri dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="61e4f-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="61e4f-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="61e4f-145">Tabella hash dei parametri da passare all'elemento del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61e4f-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="61e4f-146">-SecureStringParameter</span></span>
<span data-ttu-id="61e4f-147">Parametro della stringa di protezione per ID di risorsa KeyVault, nome e versione.</span><span class="sxs-lookup"><span data-stu-id="61e4f-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61e4f-148">-SubscriptionId</span></span>
<span data-ttu-id="61e4f-149">ID sottoscrizione per assegnare la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="61e4f-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="61e4f-150">Può essere un elenco con valori delimitati da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="61e4f-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="61e4f-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="61e4f-152">Identità assegnate dal sistema (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="61e4f-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="61e4f-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="61e4f-154">Identità assegnate dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="61e4f-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4f-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e4f-155">-Confirm</span></span>
<span data-ttu-id="61e4f-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e4f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e4f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e4f-157">-WhatIf</span></span>
<span data-ttu-id="61e4f-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61e4f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e4f-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61e4f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e4f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e4f-160">CommonParameters</span></span>
<span data-ttu-id="61e4f-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e4f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e4f-162">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61e4f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e4f-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="61e4f-163">INPUTS</span></span>

### <span data-ttu-id="61e4f-164">System.String</span><span class="sxs-lookup"><span data-stu-id="61e4f-164">System.String</span></span>

### <span data-ttu-id="61e4f-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="61e4f-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="61e4f-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="61e4f-166">System.String[]</span></span>

### <span data-ttu-id="61e4f-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="61e4f-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="61e4f-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61e4f-168">OUTPUTS</span></span>

### <span data-ttu-id="61e4f-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="61e4f-169">System.Object</span></span>
## <span data-ttu-id="61e4f-170">NOTE</span><span class="sxs-lookup"><span data-stu-id="61e4f-170">NOTES</span></span>

## <span data-ttu-id="61e4f-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61e4f-171">RELATED LINKS</span></span>
