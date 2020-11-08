---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033509"
---
# <span data-ttu-id="a0252-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a0252-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="a0252-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0252-102">SYNOPSIS</span></span>
<span data-ttu-id="a0252-103">Aggiornare un elemento in una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a0252-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="a0252-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0252-104">SYNTAX</span></span>

### <span data-ttu-id="a0252-105">UpdateTemplateArtifact (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0252-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0252-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="a0252-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0252-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a0252-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0252-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a0252-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0252-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0252-109">DESCRIPTION</span></span>
<span data-ttu-id="a0252-110">Aggiornare un elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-110">Update an artifact.</span></span> <span data-ttu-id="a0252-111">Esistono due modi per aggiornare un elemento: tramite JSON di un elemento come file di input o tramite la fornitura di parametri inline per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="a0252-112">Mentre il metodo JSON non richiede il tipo di elemento per il metodo di parametro inline fornito richiede all'utente di fornire il tipo del parametro con tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="a0252-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0252-113">EXAMPLES</span></span>

### <span data-ttu-id="a0252-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0252-114">Example 1</span></span>
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

<span data-ttu-id="a0252-115">Aggiornare un elemento tramite un file JSON di un elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="a0252-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0252-116">Example 2</span></span>
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

<span data-ttu-id="a0252-117">Aggiornare un elemento tramite parametri inline.</span><span class="sxs-lookup"><span data-stu-id="a0252-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="a0252-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a0252-118">Example 3</span></span>
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

<span data-ttu-id="a0252-119">Aggiornare un elemento tramite un file di modello ARM.</span><span class="sxs-lookup"><span data-stu-id="a0252-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="a0252-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0252-120">PARAMETERS</span></span>

### <span data-ttu-id="a0252-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="a0252-121">-ArtifactFile</span></span>
<span data-ttu-id="a0252-122">Posizione del file dell'elemento in formato JSON su disco.</span><span class="sxs-lookup"><span data-stu-id="a0252-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a0252-123">-Blueprint</span></span>
<span data-ttu-id="a0252-124">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a0252-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0252-125">-DefaultProfile</span></span>
<span data-ttu-id="a0252-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0252-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0252-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="a0252-127">-DependsOn</span></span>
<span data-ttu-id="a0252-128">Elenco dei nomi degli elementi che devono essere creati prima che venga creato l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="a0252-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0252-129">-Description</span></span>
<span data-ttu-id="a0252-130">Descrizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0252-131">-Name</span></span>
<span data-ttu-id="a0252-132">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="a0252-132">Name of the artifact</span></span>

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

### <span data-ttu-id="a0252-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a0252-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="a0252-134">ID definizione della definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a0252-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="a0252-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="a0252-136">Hashtable di parametri da passare all'elemento di definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a0252-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0252-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0252-138">Nome del gruppo di risorse in cui è presente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a0252-139">-RoleDefinitionId</span></span>
<span data-ttu-id="a0252-140">Elenco della definizione di ruolo</span><span class="sxs-lookup"><span data-stu-id="a0252-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a0252-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="a0252-142">Elenco di ID entità definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="a0252-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a0252-143">-TemplateFile</span></span>
<span data-ttu-id="a0252-144">Posizione del file del modello ARM su disco.</span><span class="sxs-lookup"><span data-stu-id="a0252-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0252-145">-TemplateParameterFile</span></span>
<span data-ttu-id="a0252-146">Posizione del file del parametro del modello ARM sul disco.</span><span class="sxs-lookup"><span data-stu-id="a0252-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-147">-Digitare</span><span class="sxs-lookup"><span data-stu-id="a0252-147">-Type</span></span>
<span data-ttu-id="a0252-148">Tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="a0252-148">Type of the artifact.</span></span>
<span data-ttu-id="a0252-149">Sono supportati 3 tipi: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="a0252-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0252-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0252-150">-Confirm</span></span>
<span data-ttu-id="a0252-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0252-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0252-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0252-152">-WhatIf</span></span>
<span data-ttu-id="a0252-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0252-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0252-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0252-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0252-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0252-155">CommonParameters</span></span>
<span data-ttu-id="a0252-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0252-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0252-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0252-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0252-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0252-158">INPUTS</span></span>

### <span data-ttu-id="a0252-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a0252-159">System.String</span></span>

### <span data-ttu-id="a0252-160">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="a0252-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="a0252-161">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a0252-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a0252-162">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a0252-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a0252-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0252-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a0252-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="a0252-164">System.String[]</span></span>

## <span data-ttu-id="a0252-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0252-165">OUTPUTS</span></span>

### <span data-ttu-id="a0252-166">Microsoft. Azure. Management. Blueprint. Models. artefatto</span><span class="sxs-lookup"><span data-stu-id="a0252-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="a0252-167">Note</span><span class="sxs-lookup"><span data-stu-id="a0252-167">NOTES</span></span>

## <span data-ttu-id="a0252-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0252-168">RELATED LINKS</span></span>
