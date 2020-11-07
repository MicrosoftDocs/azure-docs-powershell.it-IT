---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675606"
---
# <span data-ttu-id="643af-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="643af-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="643af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="643af-102">SYNOPSIS</span></span>
<span data-ttu-id="643af-103">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="643af-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="643af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="643af-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="643af-105">DESCRIPTION</span></span>
<span data-ttu-id="643af-106">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="643af-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="643af-107">Se non viene specificata una versione di definizione del modello, viene recuperata la versione bozza.</span><span class="sxs-lookup"><span data-stu-id="643af-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="643af-108">Nel caso in cui non sia presente una versione bozza, viene restituita la definizione più recente del modello pubblicato.</span><span class="sxs-lookup"><span data-stu-id="643af-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="643af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="643af-109">EXAMPLES</span></span>

### <span data-ttu-id="643af-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="643af-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="643af-111">Recuperare gli elementi da una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="643af-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="643af-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="643af-112">PARAMETERS</span></span>

### <span data-ttu-id="643af-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="643af-113">-ArtifactFile</span></span>
<span data-ttu-id="643af-114">Posizione del file dell'elemento in formato JSON su disco.</span><span class="sxs-lookup"><span data-stu-id="643af-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="643af-115">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="643af-115">-Blueprint</span></span>
<span data-ttu-id="643af-116">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="643af-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="643af-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="643af-117">-BlueprintVersion</span></span>
<span data-ttu-id="643af-118">Versione del modello per cui recuperare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="643af-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643af-119">-DefaultProfile</span></span>
<span data-ttu-id="643af-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="643af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643af-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="643af-121">-DependsOn</span></span>
<span data-ttu-id="643af-122">Elenco dei nomi degli elementi che devono essere creati prima che venga creato l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="643af-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="643af-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="643af-123">-Description</span></span>
<span data-ttu-id="643af-124">Descrizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="643af-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="643af-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="643af-125">-Name</span></span>
<span data-ttu-id="643af-126">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="643af-126">Name of the artifact</span></span>

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

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="643af-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="643af-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="643af-128">ID definizione della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="643af-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="643af-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="643af-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="643af-130">Hashtable di parametri da passare all'elemento di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="643af-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="643af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643af-131">-ResourceGroupName</span></span>
<span data-ttu-id="643af-132">Nome del gruppo di risorse in cui è presente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="643af-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="643af-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="643af-133">-RoleDefinitionId</span></span>
<span data-ttu-id="643af-134">Elenco della definizione di ruolo</span><span class="sxs-lookup"><span data-stu-id="643af-134">List of role definition</span></span>

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

### <span data-ttu-id="643af-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="643af-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="643af-136">Elenco di ID entità definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="643af-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="643af-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="643af-137">-TemplateFile</span></span>
<span data-ttu-id="643af-138">Posizione del file del modello ARM su disco.</span><span class="sxs-lookup"><span data-stu-id="643af-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="643af-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="643af-139">-TemplateParameterFile</span></span>
<span data-ttu-id="643af-140">Posizione del file del parametro del modello ARM sul disco.</span><span class="sxs-lookup"><span data-stu-id="643af-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="643af-141">-Digitare</span><span class="sxs-lookup"><span data-stu-id="643af-141">-Type</span></span>
<span data-ttu-id="643af-142">Tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="643af-142">Type of the artifact.</span></span>
<span data-ttu-id="643af-143">Sono supportati 3 tipi: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="643af-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="643af-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="643af-144">-Confirm</span></span>
<span data-ttu-id="643af-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643af-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643af-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643af-146">-WhatIf</span></span>
<span data-ttu-id="643af-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="643af-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643af-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="643af-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643af-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643af-149">CommonParameters</span></span>
<span data-ttu-id="643af-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643af-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="643af-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643af-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643af-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="643af-152">INPUTS</span></span>

### <span data-ttu-id="643af-153">System. String</span><span class="sxs-lookup"><span data-stu-id="643af-153">System.String</span></span>

### <span data-ttu-id="643af-154">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="643af-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="643af-155">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="643af-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="643af-156">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="643af-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="643af-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="643af-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="643af-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="643af-158">System.String[]</span></span>

## <span data-ttu-id="643af-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="643af-159">OUTPUTS</span></span>

### <span data-ttu-id="643af-160">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="643af-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="643af-161">Note</span><span class="sxs-lookup"><span data-stu-id="643af-161">NOTES</span></span>

## <span data-ttu-id="643af-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="643af-162">RELATED LINKS</span></span>
