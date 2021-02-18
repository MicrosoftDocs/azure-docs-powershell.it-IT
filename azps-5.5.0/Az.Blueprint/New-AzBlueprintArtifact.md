---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200910"
---
# <span data-ttu-id="aadc8-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="aadc8-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="aadc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aadc8-102">SYNOPSIS</span></span>
<span data-ttu-id="aadc8-103">Creare un nuovo elemento e salvarlo all'interno di una definizione di progetto.</span><span class="sxs-lookup"><span data-stu-id="aadc8-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="aadc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aadc8-104">SYNTAX</span></span>

### <span data-ttu-id="aadc8-105">CreateTemplateArtifact (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aadc8-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aadc8-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="aadc8-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aadc8-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="aadc8-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aadc8-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="aadc8-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aadc8-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aadc8-109">DESCRIPTION</span></span>
<span data-ttu-id="aadc8-110">Creare un nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-110">Create a new artifact.</span></span> <span data-ttu-id="aadc8-111">Esistono due modi per creare un elemento: tramite un JSON dell'elemento come file di input o fornendo parametri inline per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="aadc8-112">Anche se il metodo JSON non richiede che il tipo dell'elemento sia fornito con il metodo del parametro inline, è necessario fornire all'utente il tipo dell'elemento tramite il parametro -Type.</span><span class="sxs-lookup"><span data-stu-id="aadc8-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="aadc8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aadc8-113">EXAMPLES</span></span>

### <span data-ttu-id="aadc8-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aadc8-114">Example 1</span></span>
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

<span data-ttu-id="aadc8-115">Creare un nuovo elemento tramite un file JSON dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="aadc8-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aadc8-116">Example 2</span></span>
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

<span data-ttu-id="aadc8-117">Creare un nuovo elemento tramite parametri in linea.</span><span class="sxs-lookup"><span data-stu-id="aadc8-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="aadc8-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="aadc8-118">Example 3</span></span>
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

<span data-ttu-id="aadc8-119">Creare un nuovo elemento tramite un file ARM file modello.</span><span class="sxs-lookup"><span data-stu-id="aadc8-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="aadc8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aadc8-120">PARAMETERS</span></span>

### <span data-ttu-id="aadc8-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="aadc8-121">-ArtifactFile</span></span>
<span data-ttu-id="aadc8-122">Posizione del file dell'elemento in formato JSON sul disco.</span><span class="sxs-lookup"><span data-stu-id="aadc8-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-123">-Progetto</span><span class="sxs-lookup"><span data-stu-id="aadc8-123">-Blueprint</span></span>
<span data-ttu-id="aadc8-124">Oggetto progetto.</span><span class="sxs-lookup"><span data-stu-id="aadc8-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadc8-125">-DefaultProfile</span></span>
<span data-ttu-id="aadc8-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aadc8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadc8-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="aadc8-127">-DependsOn</span></span>
<span data-ttu-id="aadc8-128">Elenco dei nomi degli elementi che devono essere creati prima della creazione dell'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="aadc8-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="aadc8-129">-Description</span></span>
<span data-ttu-id="aadc8-130">Descrizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="aadc8-131">-Name</span></span>
<span data-ttu-id="aadc8-132">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="aadc8-132">Name of the artifact</span></span>

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

### <span data-ttu-id="aadc8-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="aadc8-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="aadc8-134">ID definizione della definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="aadc8-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="aadc8-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="aadc8-136">Tabella hash dei parametri da passare all'elemento della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="aadc8-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadc8-137">-ResourceGroupName</span></span>
<span data-ttu-id="aadc8-138">Nome del gruppo di risorse in cui si trova l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="aadc8-139">-RoleDefinitionId</span></span>
<span data-ttu-id="aadc8-140">Elenco della definizione di ruolo</span><span class="sxs-lookup"><span data-stu-id="aadc8-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="aadc8-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="aadc8-142">Elenco di ID entità definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="aadc8-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="aadc8-143">-TemplateFile</span></span>
<span data-ttu-id="aadc8-144">Percorso del file ARM modello sul disco.</span><span class="sxs-lookup"><span data-stu-id="aadc8-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="aadc8-145">-TemplateParameterFile</span></span>
<span data-ttu-id="aadc8-146">Percorso del file ARM parametro del modello sul disco.</span><span class="sxs-lookup"><span data-stu-id="aadc8-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-147">-Type</span><span class="sxs-lookup"><span data-stu-id="aadc8-147">-Type</span></span>
<span data-ttu-id="aadc8-148">Tipo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="aadc8-148">Type of the artifact.</span></span>
<span data-ttu-id="aadc8-149">Sono supportati tre tipi: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="aadc8-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aadc8-150">-Confirm</span></span>
<span data-ttu-id="aadc8-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aadc8-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aadc8-152">-WhatIf</span></span>
<span data-ttu-id="aadc8-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aadc8-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aadc8-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aadc8-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aadc8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadc8-155">CommonParameters</span></span>
<span data-ttu-id="aadc8-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aadc8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadc8-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aadc8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadc8-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="aadc8-158">INPUTS</span></span>

### <span data-ttu-id="aadc8-159">System.String</span><span class="sxs-lookup"><span data-stu-id="aadc8-159">System.String</span></span>

### <span data-ttu-id="aadc8-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactActAct</span><span class="sxs-lookup"><span data-stu-id="aadc8-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="aadc8-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="aadc8-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="aadc8-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="aadc8-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="aadc8-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aadc8-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aadc8-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aadc8-164">System.String[]</span></span>

## <span data-ttu-id="aadc8-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aadc8-165">OUTPUTS</span></span>

### <span data-ttu-id="aadc8-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="aadc8-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="aadc8-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="aadc8-167">NOTES</span></span>

## <span data-ttu-id="aadc8-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aadc8-168">RELATED LINKS</span></span>
