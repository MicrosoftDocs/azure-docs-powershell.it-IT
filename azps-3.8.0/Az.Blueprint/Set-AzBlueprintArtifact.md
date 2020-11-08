---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: c71a587dc755ae1834198f14142d5a511fe17ea2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018945"
---
# <span data-ttu-id="ecfe8-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="ecfe8-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="ecfe8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecfe8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfe8-103">Aggiornare un elemento in una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="ecfe8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecfe8-104">SYNTAX</span></span>


### <span data-ttu-id="ecfe8-105">UpdateTemplateArtifact (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecfe8-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfe8-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfe8-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="ecfe8-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecfe8-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="ecfe8-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecfe8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecfe8-109">DESCRIPTION</span></span>
<span data-ttu-id="ecfe8-110">Aggiornare un elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-110">Update an artifact.</span></span> <span data-ttu-id="ecfe8-111">Esistono due modi per aggiornare un elemento: tramite JSON di un elemento come file di input o tramite la fornitura di parametri inline per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="ecfe8-112">Mentre il metodo JSON non richiede il tipo di elemento per il metodo di parametro inline fornito richiede all'utente di fornire il tipo del parametro con tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="ecfe8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecfe8-113">EXAMPLES</span></span>

### <span data-ttu-id="ecfe8-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecfe8-114">Example 1</span></span>
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

<span data-ttu-id="ecfe8-115">Aggiornare un elemento tramite un file JSON di un elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="ecfe8-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ecfe8-116">Example 2</span></span>
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

<span data-ttu-id="ecfe8-117">Aggiornare un elemento tramite parametri inline.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="ecfe8-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ecfe8-118">Example 3</span></span>
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

<span data-ttu-id="ecfe8-119">Aggiornare un elemento tramite un file di modello ARM.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="ecfe8-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecfe8-120">PARAMETERS</span></span>

### <span data-ttu-id="ecfe8-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-121">-ArtifactFile</span></span>
<span data-ttu-id="ecfe8-122">Posizione del file dell'elemento in formato JSON su disco.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="ecfe8-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ecfe8-123">-Blueprint</span></span>
<span data-ttu-id="ecfe8-124">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-124">Blueprint object.</span></span>

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

### <span data-ttu-id="ecfe8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-125">-DefaultProfile</span></span>
<span data-ttu-id="ecfe8-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfe8-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="ecfe8-127">-DependsOn</span></span>
<span data-ttu-id="ecfe8-128">Elenco dei nomi degli elementi che devono essere creati prima che venga creato l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="ecfe8-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecfe8-129">-Description</span></span>
<span data-ttu-id="ecfe8-130">Descrizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="ecfe8-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecfe8-131">-Name</span></span>
<span data-ttu-id="ecfe8-132">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="ecfe8-132">Name of the artifact</span></span>

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

### <span data-ttu-id="ecfe8-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ecfe8-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="ecfe8-134">ID definizione della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="ecfe8-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="ecfe8-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="ecfe8-136">Hashtable di parametri da passare all'elemento di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="ecfe8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfe8-137">-ResourceGroupName</span></span>
<span data-ttu-id="ecfe8-138">Nome del gruppo di risorse in cui è presente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="ecfe8-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ecfe8-139">-RoleDefinitionId</span></span>
<span data-ttu-id="ecfe8-140">Elenco della definizione di ruolo</span><span class="sxs-lookup"><span data-stu-id="ecfe8-140">List of role definition</span></span>

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

### <span data-ttu-id="ecfe8-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="ecfe8-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="ecfe8-142">Elenco di ID entità definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="ecfe8-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-143">-TemplateFile</span></span>
<span data-ttu-id="ecfe8-144">Posizione del file del modello ARM su disco.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="ecfe8-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-145">-TemplateParameterFile</span></span>
<span data-ttu-id="ecfe8-146">Posizione del file del parametro del modello ARM sul disco.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="ecfe8-147">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ecfe8-147">-Type</span></span>
<span data-ttu-id="ecfe8-148">Tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-148">Type of the artifact.</span></span>
<span data-ttu-id="ecfe8-149">Sono supportati 3 tipi: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="ecfe8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfe8-150">CommonParameters</span></span>
<span data-ttu-id="ecfe8-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ecfe8-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfe8-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfe8-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecfe8-153">INPUTS</span></span>

### <span data-ttu-id="ecfe8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ecfe8-154">System.String</span></span>

### <span data-ttu-id="ecfe8-155">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="ecfe8-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="ecfe8-156">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ecfe8-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ecfe8-157">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ecfe8-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ecfe8-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ecfe8-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ecfe8-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="ecfe8-159">System.String[]</span></span>

## <span data-ttu-id="ecfe8-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecfe8-160">OUTPUTS</span></span>

### <span data-ttu-id="ecfe8-161">Microsoft. Azure. Management. Blueprint. Models. artefatto</span><span class="sxs-lookup"><span data-stu-id="ecfe8-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="ecfe8-162">Note</span><span class="sxs-lookup"><span data-stu-id="ecfe8-162">NOTES</span></span>

## <span data-ttu-id="ecfe8-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecfe8-163">RELATED LINKS</span></span>
