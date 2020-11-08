---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018594"
---
# <span data-ttu-id="7e654-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="7e654-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="7e654-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e654-102">SYNOPSIS</span></span>
<span data-ttu-id="7e654-103">Assegnare una definizione Blueprint a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e654-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="7e654-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e654-104">SYNTAX</span></span>

### <span data-ttu-id="7e654-105">CreateBlueprintAssignment (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e654-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e654-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="7e654-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e654-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e654-107">DESCRIPTION</span></span>
<span data-ttu-id="7e654-108">Assegnare una definizione Blueprint a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e654-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="7e654-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e654-109">EXAMPLES</span></span>

### <span data-ttu-id="7e654-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e654-110">Example 1</span></span>
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

<span data-ttu-id="7e654-111">Creare una nuova assegnazione Blueprint della definizione del modello `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario definito per il parametro e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e654-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="7e654-112">Usa l'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7e654-112">Uses system-assigned identity.</span></span> <span data-ttu-id="7e654-113">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="7e654-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="7e654-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e654-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="7e654-115">Creare una nuova assegnazione Blueprint della definizione Blueprint `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario dei parametri e del gruppo di risorse definito e configurando il blocco delle risorse in **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="7e654-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="7e654-116">Il valore predefinito è l'utilizzo dell'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7e654-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="7e654-117">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="7e654-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="7e654-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7e654-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="7e654-119">Crea una nuova assegnazione Blueprint della definizione Blueprint `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario definito per il parametro e il gruppo di risorse usando l'ID identità assegnato dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="7e654-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="7e654-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7e654-120">Example 4</span></span>
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

<span data-ttu-id="7e654-121">Creare un'attività Blueprint tramite un file di assegnazione.</span><span class="sxs-lookup"><span data-stu-id="7e654-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="7e654-122">Il formato del file di assegnazione può essere trovato negli esempi di richiesta/risposta in: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="7e654-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="7e654-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e654-123">PARAMETERS</span></span>

### <span data-ttu-id="7e654-124">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="7e654-124">-Blueprint</span></span>
<span data-ttu-id="7e654-125">Oggetto definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e654-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e654-126">-DefaultProfile</span></span>
<span data-ttu-id="7e654-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e654-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e654-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7e654-128">-Location</span></span>
<span data-ttu-id="7e654-129">Area geografica in cui creare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="7e654-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="7e654-130">Altre informazioni su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="7e654-130">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="7e654-131">-Lock</span></span>
<span data-ttu-id="7e654-132">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="7e654-132">Lock resources.</span></span>
<span data-ttu-id="7e654-133">Altre informazioni su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="7e654-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e654-134">-Name</span></span>
<span data-ttu-id="7e654-135">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="7e654-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-136">Parametro-</span><span class="sxs-lookup"><span data-stu-id="7e654-136">-Parameter</span></span>
<span data-ttu-id="7e654-137">Parametri degli elementi.</span><span class="sxs-lookup"><span data-stu-id="7e654-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="7e654-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="7e654-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="7e654-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="7e654-140">-SecureStringParameter</span></span>
<span data-ttu-id="7e654-141">Parametro stringa sicuro per l'ID risorsa, il nome e la versione di Resource Vault.</span><span class="sxs-lookup"><span data-stu-id="7e654-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e654-142">-SubscriptionId</span></span>
<span data-ttu-id="7e654-143">ID abbonamento per assegnare la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="7e654-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="7e654-144">Può essere un elenco delimitato da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="7e654-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e654-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7e654-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="7e654-146">Identità di sistema assegnata (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7e654-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="7e654-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7e654-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="7e654-148">Identità assegnata dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7e654-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="7e654-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e654-149">-Confirm</span></span>
<span data-ttu-id="7e654-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e654-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e654-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e654-151">-WhatIf</span></span>
<span data-ttu-id="7e654-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e654-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e654-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e654-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e654-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e654-154">CommonParameters</span></span>
<span data-ttu-id="7e654-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e654-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e654-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e654-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e654-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e654-157">INPUTS</span></span>

### <span data-ttu-id="7e654-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7e654-158">System.String</span></span>

### <span data-ttu-id="7e654-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="7e654-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="7e654-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="7e654-160">System.String[]</span></span>

### <span data-ttu-id="7e654-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e654-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e654-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e654-162">OUTPUTS</span></span>

### <span data-ttu-id="7e654-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="7e654-163">System.Object</span></span>
## <span data-ttu-id="7e654-164">Note</span><span class="sxs-lookup"><span data-stu-id="7e654-164">NOTES</span></span>

## <span data-ttu-id="7e654-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e654-165">RELATED LINKS</span></span>
