---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972638"
---
# <span data-ttu-id="f5482-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5482-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="f5482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5482-102">SYNOPSIS</span></span>
<span data-ttu-id="f5482-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="f5482-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5482-104">SYNTAX</span></span>

### <span data-ttu-id="f5482-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f5482-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5482-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5482-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5482-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5482-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5482-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5482-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5482-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5482-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5482-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5482-110">DESCRIPTION</span></span>
<span data-ttu-id="f5482-111">Il cmdlet **New-AzPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="f5482-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="f5482-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="f5482-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5482-113">EXAMPLES</span></span>

### <span data-ttu-id="f5482-114">Esempio 1: Assegnazione di criteri a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f5482-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="f5482-115">Il primo comando ottiene una sottoscrizione denominata Subscription01 usando il cmdlet Get-AzSubscription e la archivia nella $Subscription variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="f5482-116">Il secondo comando ottiene la definizione del criterio denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e la archivia nella variabile $Policy locale.</span><span class="sxs-lookup"><span data-stu-id="f5482-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5482-117">Il comando finale assegna i criteri in $Policy al livello della sottoscrizione identificato dalla stringa dell'ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f5482-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="f5482-118">Esempio 2: assegnazione di criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f5482-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="f5482-119">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5482-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5482-120">Il secondo comando ottiene la definizione del criterio denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e la archivia nella variabile $Policy locale.</span><span class="sxs-lookup"><span data-stu-id="f5482-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5482-121">Il comando finale assegna i criteri in $Policy al livello del gruppo di risorse identificato dalla proprietà **ResourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5482-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="f5482-122">Esempio 3: Assegnazione di criteri a livello di gruppo di risorse con oggetto parametro dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5482-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="f5482-123">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5482-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f5482-124">Il comando archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5482-125">Il secondo comando ottiene la definizione dei criteri predefiniti per le posizioni consentite usando il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f5482-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f5482-126">Il comando archivia l'oggetto nella $Policy variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="f5482-127">Il terzo e quarto comando creano un oggetto contenente tutte le aree geografiche di Azure il cui nome contiene "est".</span><span class="sxs-lookup"><span data-stu-id="f5482-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="f5482-128">I comandi archiviano l'oggetto nella $AllowedLocations variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="f5482-129">Il comando finale assegna i criteri in $Policy a livello di gruppo di risorse usando l'oggetto parametro dei criteri in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="f5482-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="f5482-130">La **proprietà ResourceId** dell'$ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5482-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f5482-131">Esempio 4: Assegnazione di criteri a livello di gruppo di risorse con file di parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5482-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="f5482-132">Creare un file denominato _AllowedLocations.jsfile_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="f5482-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="f5482-133">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5482-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5482-134">Il secondo comando ottiene la definizione dei criteri predefiniti per le posizioni consentite usando il cmdlet Get-AzPolicyDefinition e la archivia nella $Policy variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5482-135">Il comando finale assegna i criteri in $Policy al gruppo di risorse identificato dalla proprietà **ResourceId** di $ResourceGroup usando il file dei parametri dei criteri AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="f5482-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="f5482-136">Esempio 5: Assegnazione di criteri con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="f5482-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="f5482-137">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5482-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5482-138">Il secondo comando ottiene la definizione del criterio denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e la archivia nella variabile $Policy locale.</span><span class="sxs-lookup"><span data-stu-id="f5482-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5482-139">Il comando finale assegna il criterio in $Policy al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5482-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="f5482-140">Un'identità gestita viene creata e assegnata automaticamente all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="f5482-141">Esempio 6: Assegnazione di criteri con una proprietà modalità di applicazione</span><span class="sxs-lookup"><span data-stu-id="f5482-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="f5482-142">Il primo comando ottiene una sottoscrizione denominata Subscription01 usando il cmdlet Get-AzSubscription e la archivia nella $Subscription variabile.</span><span class="sxs-lookup"><span data-stu-id="f5482-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="f5482-143">Il secondo comando ottiene la definizione del criterio denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e la archivia nella variabile $Policy locale.</span><span class="sxs-lookup"><span data-stu-id="f5482-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5482-144">Il comando finale assegna i criteri in $Policy al livello della sottoscrizione identificato dalla stringa dell'ambito di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f5482-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="f5482-145">L'assegnazione viene impostata con un valore EnforcementMode di _DoNotEnforce,_ ad esempio l'effetto del criterio non viene applicato durante la creazione o l'aggiornamento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f5482-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="f5482-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5482-146">PARAMETERS</span></span>

