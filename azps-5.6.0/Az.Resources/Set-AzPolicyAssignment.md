---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: dcfc63c1dbf36cf7c592fe8fc7eb5afae09dc4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011773"
---
# <span data-ttu-id="e5b58-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b58-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="e5b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b58-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b58-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="e5b58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5b58-104">SYNTAX</span></span>

### <span data-ttu-id="e5b58-105">NameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e5b58-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5b58-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b58-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5b58-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5b58-112">DESCRIPTION</span></span>
<span data-ttu-id="e5b58-113">Il cmdlet **Set-AzPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="e5b58-114">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="e5b58-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="e5b58-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5b58-115">EXAMPLES</span></span>

### <span data-ttu-id="e5b58-116">Esempio 1: Aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="e5b58-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="e5b58-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="e5b58-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e5b58-118">Il comando archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5b58-119">Il secondo comando ottiene l'assegnazione dei criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="e5b58-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e5b58-120">Il comando archivia l'oggetto nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e5b58-121">Il comando finale aggiorna il nome visualizzato nell'assegnazione dei criteri nel gruppo di risorse identificato dalla proprietà **ResourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e5b58-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="e5b58-122">Esempio 2: Aggiungere un'identità gestita all'assegnazione dei criteri</span><span class="sxs-lookup"><span data-stu-id="e5b58-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="e5b58-123">Il primo comando recupera l'assegnazione dei criteri denominata PolicyAssignment dalla sottoscrizione corrente usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="e5b58-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e5b58-124">Il comando archivia l'oggetto nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e5b58-125">Il comando finale assegna un'identità gestita all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="e5b58-126">Esempio 3: Aggiornare i parametri di assegnazione dei criteri con un nuovo oggetto parametro dei criteri</span><span class="sxs-lookup"><span data-stu-id="e5b58-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="e5b58-127">Il primo e il secondo comando creano un oggetto contenente tutte le aree geografiche di Azure il cui nome inizia con "francia" o "uk".</span><span class="sxs-lookup"><span data-stu-id="e5b58-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="e5b58-128">Il secondo comando archivia l'oggetto nella $AllowedLocations variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="e5b58-129">Il terzo comando ottiene l'assegnazione di criteri denominata 'PolicyAssignment' Il comando archivia l'oggetto nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e5b58-130">Il comando finale aggiorna i valori dei parametri nell'assegnazione dei criteri denominata PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="e5b58-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="e5b58-131">Esempio 4: Aggiornare i parametri di assegnazione dei criteri con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="e5b58-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="e5b58-132">Creare un file denominato _AllowedLocations.jsfile_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="e5b58-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="e5b58-133">Il comando aggiorna l'assegnazione di criteri denominata "PolicyAssignment" usando il file AllowedLocations.jsdei parametri dei criteri dalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="e5b58-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="e5b58-134">Esempio 5: Aggiornare una enforcementMode</span><span class="sxs-lookup"><span data-stu-id="e5b58-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="e5b58-135">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup risorsa.</span><span class="sxs-lookup"><span data-stu-id="e5b58-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e5b58-136">Il comando archivia l'oggetto nella $ResourceGroup variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e5b58-137">Il secondo comando ottiene l'assegnazione dei criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="e5b58-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e5b58-138">Il comando archivia l'oggetto nella $PolicyAssignment variabile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e5b58-139">Il comando finale aggiorna la proprietà enforcementMode nell'assegnazione dei criteri nel gruppo di risorse identificato dalla **proprietà ResourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e5b58-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="e5b58-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b58-140">PARAMETERS</span></span>

### <span data-ttu-id="e5b58-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5b58-141">-ApiVersion</span></span>
<span data-ttu-id="e5b58-142">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e5b58-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5b58-143">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="e5b58-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e5b58-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e5b58-144">-AssignIdentity</span></span>
<span data-ttu-id="e5b58-145">Generare e assegnare un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="e5b58-146">L'identità verrà usata durante l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="e5b58-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="e5b58-147">Quando si assegna un'identità, è necessaria la posizione.</span><span class="sxs-lookup"><span data-stu-id="e5b58-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="e5b58-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b58-148">-DefaultProfile</span></span>
<span data-ttu-id="e5b58-149">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5b58-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5b58-150">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5b58-150">-Description</span></span>
<span data-ttu-id="e5b58-151">Descrizione per l'assegnazione dei criteri</span><span class="sxs-lookup"><span data-stu-id="e5b58-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="e5b58-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5b58-152">-DisplayName</span></span>
<span data-ttu-id="e5b58-153">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="e5b58-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="e5b58-154">-EnforcementMode</span></span>
<span data-ttu-id="e5b58-155">Modalità di applicazione dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="e5b58-156">Attualmente, i valori validi sono Default, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="e5b58-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="e5b58-157">-Id</span><span class="sxs-lookup"><span data-stu-id="e5b58-157">-Id</span></span>
<span data-ttu-id="e5b58-158">Specifica l'ID risorsa completo per l'assegnazione dei criteri modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b58-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b58-159">-InputObject</span></span>
<span data-ttu-id="e5b58-160">Oggetto di assegnazione dei criteri per aggiornare l'output di un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b58-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-161">-Location</span><span class="sxs-lookup"><span data-stu-id="e5b58-161">-Location</span></span>
<span data-ttu-id="e5b58-162">Posizione dell'identità della risorsa dell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="e5b58-163">È obbligatorio quando si usa l'opzione -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="e5b58-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="e5b58-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e5b58-164">-Metadata</span></span>
<span data-ttu-id="e5b58-165">Metadati aggiornati per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="e5b58-166">Può trattarsi del percorso di un nome file contenente i metadati o dei metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="e5b58-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e5b58-167">-Name</span><span class="sxs-lookup"><span data-stu-id="e5b58-167">-Name</span></span>
<span data-ttu-id="e5b58-168">Specifica il nome dell'assegnazione di criteri modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b58-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="e5b58-169">-NotScope</span></span>
<span data-ttu-id="e5b58-170">L'assegnazione dei criteri non ha ambiti.</span><span class="sxs-lookup"><span data-stu-id="e5b58-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="e5b58-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="e5b58-171">-PolicyParameter</span></span>
<span data-ttu-id="e5b58-172">Percorso file o stringa del nuovo parametro dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="e5b58-173">-PolicyParameterObject</span></span>
<span data-ttu-id="e5b58-174">Nuovo oggetto parametri dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e5b58-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5b58-175">-Pre</span></span>
<span data-ttu-id="e5b58-176">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e5b58-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5b58-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="e5b58-177">-Scope</span></span>
<span data-ttu-id="e5b58-178">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="e5b58-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b58-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b58-179">CommonParameters</span></span>
<span data-ttu-id="e5b58-180">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b58-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b58-181">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5b58-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b58-182">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5b58-182">INPUTS</span></span>

### <span data-ttu-id="e5b58-183">System.String</span><span class="sxs-lookup"><span data-stu-id="e5b58-183">System.String</span></span>

### <span data-ttu-id="e5b58-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e5b58-184">System.String[]</span></span>

## <span data-ttu-id="e5b58-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5b58-185">OUTPUTS</span></span>

### <span data-ttu-id="e5b58-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5b58-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5b58-187">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5b58-187">NOTES</span></span>

## <span data-ttu-id="e5b58-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5b58-188">RELATED LINKS</span></span>

[<span data-ttu-id="e5b58-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b58-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="e5b58-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b58-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="e5b58-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e5b58-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


