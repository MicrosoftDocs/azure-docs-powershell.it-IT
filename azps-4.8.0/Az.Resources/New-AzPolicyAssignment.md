---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189386"
---
# <span data-ttu-id="91a52-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="91a52-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="91a52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91a52-102">SYNOPSIS</span></span>
<span data-ttu-id="91a52-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="91a52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91a52-104">SYNTAX</span></span>

### <span data-ttu-id="91a52-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91a52-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a52-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a52-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a52-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a52-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a52-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a52-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91a52-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a52-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91a52-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a52-110">DESCRIPTION</span></span>
<span data-ttu-id="91a52-111">Il cmdlet **New-AzPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="91a52-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="91a52-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="91a52-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91a52-113">EXAMPLES</span></span>

### <span data-ttu-id="91a52-114">Esempio 1: assegnazione dei criteri a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="91a52-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="91a52-115">Il primo comando ottiene un abbonamento denominato Subscription01 usando il cmdlet Get-AzSubscription e lo archivia nella variabile $Subscription.</span><span class="sxs-lookup"><span data-stu-id="91a52-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="91a52-116">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="91a52-117">Il comando finale assegna il criterio in $Policy al livello dell'abbonamento identificato dalla stringa dell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="91a52-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="91a52-118">Esempio 2: assegnazione dei criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="91a52-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="91a52-119">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="91a52-120">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="91a52-121">Il comando finale assegna il criterio in $Policy a livello di gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="91a52-122">Esempio 3: assegnazione dei criteri a livello di gruppo di risorse con l'oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="91a52-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="91a52-123">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="91a52-124">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="91a52-125">Il secondo comando consente di ottenere la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="91a52-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="91a52-126">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="91a52-127">Il terzo e il quarto comando creano un oggetto contenente tutte le aree di Azure con "East" nel nome.</span><span class="sxs-lookup"><span data-stu-id="91a52-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="91a52-128">I comandi archiviano l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="91a52-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="91a52-129">Il comando finale assegna i criteri in $Policy a livello di un gruppo di risorse usando l'oggetto Parameter Policy in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="91a52-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="91a52-130">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91a52-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="91a52-131">Esempio 4: assegnazione dei criteri a livello di gruppo di risorse con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="91a52-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="91a52-132">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="91a52-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="91a52-133">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="91a52-134">Il secondo comando ottiene la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="91a52-135">Il comando finale assegna i criteri in $Policy al gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="91a52-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="91a52-136">Esempio 5: assegnazione di criteri con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="91a52-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="91a52-137">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="91a52-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="91a52-138">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="91a52-139">Il comando finale assegna il criterio in $Policy al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91a52-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="91a52-140">Un'identità gestita viene creata automaticamente e assegnata all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="91a52-141">Esempio 6: assegnazione di criteri con una proprietà modalità di applicazione</span><span class="sxs-lookup"><span data-stu-id="91a52-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="91a52-142">Il primo comando ottiene un abbonamento denominato Subscription01 usando il cmdlet Get-AzSubscription e lo archivia nella variabile $Subscription.</span><span class="sxs-lookup"><span data-stu-id="91a52-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="91a52-143">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="91a52-144">Il comando finale assegna il criterio in $Policy al livello dell'abbonamento identificato dalla stringa dell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="91a52-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="91a52-145">L'assegnazione viene impostata con un valore EnforcementMode di _DoNotEnforce_ , ossia l'effetto dei criteri non viene applicato durante la creazione o l'aggiornamento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="91a52-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="91a52-146">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91a52-146">PARAMETERS</span></span>

### <span data-ttu-id="91a52-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="91a52-147">-ApiVersion</span></span>
<span data-ttu-id="91a52-148">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="91a52-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="91a52-149">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="91a52-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="91a52-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="91a52-150">-AssignIdentity</span></span>
<span data-ttu-id="91a52-151">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="91a52-152">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="91a52-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="91a52-153">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="91a52-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="91a52-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a52-154">-DefaultProfile</span></span>
<span data-ttu-id="91a52-155">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="91a52-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91a52-156">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="91a52-156">-Description</span></span>
<span data-ttu-id="91a52-157">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="91a52-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="91a52-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="91a52-158">-DisplayName</span></span>
<span data-ttu-id="91a52-159">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="91a52-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="91a52-160">-EnforcementMode</span></span>
<span data-ttu-id="91a52-161">Modalità di applicazione per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="91a52-162">Attualmente i valori validi sono predefiniti, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="91a52-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="91a52-163">-Posizione</span><span class="sxs-lookup"><span data-stu-id="91a52-163">-Location</span></span>
<span data-ttu-id="91a52-164">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="91a52-165">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="91a52-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="91a52-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="91a52-166">-Metadata</span></span>
<span data-ttu-id="91a52-167">Metadati per la nuova assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="91a52-168">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="91a52-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="91a52-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="91a52-169">-Name</span></span>
<span data-ttu-id="91a52-170">Specifica un nome per l'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="91a52-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="91a52-171">-NotScope</span></span>
<span data-ttu-id="91a52-172">Gli ambiti non per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="91a52-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91a52-173">-PolicyDefinition</span></span>
<span data-ttu-id="91a52-174">Specifica un criterio, come oggetto **PsPolicyDefinition** che contiene la regola dei criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="91a52-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="91a52-175">-PolicyParameter</span></span>
<span data-ttu-id="91a52-176">Il percorso del file del parametro policy o la stringa del parametro Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="91a52-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="91a52-177">-PolicyParameterObject</span></span>
<span data-ttu-id="91a52-178">Oggetto Parameter. Policy.</span><span class="sxs-lookup"><span data-stu-id="91a52-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="91a52-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="91a52-179">-PolicySetDefinition</span></span>
<span data-ttu-id="91a52-180">Oggetto definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="91a52-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="91a52-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="91a52-181">-Pre</span></span>
<span data-ttu-id="91a52-182">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="91a52-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="91a52-183">-Ambito</span><span class="sxs-lookup"><span data-stu-id="91a52-183">-Scope</span></span>
<span data-ttu-id="91a52-184">Specifica l'ambito in cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="91a52-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="91a52-185">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare quanto segue: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="91a52-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="91a52-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a52-186">CommonParameters</span></span>
<span data-ttu-id="91a52-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a52-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a52-188">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91a52-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a52-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91a52-189">INPUTS</span></span>

### <span data-ttu-id="91a52-190">System. String</span><span class="sxs-lookup"><span data-stu-id="91a52-190">System.String</span></span>

### <span data-ttu-id="91a52-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="91a52-191">System.String[]</span></span>

### <span data-ttu-id="91a52-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="91a52-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="91a52-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91a52-193">OUTPUTS</span></span>

### <span data-ttu-id="91a52-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="91a52-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="91a52-195">Note</span><span class="sxs-lookup"><span data-stu-id="91a52-195">NOTES</span></span>

## <span data-ttu-id="91a52-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91a52-196">RELATED LINKS</span></span>

[<span data-ttu-id="91a52-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="91a52-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="91a52-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="91a52-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="91a52-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="91a52-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="91a52-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="91a52-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