### <span data-ttu-id="f5482-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5482-147">-ApiVersion</span></span>
<span data-ttu-id="f5482-148">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f5482-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5482-149">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="f5482-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f5482-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f5482-150">-AssignIdentity</span></span>
<span data-ttu-id="f5482-151">Generare e assegnare un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="f5482-152">L'identità verrà usata durante l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="f5482-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="f5482-153">Quando si assegna un'identità, è necessaria la posizione.</span><span class="sxs-lookup"><span data-stu-id="f5482-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="f5482-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5482-154">-DefaultProfile</span></span>
<span data-ttu-id="f5482-155">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f5482-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5482-156">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5482-156">-Description</span></span>
<span data-ttu-id="f5482-157">Descrizione per l'assegnazione dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5482-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="f5482-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f5482-158">-DisplayName</span></span>
<span data-ttu-id="f5482-159">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="f5482-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="f5482-160">-EnforcementMode</span></span>
<span data-ttu-id="f5482-161">Modalità di applicazione dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="f5482-162">Attualmente, i valori validi sono Default, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="f5482-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5482-163">-Location</span><span class="sxs-lookup"><span data-stu-id="f5482-163">-Location</span></span>
<span data-ttu-id="f5482-164">Posizione dell'identità della risorsa dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="f5482-165">È obbligatorio quando si usa l'opzione -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="f5482-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="f5482-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f5482-166">-Metadata</span></span>
<span data-ttu-id="f5482-167">Metadati per la nuova assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="f5482-168">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="f5482-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="f5482-169">-Name</span><span class="sxs-lookup"><span data-stu-id="f5482-169">-Name</span></span>
<span data-ttu-id="f5482-170">Specifica un nome per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="f5482-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f5482-171">-NotScope</span></span>
<span data-ttu-id="f5482-172">Gli ambiti Not per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="f5482-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5482-173">-PolicyDefinition</span></span>
<span data-ttu-id="f5482-174">Specifica un criterio, come oggetto **PsPolicyDefinition** che contiene la regola del criterio.</span><span class="sxs-lookup"><span data-stu-id="f5482-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5482-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="f5482-175">-PolicyParameter</span></span>
<span data-ttu-id="f5482-176">Percorso del file dei parametri dei criteri o stringa del parametro dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5482-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="f5482-177">-PolicyParameterObject</span></span>
<span data-ttu-id="f5482-178">Oggetto parametro dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5482-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f5482-179">-PolicySetDefinition</span></span>
<span data-ttu-id="f5482-180">Oggetto definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5482-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5482-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5482-181">-Pre</span></span>
<span data-ttu-id="f5482-182">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f5482-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5482-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="f5482-183">-Scope</span></span>
<span data-ttu-id="f5482-184">Specifica l'ambito a cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="f5482-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="f5482-185">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare il nome seguente: `/subscriptions/` ID sottoscrizione del gruppo di `/resourcegroups/` risorse</span><span class="sxs-lookup"><span data-stu-id="f5482-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="f5482-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5482-186">CommonParameters</span></span>
<span data-ttu-id="f5482-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5482-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5482-188">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5482-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5482-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5482-189">INPUTS</span></span>

### <span data-ttu-id="f5482-190">System.String</span><span class="sxs-lookup"><span data-stu-id="f5482-190">System.String</span></span>

### <span data-ttu-id="f5482-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f5482-191">System.String[]</span></span>

### <span data-ttu-id="f5482-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f5482-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5482-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5482-193">OUTPUTS</span></span>

### <span data-ttu-id="f5482-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f5482-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5482-195">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5482-195">NOTES</span></span>

## <span data-ttu-id="f5482-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5482-196">RELATED LINKS</span></span>

[<span data-ttu-id="f5482-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5482-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f5482-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5482-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="f5482-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5482-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="f5482-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5482-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


