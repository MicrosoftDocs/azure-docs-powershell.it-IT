---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018944"
---
# <span data-ttu-id="2a58a-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="2a58a-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="2a58a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a58a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a58a-103">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="2a58a-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2a58a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a58a-104">SYNTAX</span></span>

### <span data-ttu-id="2a58a-105">UpdateBlueprintAssignment (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a58a-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a58a-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="2a58a-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a58a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a58a-107">DESCRIPTION</span></span>
<span data-ttu-id="2a58a-108">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="2a58a-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="2a58a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a58a-109">EXAMPLES</span></span>

### <span data-ttu-id="2a58a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a58a-110">Example 1</span></span>
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

<span data-ttu-id="2a58a-111">Aggiornare l'assegnazione di un modello esistente della definizione del progetto `$blueprintObject` all'interno della sottoscrizione specificata, aggiornando i parametri.</span><span class="sxs-lookup"><span data-stu-id="2a58a-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="2a58a-112">Usa l'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2a58a-112">Uses system-assigned identity.</span></span> <span data-ttu-id="2a58a-113">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="2a58a-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="2a58a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2a58a-114">Example 2</span></span>
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

<span data-ttu-id="2a58a-115">Aggiornare un'attività di progetto esistente tramite un file di assegnazione.</span><span class="sxs-lookup"><span data-stu-id="2a58a-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="2a58a-116">Il formato del file di assegnazione può essere trovato negli esempi di richiesta/risposta in: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="2a58a-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="2a58a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a58a-117">PARAMETERS</span></span>

### <span data-ttu-id="2a58a-118">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="2a58a-118">-Blueprint</span></span>
<span data-ttu-id="2a58a-119">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="2a58a-119">Blueprint object.</span></span>

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

### <span data-ttu-id="2a58a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a58a-120">-DefaultProfile</span></span>
<span data-ttu-id="2a58a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a58a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a58a-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2a58a-122">-Location</span></span>
<span data-ttu-id="2a58a-123">Area geografica in cui creare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="2a58a-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="2a58a-124">Altre informazioni su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="2a58a-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="2a58a-125">-Lock</span><span class="sxs-lookup"><span data-stu-id="2a58a-125">-Lock</span></span>
<span data-ttu-id="2a58a-126">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="2a58a-126">Lock resources.</span></span>
<span data-ttu-id="2a58a-127">Altre informazioni su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="2a58a-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="2a58a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a58a-128">-Name</span></span>
<span data-ttu-id="2a58a-129">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="2a58a-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="2a58a-130">Parametro-</span><span class="sxs-lookup"><span data-stu-id="2a58a-130">-Parameter</span></span>
<span data-ttu-id="2a58a-131">Parametro dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2a58a-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="2a58a-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="2a58a-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="2a58a-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="2a58a-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="2a58a-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="2a58a-134">-SecureStringParameter</span></span>
<span data-ttu-id="2a58a-135">Parametro stringa sicuro per l'ID risorsa, il nome e la versione di Resource Vault.</span><span class="sxs-lookup"><span data-stu-id="2a58a-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="2a58a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a58a-136">-SubscriptionId</span></span>
<span data-ttu-id="2a58a-137">SubscriptionId per assegnare la cianografia.</span><span class="sxs-lookup"><span data-stu-id="2a58a-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="2a58a-138">Può essere un elenco delimitato da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2a58a-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="2a58a-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2a58a-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="2a58a-140">Identità di sistema assegnata (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="2a58a-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="2a58a-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2a58a-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="2a58a-142">Identità assegnata dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="2a58a-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a58a-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a58a-143">-Confirm</span></span>
<span data-ttu-id="2a58a-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a58a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a58a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a58a-145">-WhatIf</span></span>
<span data-ttu-id="2a58a-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a58a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a58a-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a58a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a58a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a58a-148">CommonParameters</span></span>
<span data-ttu-id="2a58a-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a58a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a58a-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a58a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a58a-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a58a-151">INPUTS</span></span>

### <span data-ttu-id="2a58a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2a58a-152">System.String</span></span>

### <span data-ttu-id="2a58a-153">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2a58a-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2a58a-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a58a-154">System.String[]</span></span>

### <span data-ttu-id="2a58a-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a58a-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a58a-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a58a-156">OUTPUTS</span></span>

### <span data-ttu-id="2a58a-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="2a58a-157">System.Object</span></span>
## <span data-ttu-id="2a58a-158">Note</span><span class="sxs-lookup"><span data-stu-id="2a58a-158">NOTES</span></span>

## <span data-ttu-id="2a58a-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a58a-159">RELATED LINKS</span></span>
