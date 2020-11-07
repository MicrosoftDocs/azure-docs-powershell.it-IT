---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: bec39b242de14da944496a4371fa661d95ce9c59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856397"
---
# <span data-ttu-id="f5d6c-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5d6c-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="f5d6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d6c-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="f5d6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5d6c-104">SYNTAX</span></span>

### <span data-ttu-id="f5d6c-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5d6c-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d6c-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d6c-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d6c-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d6c-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d6c-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d6c-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5d6c-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d6c-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d6c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d6c-110">DESCRIPTION</span></span>
<span data-ttu-id="f5d6c-111">Il cmdlet **New-AzPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="f5d6c-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="f5d6c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5d6c-113">EXAMPLES</span></span>

### <span data-ttu-id="f5d6c-114">Esempio 1: assegnazione dei criteri a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="f5d6c-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="f5d6c-115">Il primo comando ottiene un abbonamento denominato Subscription01 usando il cmdlet Get-AzSubscription e lo archivia nella variabile $Subscription.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="f5d6c-116">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5d6c-117">Il comando finale assegna il criterio in $Policy al livello dell'abbonamento identificato dalla stringa dell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="f5d6c-118">Esempio 2: assegnazione dei criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f5d6c-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="f5d6c-119">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5d6c-120">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5d6c-121">Il comando finale assegna il criterio in $Policy a livello di gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="f5d6c-122">Esempio 3: assegnazione dei criteri a livello di gruppo di risorse con l'oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="f5d6c-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="f5d6c-123">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f5d6c-124">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5d6c-125">Il secondo comando consente di ottenere la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f5d6c-126">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="f5d6c-127">Il terzo e il quarto comando creano un oggetto contenente tutte le aree di Azure con "East" nel nome.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="f5d6c-128">I comandi archiviano l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="f5d6c-129">Il comando finale assegna i criteri in $Policy a livello di un gruppo di risorse usando l'oggetto Parameter Policy in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="f5d6c-130">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f5d6c-131">Esempio 4: assegnazione dei criteri a livello di gruppo di risorse con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5d6c-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="f5d6c-132">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="f5d6c-133">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5d6c-134">Il secondo comando ottiene la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5d6c-135">Il comando finale assegna i criteri in $Policy al gruppo di risorse identificato dalla proprietà **resourceId** di $ResourceGroup usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="f5d6c-136">Esempio 5: assegnazione di criteri con un'identità gestita</span><span class="sxs-lookup"><span data-stu-id="f5d6c-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="f5d6c-137">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzResourceGroup e lo archivia nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f5d6c-138">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzPolicyDefinition e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="f5d6c-139">Il comando finale assegna il criterio in $Policy al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="f5d6c-140">Un'identità gestita viene creata automaticamente e assegnata all'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="f5d6c-141">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5d6c-141">PARAMETERS</span></span>

### <span data-ttu-id="f5d6c-142">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5d6c-142">-ApiVersion</span></span>
<span data-ttu-id="f5d6c-143">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-143">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5d6c-144">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-144">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f5d6c-145">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d6c-145">-AssignIdentity</span></span>
<span data-ttu-id="f5d6c-146">Genera e assegna un'identità di Azure Active Directory per questa assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-146">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="f5d6c-147">L'identità verrà usata per l'esecuzione di distribuzioni per i criteri "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="f5d6c-147">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="f5d6c-148">La posizione è obbligatoria per l'assegnazione di un'identità.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-148">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="f5d6c-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d6c-149">-DefaultProfile</span></span>
<span data-ttu-id="f5d6c-150">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f5d6c-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5d6c-151">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d6c-151">-Description</span></span>
<span data-ttu-id="f5d6c-152">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="f5d6c-152">The description for policy assignment</span></span>

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

### <span data-ttu-id="f5d6c-153">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f5d6c-153">-DisplayName</span></span>
<span data-ttu-id="f5d6c-154">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-154">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="f5d6c-155">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f5d6c-155">-Location</span></span>
<span data-ttu-id="f5d6c-156">Posizione dell'identità delle risorse dell'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-156">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="f5d6c-157">Questo è necessario quando viene usato l'opzione-AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-157">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="f5d6c-158">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f5d6c-158">-Metadata</span></span>
<span data-ttu-id="f5d6c-159">Metadati per la nuova assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-159">The metadata for the new policy assignment.</span></span> <span data-ttu-id="f5d6c-160">Può essere un percorso per un nome di file contenente i metadati o i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-160">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="f5d6c-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5d6c-161">-Name</span></span>
<span data-ttu-id="f5d6c-162">Specifica un nome per l'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-162">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="f5d6c-163">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f5d6c-163">-NotScope</span></span>
<span data-ttu-id="f5d6c-164">Gli ambiti non per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-164">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="f5d6c-165">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5d6c-165">-PolicyDefinition</span></span>
<span data-ttu-id="f5d6c-166">Specifica un criterio, come oggetto **PsPolicyDefinition** che contiene la regola dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-166">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="f5d6c-167">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="f5d6c-167">-PolicyParameter</span></span>
<span data-ttu-id="f5d6c-168">Il percorso del file del parametro policy o la stringa del parametro Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-168">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="f5d6c-169">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="f5d6c-169">-PolicyParameterObject</span></span>
<span data-ttu-id="f5d6c-170">Oggetto Parameter. Policy.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-170">The policy parameter object.</span></span>

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

### <span data-ttu-id="f5d6c-171">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f5d6c-171">-PolicySetDefinition</span></span>
<span data-ttu-id="f5d6c-172">Oggetto definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-172">The policy set definition object.</span></span>

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

### <span data-ttu-id="f5d6c-173">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5d6c-173">-Pre</span></span>
<span data-ttu-id="f5d6c-174">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-174">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5d6c-175">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f5d6c-175">-Scope</span></span>
<span data-ttu-id="f5d6c-176">Specifica l'ambito in cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-176">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="f5d6c-177">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare quanto segue: `/subscriptions/` nome del gruppo di risorse ID sottoscrizione `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="f5d6c-177">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="f5d6c-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d6c-178">CommonParameters</span></span>
<span data-ttu-id="f5d6c-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d6c-180">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5d6c-180">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d6c-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5d6c-181">INPUTS</span></span>

### <span data-ttu-id="f5d6c-182">System. String</span><span class="sxs-lookup"><span data-stu-id="f5d6c-182">System.String</span></span>

### <span data-ttu-id="f5d6c-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="f5d6c-183">System.String[]</span></span>

### <span data-ttu-id="f5d6c-184">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5d6c-184">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5d6c-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5d6c-185">OUTPUTS</span></span>

### <span data-ttu-id="f5d6c-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5d6c-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5d6c-187">Note</span><span class="sxs-lookup"><span data-stu-id="f5d6c-187">NOTES</span></span>

## <span data-ttu-id="f5d6c-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5d6c-188">RELATED LINKS</span></span>

[<span data-ttu-id="f5d6c-189">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5d6c-189">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f5d6c-190">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5d6c-190">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="f5d6c-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5d6c-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="f5d6c-192">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f5d6c-192">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


