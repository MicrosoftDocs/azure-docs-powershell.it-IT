---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852282"
---
# <span data-ttu-id="4e4dc-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="4e4dc-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="4e4dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4dc-103">Assegnare una definizione Blueprint a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="4e4dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e4dc-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e4dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4dc-106">Assegnare una definizione Blueprint a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="4e4dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="4e4dc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e4dc-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="4e4dc-109">Creare una nuova assegnazione Blueprint della definizione del modello `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario definito per il parametro e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="4e4dc-110">Usa l'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-110">Uses system-assigned identity.</span></span> <span data-ttu-id="4e4dc-111">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="4e4dc-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4e4dc-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="4e4dc-113">Creare una nuova assegnazione Blueprint della definizione Blueprint `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario dei parametri e del gruppo di risorse definito e configurando il blocco delle risorse in **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="4e4dc-114">Il valore predefinito è l'utilizzo dell'identità assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="4e4dc-115">La posizione definisce l'area geografica per la creazione dell'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="4e4dc-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4e4dc-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="4e4dc-117">Crea una nuova assegnazione Blueprint della definizione Blueprint `$blueprintObject` all'interno della sottoscrizione specificata usando il dizionario definito per il parametro e il gruppo di risorse usando l'ID identità assegnato dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="4e4dc-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e4dc-118">PARAMETERS</span></span>

### <span data-ttu-id="4e4dc-119">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="4e4dc-119">-Blueprint</span></span>
<span data-ttu-id="4e4dc-120">Oggetto definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="4e4dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4dc-121">-DefaultProfile</span></span>
<span data-ttu-id="4e4dc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4dc-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4e4dc-123">-Location</span></span>
<span data-ttu-id="4e4dc-124">Area geografica in cui creare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="4e4dc-125">Altre informazioni su aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="4e4dc-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="4e4dc-126">-Lock</span><span class="sxs-lookup"><span data-stu-id="4e4dc-126">-Lock</span></span>
<span data-ttu-id="4e4dc-127">Bloccare le risorse.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-127">Lock resources.</span></span>
<span data-ttu-id="4e4dc-128">Altre informazioni su aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="4e4dc-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="4e4dc-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e4dc-129">-Name</span></span>
<span data-ttu-id="4e4dc-130">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="4e4dc-131">Parametro-</span><span class="sxs-lookup"><span data-stu-id="4e4dc-131">-Parameter</span></span>
<span data-ttu-id="4e4dc-132">Parametri degli elementi.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="4e4dc-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="4e4dc-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="4e4dc-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="4e4dc-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="4e4dc-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="4e4dc-135">-SecureStringParameter</span></span>
<span data-ttu-id="4e4dc-136">Parametro stringa sicuro per l'ID risorsa, il nome e la versione di Resource Vault.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="4e4dc-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e4dc-137">-SubscriptionId</span></span>
<span data-ttu-id="4e4dc-138">ID abbonamento per assegnare la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="4e4dc-139">Può essere un elenco delimitato da virgole di stringhe subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="4e4dc-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4e4dc-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="4e4dc-141">Identità di sistema assegnata (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="4e4dc-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4e4dc-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="4e4dc-143">Identità assegnata dall'utente (MSI) per distribuire gli elementi.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="4e4dc-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e4dc-144">-Confirm</span></span>
<span data-ttu-id="4e4dc-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4dc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4dc-146">-WhatIf</span></span>
<span data-ttu-id="4e4dc-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4dc-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4dc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4dc-149">CommonParameters</span></span>
<span data-ttu-id="4e4dc-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4dc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4dc-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4dc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4dc-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e4dc-152">INPUTS</span></span>

### <span data-ttu-id="4e4dc-153">System. String</span><span class="sxs-lookup"><span data-stu-id="4e4dc-153">System.String</span></span>

### <span data-ttu-id="4e4dc-154">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="4e4dc-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="4e4dc-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="4e4dc-155">System.String[]</span></span>

### <span data-ttu-id="4e4dc-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e4dc-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e4dc-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e4dc-157">OUTPUTS</span></span>

### <span data-ttu-id="4e4dc-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e4dc-158">System.Object</span></span>
## <span data-ttu-id="4e4dc-159">Note</span><span class="sxs-lookup"><span data-stu-id="4e4dc-159">NOTES</span></span>

## <span data-ttu-id="4e4dc-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e4dc-160">RELATED LINKS</span></span>
