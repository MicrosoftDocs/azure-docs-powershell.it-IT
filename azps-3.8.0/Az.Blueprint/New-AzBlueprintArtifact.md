---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 5ee859811ce791f57fc8c4fa08d2584b28bef1dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018954"
---
# <span data-ttu-id="07d10-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="07d10-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="07d10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07d10-102">SYNOPSIS</span></span>
<span data-ttu-id="07d10-103">Creare un nuovo elemento e salvarlo all'interno di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="07d10-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="07d10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07d10-104">SYNTAX</span></span>

### <span data-ttu-id="07d10-105">CreateTemplateArtifact (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07d10-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d10-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="07d10-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d10-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="07d10-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d10-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="07d10-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d10-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d10-109">DESCRIPTION</span></span>
<span data-ttu-id="07d10-110">Creare un nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-110">Create a new artifact.</span></span> <span data-ttu-id="07d10-111">Esistono due modi per creare un elemento: tramite un elemento JSON come file di input o tramite la creazione di parametri inline per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="07d10-112">Mentre il metodo JSON non richiede il tipo di elemento per il metodo di parametro inline fornito richiede all'utente di fornire il tipo del parametro con tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="07d10-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07d10-113">EXAMPLES</span></span>

### <span data-ttu-id="07d10-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07d10-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="07d10-115">Creare un nuovo elemento tramite un file JSON di un elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="07d10-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="07d10-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG

```

<span data-ttu-id="07d10-117">Creare un nuovo elemento tramite i parametri inline.</span><span class="sxs-lookup"><span data-stu-id="07d10-117">Create a new artifact through inline parameters.</span></span>


### <span data-ttu-id="07d10-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="07d10-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account

```

<span data-ttu-id="07d10-119">Creare un nuovo elemento tramite un file di modello ARM.</span><span class="sxs-lookup"><span data-stu-id="07d10-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="07d10-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07d10-120">PARAMETERS</span></span>

### <span data-ttu-id="07d10-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="07d10-121">-ArtifactFile</span></span>
<span data-ttu-id="07d10-122">Posizione del file dell'elemento in formato JSON su disco.</span><span class="sxs-lookup"><span data-stu-id="07d10-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="07d10-123">-Blueprint</span></span>
<span data-ttu-id="07d10-124">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="07d10-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d10-125">-DefaultProfile</span></span>
<span data-ttu-id="07d10-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07d10-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="07d10-127">-DependsOn</span></span>
<span data-ttu-id="07d10-128">Elenco dei nomi degli elementi che devono essere creati prima che venga creato l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="07d10-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d10-129">-Description</span></span>
<span data-ttu-id="07d10-130">Descrizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="07d10-131">-Name</span></span>
<span data-ttu-id="07d10-132">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="07d10-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="07d10-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="07d10-134">ID definizione della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="07d10-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="07d10-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="07d10-136">Hashtable di parametri da passare all'elemento di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="07d10-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d10-137">-ResourceGroupName</span></span>
<span data-ttu-id="07d10-138">Nome del gruppo di risorse in cui è presente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="07d10-139">-RoleDefinitionId</span></span>
<span data-ttu-id="07d10-140">Elenco della definizione di ruolo</span><span class="sxs-lookup"><span data-stu-id="07d10-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="07d10-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="07d10-142">Elenco di ID entità definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="07d10-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="07d10-143">-TemplateFile</span></span>
<span data-ttu-id="07d10-144">Posizione del file del modello ARM su disco.</span><span class="sxs-lookup"><span data-stu-id="07d10-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="07d10-145">-TemplateParameterFile</span></span>
<span data-ttu-id="07d10-146">Posizione del file del parametro del modello ARM sul disco.</span><span class="sxs-lookup"><span data-stu-id="07d10-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-147">-Digitare</span><span class="sxs-lookup"><span data-stu-id="07d10-147">-Type</span></span>
<span data-ttu-id="07d10-148">Tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="07d10-148">Type of the artifact.</span></span>
<span data-ttu-id="07d10-149">Sono supportati 3 tipi: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="07d10-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d10-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d10-150">CommonParameters</span></span>
<span data-ttu-id="07d10-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d10-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07d10-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d10-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d10-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07d10-153">INPUTS</span></span>

### <span data-ttu-id="07d10-154">System. String</span><span class="sxs-lookup"><span data-stu-id="07d10-154">System.String</span></span>

### <span data-ttu-id="07d10-155">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="07d10-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="07d10-156">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="07d10-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="07d10-157">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="07d10-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="07d10-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07d10-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="07d10-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="07d10-159">System.String[]</span></span>

## <span data-ttu-id="07d10-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07d10-160">OUTPUTS</span></span>

### <span data-ttu-id="07d10-161">Microsoft. Azure. Management. Blueprint. Models. artefatto</span><span class="sxs-lookup"><span data-stu-id="07d10-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="07d10-162">Note</span><span class="sxs-lookup"><span data-stu-id="07d10-162">NOTES</span></span>

## <span data-ttu-id="07d10-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07d10-163">RELATED LINKS</span></span>
