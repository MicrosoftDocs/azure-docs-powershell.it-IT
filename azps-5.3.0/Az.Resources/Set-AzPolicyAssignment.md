---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487163"
---
# <span data-ttu-id="9b81b-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9b81b-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="9b81b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b81b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b81b-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="9b81b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b81b-104">SYNTAX</span></span>

### <span data-ttu-id="9b81b-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b81b-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b81b-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b81b-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b81b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b81b-112">DESCRIPTION</span></span>
<span data-ttu-id="9b81b-113">Il cmdlet **set-AzPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="9b81b-114">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="9b81b-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="9b81b-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b81b-115">EXAMPLES</span></span>

### <span data-ttu-id="9b81b-116">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="9b81b-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="9b81b-117">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9b81b-118">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9b81b-119">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="9b81b-120">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9b81b-121">Il comando finale aggiorna il nome visualizzato nell'assegnazione dei criteri nel gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="9b81b-122">Esempio 2: aggiungere un'identità gestita all'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="9b81b-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="9b81b-123">Il primo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment dalla sottoscrizione corrente tramite il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="9b81b-124">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9b81b-125">Il comando finale assegna un'identità gestita all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="9b81b-126">Esempio 3: aggiornare i parametri delle assegnazioni dei criteri con un nuovo oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="9b81b-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="9b81b-127">Il primo e il secondo comando creano un oggetto contenente tutte le aree di Azure i cui nomi iniziano con "France" o "UK".</span><span class="sxs-lookup"><span data-stu-id="9b81b-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="9b81b-128">Il secondo comando Archivia l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="9b81b-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="9b81b-129">Il terzo comando ottiene l'assegnazione di criteri denominata "PolicyAssignment" il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9b81b-130">Il comando finale aggiorna i valori dei parametri nell'assegnazione dei criteri denominata PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="9b81b-131">Esempio 4: aggiornare i parametri delle assegnazioni dei criteri con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="9b81b-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="9b81b-132">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="9b81b-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="9b81b-133">Il comando Aggiorna l'assegnazione dei criteri denominata "PolicyAssignment" usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="9b81b-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="9b81b-134">Esempio 5: aggiornare un enforcementMode</span><span class="sxs-lookup"><span data-stu-id="9b81b-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="9b81b-135">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9b81b-136">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="9b81b-137">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="9b81b-138">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="9b81b-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="9b81b-139">Il comando finale aggiorna la proprietà enforcementMode per l'assegnazione di criteri nel gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b81b-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="9b81b-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b81b-140">PARAMETERS</span></span>

### <span data-ttu-id="9b81b-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9b81b-141">-ApiVersion</span></span>
<span data-ttu-id="9b81b-142">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9b81b-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9b81b-143">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="9b81b-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9b81b-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9b81b-144">-AssignIdentity</span></span>
<span data-ttu-id="9b81b-145">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="9b81b-146">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="9b81b-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="9b81b-147">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="9b81b-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="9b81b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b81b-148">-DefaultProfile</span></span>
<span data-ttu-id="9b81b-149">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b81b-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b81b-150">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b81b-150">-Description</span></span>
<span data-ttu-id="9b81b-151">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="9b81b-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="9b81b-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9b81b-152">-DisplayName</span></span>
<span data-ttu-id="9b81b-153">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="9b81b-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="9b81b-154">-EnforcementMode</span></span>
<span data-ttu-id="9b81b-155">Modalità di applicazione per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="9b81b-156">Attualmente i valori validi sono predefiniti, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="9b81b-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="9b81b-157">-ID</span><span class="sxs-lookup"><span data-stu-id="9b81b-157">-Id</span></span>
<span data-ttu-id="9b81b-158">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9b81b-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b81b-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b81b-159">-InputObject</span></span>
<span data-ttu-id="9b81b-160">L'oggetto assegnazione dei criteri da aggiornare che è stato restituito da un altro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b81b-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="9b81b-161">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9b81b-161">-Location</span></span>
<span data-ttu-id="9b81b-162">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="9b81b-163">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="9b81b-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="9b81b-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9b81b-164">-Metadata</span></span>
<span data-ttu-id="9b81b-165">Metadati aggiornati per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="9b81b-166">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="9b81b-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="9b81b-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b81b-167">-Name</span></span>
<span data-ttu-id="9b81b-168">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9b81b-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b81b-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="9b81b-169">-NotScope</span></span>
<span data-ttu-id="9b81b-170">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="9b81b-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="9b81b-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="9b81b-171">-PolicyParameter</span></span>
<span data-ttu-id="9b81b-172">Il percorso del file o la stringa del nuovo parametro dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="9b81b-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="9b81b-173">-PolicyParameterObject</span></span>
<span data-ttu-id="9b81b-174">Nuovo oggetto parametri dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9b81b-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="9b81b-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="9b81b-175">-Pre</span></span>
<span data-ttu-id="9b81b-176">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9b81b-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9b81b-177">-Ambito</span><span class="sxs-lookup"><span data-stu-id="9b81b-177">-Scope</span></span>
<span data-ttu-id="9b81b-178">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="9b81b-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="9b81b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b81b-179">CommonParameters</span></span>
<span data-ttu-id="9b81b-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b81b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b81b-181">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b81b-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b81b-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b81b-182">INPUTS</span></span>

### <span data-ttu-id="9b81b-183">System. String</span><span class="sxs-lookup"><span data-stu-id="9b81b-183">System.String</span></span>

### <span data-ttu-id="9b81b-184">System. String []</span><span class="sxs-lookup"><span data-stu-id="9b81b-184">System.String[]</span></span>

## <span data-ttu-id="9b81b-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b81b-185">OUTPUTS</span></span>

### <span data-ttu-id="9b81b-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9b81b-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9b81b-187">Note</span><span class="sxs-lookup"><span data-stu-id="9b81b-187">NOTES</span></span>

## <span data-ttu-id="9b81b-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b81b-188">RELATED LINKS</span></span>

[<span data-ttu-id="9b81b-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9b81b-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="9b81b-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9b81b-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="9b81b-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="9b81b-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


