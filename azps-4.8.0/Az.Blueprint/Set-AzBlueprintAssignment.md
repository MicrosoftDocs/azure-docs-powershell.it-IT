---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188562"
---
# <span data-ttu-id="55b26-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="55b26-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="55b26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55b26-102">SYNOPSIS</span></span>
<span data-ttu-id="55b26-103">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="55b26-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="55b26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55b26-104">SYNTAX</span></span>

### <span data-ttu-id="55b26-105">UpdateBlueprintAssignment (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55b26-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55b26-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="55b26-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55b26-107">DESCRIPTION</span></span>
<span data-ttu-id="55b26-108">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="55b26-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="55b26-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55b26-109">EXAMPLES</span></span>

### <span data-ttu-id="55b26-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55b26-110">Example 1</span></span>
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

<span data-ttu-id="55b26-111">Aggiornare l'assegnazione di un modello esistente della definizione del progetto `$blueprintObject` all'interno della sottoscrizione specificata, aggiornando i parametri.</span><span class="sxs-lookup"><span data-stu-id="55b26-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="55b26-112">Usa l'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="55b26-112">Uses system-assigned identity.</span></span> <span data-ttu-id="55b26-113">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="55b26-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="55b26-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="55b26-114">Example 2</span></span>
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

<span data-ttu-id="55b26-115">Aggiornare un'attività di progetto esistente tramite un file di assegnazione.</span><span class="sxs-lookup"><span data-stu-id="55b26-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="55b26-116">Il formato del file di assegnazione può essere trovato negli esempi di richiesta/risposta in: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="55b26-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="55b26-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="55b26-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="55b26-118">Aggiornare un'assegnazione di modello esistente della definizione del modello `$blueprintObject` destinata alla sottoscrizione specificata nel gruppo di gestione specificato usando il parametro defined.</span><span class="sxs-lookup"><span data-stu-id="55b26-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="55b26-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55b26-119">PARAMETERS</span></span>

### <span data-ttu-id="55b26-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="55b26-120">-AssignmentFile</span></span>
<span data-ttu-id="55b26-121">Posizione del file di assegnazione in formato JSON su disco.</span><span class="sxs-lookup"><span data-stu-id="55b26-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="55b26-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="55b26-122">-Blueprint</span></span>
<span data-ttu-id="55b26-123">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="55b26-123">Blueprint object.</span></span>

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

### <span data-ttu-id="55b26-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b26-124">-DefaultProfile</span></span>
<span data-ttu-id="55b26-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55b26-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b26-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="55b26-126">-Location</span></span>
<span data-ttu-id="55b26-127">Area geografica in cui creare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="55b26-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="55b26-128">Altre informazioni su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="55b26-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="55b26-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="55b26-129">-Lock</span></span>
<span data-ttu-id="55b26-130">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="55b26-130">Lock resources.</span></span>
<span data-ttu-id="55b26-131">Altre informazioni su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="55b26-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="55b26-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="55b26-132">-ManagementGroupId</span></span>
<span data-ttu-id="55b26-133">ID del gruppo di gestione in cui verranno salvate le assegnazioni cianografiche.</span><span class="sxs-lookup"><span data-stu-id="55b26-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="55b26-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="55b26-134">-Name</span></span>
<span data-ttu-id="55b26-135">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="55b26-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="55b26-136">Parametro-</span><span class="sxs-lookup"><span data-stu-id="55b26-136">-Parameter</span></span>
<span data-ttu-id="55b26-137">Parametro dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="55b26-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="55b26-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="55b26-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="55b26-139">Hashtable di parametri da passare all'elemento del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55b26-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="55b26-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="55b26-140">-SecureStringParameter</span></span>
<span data-ttu-id="55b26-141">Parametro stringa sicuro per l'ID risorsa, il nome e la versione di Resource Vault.</span><span class="sxs-lookup"><span data-stu-id="55b26-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="55b26-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55b26-142">-SubscriptionId</span></span>
<span data-ttu-id="55b26-143">SubscriptionId per assegnare la cianografia.</span><span class="sxs-lookup"><span data-stu-id="55b26-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="55b26-144">Può essere un elenco delimitato da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="55b26-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="55b26-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="55b26-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="55b26-146">Identità di sistema assegnata (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="55b26-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="55b26-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="55b26-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="55b26-148">Identità assegnata dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="55b26-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="55b26-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55b26-149">-Confirm</span></span>
<span data-ttu-id="55b26-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b26-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b26-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b26-151">-WhatIf</span></span>
<span data-ttu-id="55b26-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55b26-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b26-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55b26-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b26-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b26-154">CommonParameters</span></span>
<span data-ttu-id="55b26-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b26-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b26-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55b26-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b26-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55b26-157">INPUTS</span></span>

### <span data-ttu-id="55b26-158">System. String</span><span class="sxs-lookup"><span data-stu-id="55b26-158">System.String</span></span>

### <span data-ttu-id="55b26-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="55b26-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="55b26-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="55b26-160">System.String[]</span></span>

### <span data-ttu-id="55b26-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55b26-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55b26-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55b26-162">OUTPUTS</span></span>

### <span data-ttu-id="55b26-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="55b26-163">System.Object</span></span>
## <span data-ttu-id="55b26-164">Note</span><span class="sxs-lookup"><span data-stu-id="55b26-164">NOTES</span></span>

## <span data-ttu-id="55b26-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55b26-165">RELATED LINKS</span></span>
