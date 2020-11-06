---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519368"
---
# <span data-ttu-id="76308-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76308-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="76308-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76308-102">SYNOPSIS</span></span>
<span data-ttu-id="76308-103">Crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76308-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76308-104">SYNTAX</span></span>

### <span data-ttu-id="76308-105">CreateWithoutParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76308-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76308-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="76308-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76308-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="76308-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76308-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="76308-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76308-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="76308-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76308-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76308-110">DESCRIPTION</span></span>
<span data-ttu-id="76308-111">Il cmdlet **New-AzureRmPolicyAssignment** crea un'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="76308-112">Specificare un criterio e un ambito.</span><span class="sxs-lookup"><span data-stu-id="76308-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="76308-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76308-113">EXAMPLES</span></span>

### <span data-ttu-id="76308-114">Esempio 1: assegnazione dei criteri a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="76308-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="76308-115">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="76308-116">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="76308-117">Il secondo comando ottiene la definizione dei criteri denominata VirtualMachinePolicy usando il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76308-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="76308-118">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="76308-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="76308-119">Il comando finale assegna il criterio in $Policy a livello di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76308-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="76308-120">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76308-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="76308-121">Esempio 2: assegnazione dei criteri a livello di gruppo di risorse con l'oggetto Parameter Policy</span><span class="sxs-lookup"><span data-stu-id="76308-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="76308-122">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="76308-123">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="76308-124">Il secondo comando consente di ottenere la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76308-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="76308-125">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="76308-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="76308-126">Il terzo e il quarto comando creano un oggetto contenente tutte le aree di Azure con "East" nel nome.</span><span class="sxs-lookup"><span data-stu-id="76308-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="76308-127">I comandi archiviano l'oggetto nella variabile $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="76308-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="76308-128">Il comando finale assegna i criteri in $Policy a livello di un gruppo di risorse usando l'oggetto Parameter Policy in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="76308-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="76308-129">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76308-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="76308-130">Esempio 3: assegnazione dei criteri a livello di gruppo di risorse con il file dei parametri dei criteri</span><span class="sxs-lookup"><span data-stu-id="76308-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="76308-131">Creare un file denominato _AllowedLocations.js_ nella directory di lavoro locale con il contenuto seguente.</span><span class="sxs-lookup"><span data-stu-id="76308-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="76308-132">Il primo comando ottiene un gruppo di risorse denominato ResourceGroup11 usando il cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="76308-133">Il comando Archivia l'oggetto nella variabile $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76308-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="76308-134">Il secondo comando consente di ottenere la definizione dei criteri predefinita per i percorsi consentiti usando il cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76308-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="76308-135">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="76308-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="76308-136">Il comando finale assegna i criteri in $Policy a livello di un gruppo di risorse usando il file dei parametri del criterio AllowedLocations.jsdalla directory di lavoro locale.</span><span class="sxs-lookup"><span data-stu-id="76308-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="76308-137">La proprietà **resourceId** di $ResourceGroup identifica il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76308-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="76308-138">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76308-138">PARAMETERS</span></span>

### <span data-ttu-id="76308-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76308-139">-ApiVersion</span></span>
<span data-ttu-id="76308-140">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="76308-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="76308-141">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="76308-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76308-142">-DefaultProfile</span></span>
<span data-ttu-id="76308-143">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="76308-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-144">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="76308-144">-Description</span></span>
<span data-ttu-id="76308-145">Descrizione dell'assegnazione di criteri</span><span class="sxs-lookup"><span data-stu-id="76308-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76308-146">-DisplayName</span></span>
<span data-ttu-id="76308-147">Specifica un nome visualizzato per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76308-148">-InformationAction</span></span>
<span data-ttu-id="76308-149">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="76308-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76308-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="76308-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76308-151">Continuare</span><span class="sxs-lookup"><span data-stu-id="76308-151">Continue</span></span>
- <span data-ttu-id="76308-152">Ignora</span><span class="sxs-lookup"><span data-stu-id="76308-152">Ignore</span></span>
- <span data-ttu-id="76308-153">Informarsi</span><span class="sxs-lookup"><span data-stu-id="76308-153">Inquire</span></span>
- <span data-ttu-id="76308-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76308-154">SilentlyContinue</span></span>
- <span data-ttu-id="76308-155">Stop</span><span class="sxs-lookup"><span data-stu-id="76308-155">Stop</span></span>
- <span data-ttu-id="76308-156">Sospensione</span><span class="sxs-lookup"><span data-stu-id="76308-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76308-157">-InformationVariable</span></span>
<span data-ttu-id="76308-158">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="76308-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="76308-159">-Name</span></span>
<span data-ttu-id="76308-160">Specifica un nome per l'assegnazione di criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="76308-161">-NotScope</span></span>
<span data-ttu-id="76308-162">Gli ambiti non per l'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76308-163">-PolicyDefinition</span></span>
<span data-ttu-id="76308-164">Specifica un criterio, come oggetto **PSObject** che contiene la regola dei criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="76308-165">-PolicyParameter</span></span>
<span data-ttu-id="76308-166">Il percorso del file del parametro policy o la stringa del parametro Policy.</span><span class="sxs-lookup"><span data-stu-id="76308-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="76308-167">-PolicyParameterObject</span></span>
<span data-ttu-id="76308-168">Oggetto Parameter. Policy.</span><span class="sxs-lookup"><span data-stu-id="76308-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="76308-169">-PolicySetDefinition</span></span>
<span data-ttu-id="76308-170">Oggetto definizione set di criteri.</span><span class="sxs-lookup"><span data-stu-id="76308-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="76308-171">-Pre</span></span>
<span data-ttu-id="76308-172">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="76308-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76308-173">-Ambito</span><span class="sxs-lookup"><span data-stu-id="76308-173">-Scope</span></span>
<span data-ttu-id="76308-174">Specifica l'ambito in cui assegnare il criterio.</span><span class="sxs-lookup"><span data-stu-id="76308-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="76308-175">Ad esempio, per assegnare un criterio a un gruppo di risorse, specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="76308-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="76308-176">`/subscriptions/`nome del `/resourcegroups/` gruppo di risorse ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="76308-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="76308-177">-Sku</span></span>
<span data-ttu-id="76308-178">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="76308-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="76308-179">Impostazioni predefinite per il codice SKU gratuito: nome = a0, Tier = fre</span><span class="sxs-lookup"><span data-stu-id="76308-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76308-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76308-180">CommonParameters</span></span>
<span data-ttu-id="76308-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76308-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76308-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76308-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76308-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76308-183">INPUTS</span></span>

### <span data-ttu-id="76308-184">Nessuno</span><span class="sxs-lookup"><span data-stu-id="76308-184">None</span></span>
<span data-ttu-id="76308-185">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="76308-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76308-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76308-186">OUTPUTS</span></span>

### <span data-ttu-id="76308-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="76308-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="76308-188">Note</span><span class="sxs-lookup"><span data-stu-id="76308-188">NOTES</span></span>

## <span data-ttu-id="76308-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76308-189">RELATED LINKS</span></span>

[<span data-ttu-id="76308-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76308-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="76308-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76308-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="76308-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76308-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="76308-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76308-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


