---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862498"
---
# <span data-ttu-id="c99cd-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c99cd-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="c99cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c99cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c99cd-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="c99cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c99cd-104">SYNTAX</span></span>

### <span data-ttu-id="c99cd-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c99cd-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c99cd-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99cd-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c99cd-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99cd-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c99cd-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99cd-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c99cd-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99cd-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c99cd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c99cd-110">DESCRIPTION</span></span>
<span data-ttu-id="c99cd-111">Il cmdlet **New-AzPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="c99cd-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="c99cd-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="c99cd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c99cd-113">EXAMPLES</span></span>

### <span data-ttu-id="c99cd-114">Esempio 1: assegnazione dei criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c99cd-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c99cd-115">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c99cd-116">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c99cd-117">Il comando finale assegna il criterio in $Policy a livello di gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="c99cd-118">Esempio 2: assegnazione dei criteri a livello di gruppo di risorse con l'oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="c99cd-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c99cd-119">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c99cd-120">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c99cd-121">Il secondo comando consente di ottenere la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c99cd-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c99cd-122">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="c99cd-123">Il terzo e il quarto comando creano un oggetto contenente tutte le aree di Azure con "East" nel nome.</span><span class="sxs-lookup"><span data-stu-id="c99cd-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="c99cd-124">I comandi archiviano l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c99cd-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="c99cd-125">Il comando finale assegna i criteri in $Policy a livello di un gruppo di risorse usando l'oggetto Parameter Policy in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c99cd-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="c99cd-126">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c99cd-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c99cd-127">Esempio 3: assegnazione dei criteri a livello di gruppo di risorse con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="c99cd-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="c99cd-128">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="c99cd-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="c99cd-129">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c99cd-130">Il secondo comando ottiene la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c99cd-131">Il comando finale assegna i criteri in $Policy al gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="c99cd-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="c99cd-132">Esempio 4: assegnazione di criteri con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="c99cd-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="c99cd-133">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c99cd-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c99cd-134">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c99cd-135">Il comando finale assegna il criterio in $Policy al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c99cd-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="c99cd-136">Un'identità gestita viene creata automaticamente e assegnata all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="c99cd-137">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c99cd-137">PARAMETERS</span></span>

### <span data-ttu-id="c99cd-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c99cd-138">-ApiVersion</span></span>
<span data-ttu-id="c99cd-139">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c99cd-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c99cd-140">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="c99cd-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c99cd-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c99cd-141">-AssignIdentity</span></span>
<span data-ttu-id="c99cd-142">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="c99cd-143">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="c99cd-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="c99cd-144">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="c99cd-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="c99cd-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99cd-145">-DefaultProfile</span></span>
<span data-ttu-id="c99cd-146">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c99cd-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-147">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c99cd-147">-Description</span></span>
<span data-ttu-id="c99cd-148">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="c99cd-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="c99cd-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c99cd-149">-DisplayName</span></span>
<span data-ttu-id="c99cd-150">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="c99cd-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c99cd-151">-InformationAction</span></span>
<span data-ttu-id="c99cd-152">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c99cd-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="c99cd-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c99cd-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c99cd-154">Continuare</span><span class="sxs-lookup"><span data-stu-id="c99cd-154">Continue</span></span>
- <span data-ttu-id="c99cd-155">Ignora</span><span class="sxs-lookup"><span data-stu-id="c99cd-155">Ignore</span></span>
- <span data-ttu-id="c99cd-156">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c99cd-156">Inquire</span></span>
- <span data-ttu-id="c99cd-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c99cd-157">SilentlyContinue</span></span>
- <span data-ttu-id="c99cd-158">Stop</span><span class="sxs-lookup"><span data-stu-id="c99cd-158">Stop</span></span>
- <span data-ttu-id="c99cd-159">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c99cd-159">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c99cd-160">-InformationVariable</span></span>
<span data-ttu-id="c99cd-161">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c99cd-161">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-162">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c99cd-162">-Location</span></span>
<span data-ttu-id="c99cd-163">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="c99cd-164">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="c99cd-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="c99cd-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c99cd-165">-Metadata</span></span>
<span data-ttu-id="c99cd-166">Metadati per la nuova assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="c99cd-167">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="c99cd-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c99cd-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="c99cd-168">-Name</span></span>
<span data-ttu-id="c99cd-169">Specifica un nome per l'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="c99cd-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c99cd-170">-NotScope</span></span>
<span data-ttu-id="c99cd-171">Gli ambiti non per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="c99cd-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c99cd-172">-PolicyDefinition</span></span>
<span data-ttu-id="c99cd-173">Specifica un criterio, come oggetto **PsPolicyDefinition** che contiene la regola dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c99cd-174">-PolicyParameter</span></span>
<span data-ttu-id="c99cd-175">Il percorso del file del parametro policy o la stringa del parametro Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="c99cd-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c99cd-176">-PolicyParameterObject</span></span>
<span data-ttu-id="c99cd-177">Oggetto Parameter. Policy.</span><span class="sxs-lookup"><span data-stu-id="c99cd-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="c99cd-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c99cd-178">-PolicySetDefinition</span></span>
<span data-ttu-id="c99cd-179">Oggetto definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c99cd-179">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="c99cd-180">-Pre</span></span>
<span data-ttu-id="c99cd-181">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c99cd-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c99cd-182">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c99cd-182">-Scope</span></span>
<span data-ttu-id="c99cd-183">Specifica l'ambito in cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="c99cd-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="c99cd-184">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare quanto segue: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="c99cd-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="c99cd-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="c99cd-185">-Sku</span></span>
<span data-ttu-id="c99cd-186">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="c99cd-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="c99cd-187">Per impostazione predefinita, il codice SKU gratuito contiene i valori: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="c99cd-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="c99cd-188">Per usare l'USK standard, usare i valori: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="c99cd-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99cd-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99cd-189">CommonParameters</span></span>
<span data-ttu-id="c99cd-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99cd-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99cd-191">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99cd-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99cd-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c99cd-192">INPUTS</span></span>

## <span data-ttu-id="c99cd-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c99cd-193">OUTPUTS</span></span>

## <span data-ttu-id="c99cd-194">Note</span><span class="sxs-lookup"><span data-stu-id="c99cd-194">NOTES</span></span>

## <span data-ttu-id="c99cd-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c99cd-195">RELATED LINKS</span></span>

[<span data-ttu-id="c99cd-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c99cd-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c99cd-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c99cd-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c99cd-198">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c99cd-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="c99cd-199">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c99cd-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


