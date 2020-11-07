---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856321"
---
# <span data-ttu-id="b1a87-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1a87-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="b1a87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1a87-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a87-103">Modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="b1a87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1a87-104">SYNTAX</span></span>

### <span data-ttu-id="b1a87-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1a87-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a87-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a87-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1a87-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a87-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a87-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a87-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a87-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a87-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a87-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1a87-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a87-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1a87-111">DESCRIPTION</span></span>
<span data-ttu-id="b1a87-112">Il cmdlet **set-AzPolicyAssignment** modifica un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="b1a87-113">Specificare un'assegnazione in base all'ID o al nome e all'ambito.</span><span class="sxs-lookup"><span data-stu-id="b1a87-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="b1a87-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1a87-114">EXAMPLES</span></span>

### <span data-ttu-id="b1a87-115">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="b1a87-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="b1a87-116">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b1a87-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b1a87-117">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b1a87-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b1a87-118">Il secondo comando ottiene l'assegnazione di criteri denominata PolicyAssignment usando il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b1a87-119">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b1a87-120">Il comando finale aggiorna il nome visualizzato nell'assegnazione dei criteri nel gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b1a87-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b1a87-121">Esempio 2: aggiungere un'identità gestita all'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="b1a87-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="b1a87-122">Il primo comando consente di ottenere l'assegnazione di criteri denominata PolicyAssignment dalla sottoscrizione corrente tramite il cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b1a87-123">Il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b1a87-124">Il comando finale assegna un'identità gestita all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="b1a87-125">Esempio 3: aggiornare i parametri delle assegnazioni dei criteri con un nuovo oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="b1a87-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="b1a87-126">Il primo e il secondo comando creano un oggetto contenente tutte le aree di Azure i cui nomi iniziano con "France" o "UK".</span><span class="sxs-lookup"><span data-stu-id="b1a87-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="b1a87-127">Il secondo comando Archivia l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="b1a87-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="b1a87-128">Il terzo comando ottiene l'assegnazione di criteri denominata "PolicyAssignment" il comando Archivia l'oggetto nella variabile $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b1a87-129">Il comando finale aggiorna i valori dei parametri nell'assegnazione dei criteri denominata PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="b1a87-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="b1a87-130">Esempio 4: aggiornare i parametri delle assegnazioni dei criteri con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="b1a87-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="b1a87-131">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="b1a87-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="b1a87-132">Il comando Aggiorna l'assegnazione dei criteri denominata "PolicyAssignment" usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="b1a87-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="b1a87-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1a87-133">PARAMETERS</span></span>

### <span data-ttu-id="b1a87-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1a87-134">-ApiVersion</span></span>
<span data-ttu-id="b1a87-135">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b1a87-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1a87-136">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="b1a87-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b1a87-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b1a87-137">-AssignIdentity</span></span>
<span data-ttu-id="b1a87-138">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b1a87-139">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="b1a87-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b1a87-140">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="b1a87-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b1a87-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a87-141">-DefaultProfile</span></span>
<span data-ttu-id="b1a87-142">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b1a87-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1a87-143">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1a87-143">-Description</span></span>
<span data-ttu-id="b1a87-144">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="b1a87-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="b1a87-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b1a87-145">-DisplayName</span></span>
<span data-ttu-id="b1a87-146">Specifica un nuovo nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b1a87-147">-ID</span><span class="sxs-lookup"><span data-stu-id="b1a87-147">-Id</span></span>
<span data-ttu-id="b1a87-148">Specifica l'ID di risorsa completo per l'assegnazione di criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b1a87-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b1a87-149">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b1a87-149">-Location</span></span>
<span data-ttu-id="b1a87-150">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b1a87-151">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="b1a87-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="b1a87-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b1a87-152">-Metadata</span></span>
<span data-ttu-id="b1a87-153">Metadati aggiornati per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="b1a87-154">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="b1a87-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="b1a87-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1a87-155">-Name</span></span>
<span data-ttu-id="b1a87-156">Specifica il nome dell'assegnazione dei criteri che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b1a87-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b1a87-157">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b1a87-157">-NotScope</span></span>
<span data-ttu-id="b1a87-158">L'assegnazione dei criteri non è ambiti.</span><span class="sxs-lookup"><span data-stu-id="b1a87-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="b1a87-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b1a87-159">-PolicyParameter</span></span>
<span data-ttu-id="b1a87-160">Il percorso del file o la stringa del nuovo parametro dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="b1a87-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b1a87-161">-PolicyParameterObject</span></span>
<span data-ttu-id="b1a87-162">Nuovo oggetto parametri dei criteri per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="b1a87-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="b1a87-163">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1a87-163">-Pre</span></span>
<span data-ttu-id="b1a87-164">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b1a87-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b1a87-165">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b1a87-165">-Scope</span></span>
<span data-ttu-id="b1a87-166">Specifica l'ambito in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="b1a87-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="b1a87-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a87-167">CommonParameters</span></span>
<span data-ttu-id="b1a87-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a87-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a87-169">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1a87-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a87-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1a87-170">INPUTS</span></span>

### <span data-ttu-id="b1a87-171">System. String</span><span class="sxs-lookup"><span data-stu-id="b1a87-171">System.String</span></span>

### <span data-ttu-id="b1a87-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="b1a87-172">System.String[]</span></span>

## <span data-ttu-id="b1a87-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1a87-173">OUTPUTS</span></span>

### <span data-ttu-id="b1a87-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b1a87-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b1a87-175">Note</span><span class="sxs-lookup"><span data-stu-id="b1a87-175">NOTES</span></span>

## <span data-ttu-id="b1a87-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1a87-176">RELATED LINKS</span></span>

[<span data-ttu-id="b1a87-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1a87-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b1a87-178">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1a87-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="b1a87-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1a87-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


