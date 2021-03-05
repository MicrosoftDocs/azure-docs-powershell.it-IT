---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 0e5c562d5b536e95d40bdbc1c08b2d778574fd41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001869"
---
# <span data-ttu-id="c154a-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c154a-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c154a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c154a-102">SYNOPSIS</span></span>
<span data-ttu-id="c154a-103">Aggiornare un'assegnazione di progetto esistente.</span><span class="sxs-lookup"><span data-stu-id="c154a-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c154a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c154a-104">SYNTAX</span></span>

### <span data-ttu-id="c154a-105">UpdateBlueprintAssignment (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c154a-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c154a-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="c154a-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c154a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c154a-107">DESCRIPTION</span></span>
<span data-ttu-id="c154a-108">Aggiornare un'assegnazione di progetto esistente.</span><span class="sxs-lookup"><span data-stu-id="c154a-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c154a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c154a-109">EXAMPLES</span></span>

### <span data-ttu-id="c154a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c154a-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c154a-111">Aggiornare un'assegnazione della progetto esistente della definizione del progetto `$blueprintObject` all'interno della sottoscrizione specificata, aggiornando i parametri.</span><span class="sxs-lookup"><span data-stu-id="c154a-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="c154a-112">Usa le identità assegnate dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c154a-112">Uses system-assigned identity.</span></span> <span data-ttu-id="c154a-113">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="c154a-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="c154a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c154a-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c154a-115">Aggiornare un'assegnazione di progetto esistente tramite un file di attività.</span><span class="sxs-lookup"><span data-stu-id="c154a-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="c154a-116">Il formato del file di assegnazione è disponibile negli esempi di richiesta/risposta all'indirizzo: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="c154a-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="c154a-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c154a-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="c154a-118">Aggiornare un'assegnazione del progetto esistente della definizione del progetto per la sottoscrizione specificata all'interno del `$blueprintObject` gruppo di gestione specificato usando il parametro definito.</span><span class="sxs-lookup"><span data-stu-id="c154a-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="c154a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c154a-119">PARAMETERS</span></span>

### <span data-ttu-id="c154a-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="c154a-120">-AssignmentFile</span></span>
<span data-ttu-id="c154a-121">Posizione del file dell'assegnazione in formato JSON sul disco.</span><span class="sxs-lookup"><span data-stu-id="c154a-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-122">-Progetto</span><span class="sxs-lookup"><span data-stu-id="c154a-122">-Blueprint</span></span>
<span data-ttu-id="c154a-123">Oggetto progetto.</span><span class="sxs-lookup"><span data-stu-id="c154a-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c154a-124">-DefaultProfile</span></span>
<span data-ttu-id="c154a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c154a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c154a-126">-Location</span><span class="sxs-lookup"><span data-stu-id="c154a-126">-Location</span></span>
<span data-ttu-id="c154a-127">Area geografica in cui creare le identità gestite.</span><span class="sxs-lookup"><span data-stu-id="c154a-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="c154a-128">Scopri di più su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="c154a-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="c154a-129">-Lock</span></span>
<span data-ttu-id="c154a-130">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="c154a-130">Lock resources.</span></span>
<span data-ttu-id="c154a-131">Scopri di più su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="c154a-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c154a-132">-ManagementGroupId</span></span>
<span data-ttu-id="c154a-133">ID del gruppo di gestione in cui verranno salvate le assegnazioni del progetto.</span><span class="sxs-lookup"><span data-stu-id="c154a-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="c154a-134">-Name</span></span>
<span data-ttu-id="c154a-135">Nome dell'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="c154a-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c154a-136">-Parameter</span></span>
<span data-ttu-id="c154a-137">Parametro dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c154a-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="c154a-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="c154a-139">Tabella hash dei parametri da passare all'elemento del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c154a-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="c154a-140">-SecureStringParameter</span></span>
<span data-ttu-id="c154a-141">Parametro della stringa di protezione per ID di risorsa KeyVault, nome e versione.</span><span class="sxs-lookup"><span data-stu-id="c154a-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c154a-142">-SubscriptionId</span></span>
<span data-ttu-id="c154a-143">SubscriptionId per assegnare il progetto.</span><span class="sxs-lookup"><span data-stu-id="c154a-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="c154a-144">Può essere un elenco con valori delimitati da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="c154a-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c154a-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c154a-146">Identità assegnate dal sistema (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c154a-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c154a-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="c154a-148">Identità assegnate dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c154a-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c154a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c154a-149">-Confirm</span></span>
<span data-ttu-id="c154a-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c154a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c154a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c154a-151">-WhatIf</span></span>
<span data-ttu-id="c154a-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c154a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c154a-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c154a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c154a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c154a-154">CommonParameters</span></span>
<span data-ttu-id="c154a-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c154a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c154a-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c154a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c154a-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="c154a-157">INPUTS</span></span>

### <span data-ttu-id="c154a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c154a-158">System.String</span></span>

### <span data-ttu-id="c154a-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c154a-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c154a-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c154a-160">System.String[]</span></span>

### <span data-ttu-id="c154a-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c154a-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c154a-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c154a-162">OUTPUTS</span></span>

### <span data-ttu-id="c154a-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="c154a-163">System.Object</span></span>
## <span data-ttu-id="c154a-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="c154a-164">NOTES</span></span>

## <span data-ttu-id="c154a-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c154a-165">RELATED LINKS</span></span>
