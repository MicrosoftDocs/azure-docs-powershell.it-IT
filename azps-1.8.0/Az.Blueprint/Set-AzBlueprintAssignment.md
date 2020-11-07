---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852286"
---
# <span data-ttu-id="e06bb-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e06bb-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e06bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e06bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e06bb-103">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="e06bb-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e06bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e06bb-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e06bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e06bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e06bb-106">Aggiornare un'assegnazione di modello esistente.</span><span class="sxs-lookup"><span data-stu-id="e06bb-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e06bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e06bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e06bb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e06bb-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="e06bb-109">Aggiornare l'assegnazione di un modello esistente della definizione del progetto `$blueprintObject` all'interno della sottoscrizione specificata, aggiornando i parametri.</span><span class="sxs-lookup"><span data-stu-id="e06bb-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="e06bb-110">Usa l'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e06bb-110">Uses system-assigned identity.</span></span> <span data-ttu-id="e06bb-111">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="e06bb-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="e06bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e06bb-112">PARAMETERS</span></span>

### <span data-ttu-id="e06bb-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e06bb-113">-Blueprint</span></span>
<span data-ttu-id="e06bb-114">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e06bb-114">Blueprint object.</span></span>

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

### <span data-ttu-id="e06bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e06bb-115">-DefaultProfile</span></span>
<span data-ttu-id="e06bb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e06bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e06bb-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e06bb-117">-Location</span></span>
<span data-ttu-id="e06bb-118">Area geografica in cui creare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="e06bb-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e06bb-119">Altre informazioni su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e06bb-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e06bb-120">-Lock</span><span class="sxs-lookup"><span data-stu-id="e06bb-120">-Lock</span></span>
<span data-ttu-id="e06bb-121">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="e06bb-121">Lock resources.</span></span>
<span data-ttu-id="e06bb-122">Altre informazioni su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e06bb-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e06bb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e06bb-123">-Name</span></span>
<span data-ttu-id="e06bb-124">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="e06bb-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e06bb-125">Parametro-</span><span class="sxs-lookup"><span data-stu-id="e06bb-125">-Parameter</span></span>
<span data-ttu-id="e06bb-126">Parametro dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e06bb-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="e06bb-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e06bb-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="e06bb-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="e06bb-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="e06bb-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e06bb-129">-SecureStringParameter</span></span>
<span data-ttu-id="e06bb-130">Parametro stringa sicuro per l'ID risorsa, il nome e la versione di Resource Vault.</span><span class="sxs-lookup"><span data-stu-id="e06bb-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e06bb-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e06bb-131">-SubscriptionId</span></span>
<span data-ttu-id="e06bb-132">SubscriptionId per assegnare la cianografia.</span><span class="sxs-lookup"><span data-stu-id="e06bb-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="e06bb-133">Può essere un elenco delimitato da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="e06bb-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e06bb-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e06bb-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e06bb-135">Identità di sistema assegnata (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="e06bb-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e06bb-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e06bb-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="e06bb-137">Identità assegnata dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="e06bb-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e06bb-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e06bb-138">-Confirm</span></span>
<span data-ttu-id="e06bb-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e06bb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e06bb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e06bb-140">-WhatIf</span></span>
<span data-ttu-id="e06bb-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e06bb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e06bb-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e06bb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e06bb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e06bb-143">CommonParameters</span></span>
<span data-ttu-id="e06bb-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e06bb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e06bb-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e06bb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e06bb-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e06bb-146">INPUTS</span></span>

### <span data-ttu-id="e06bb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e06bb-147">System.String</span></span>

### <span data-ttu-id="e06bb-148">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e06bb-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e06bb-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="e06bb-149">System.String[]</span></span>

### <span data-ttu-id="e06bb-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e06bb-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e06bb-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e06bb-151">OUTPUTS</span></span>

### <span data-ttu-id="e06bb-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="e06bb-152">System.Object</span></span>
## <span data-ttu-id="e06bb-153">Note</span><span class="sxs-lookup"><span data-stu-id="e06bb-153">NOTES</span></span>

## <span data-ttu-id="e06bb-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e06bb-154">RELATED LINKS</span></span>
