---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 48a700f29a80b03df0fd4fc2d858dcb1c1c57f76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982174"
---
# <span data-ttu-id="103de-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="103de-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="103de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="103de-102">SYNOPSIS</span></span>
<span data-ttu-id="103de-103">Modifica le specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="103de-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="103de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="103de-104">SYNTAX</span></span>

### <span data-ttu-id="103de-105">FromJsonStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="103de-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="103de-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103de-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103de-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103de-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103de-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103de-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="103de-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103de-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="103de-112">DESCRIPTION</span></span>
<span data-ttu-id="103de-113">Modifica una specifica di Templace. Se la specifica del modello con il nome e/o la versione specificata non esiste già, verrà creata.</span><span class="sxs-lookup"><span data-stu-id="103de-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="103de-114">Quando si modifica il contenuto del modello ARM Di una versione specifica del modello, il contenuto può essere derivato da una stringa JSON non elaborata (usando il set di parametri **UpdateVersionByNameFromJsonParameterSet)** o da un file JSON specificato (usando il set di parametri **UpdateVersionByNameFromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="103de-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="103de-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="103de-115">EXAMPLES</span></span>

### <span data-ttu-id="103de-116">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="103de-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="103de-117">Modifica la versione "v1.0" di una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="103de-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="103de-118">La versione specificata avrà $templateJson contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="103de-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="103de-119">Se la versione radice delle specifiche del modello e/o non esiste già, verranno create.</span><span class="sxs-lookup"><span data-stu-id="103de-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="103de-120">**Note:**</span><span class="sxs-lookup"><span data-stu-id="103de-120">**Notes:**</span></span> 

* <span data-ttu-id="103de-121">Il ARM predefinito nell'esempio non ha alcuna attività perché non contiene risorse effettive.</span><span class="sxs-lookup"><span data-stu-id="103de-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="103de-122">Il percorso è obbligatorio solo se la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="103de-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="103de-123">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="103de-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="103de-124">Modifica la versione "v2.0" di una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="103de-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="103de-125">La versione specificata avrà il contenuto del file locale "myTemplateContent.js" come contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="103de-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="103de-126">Se la versione radice delle specifiche del modello e/o non esiste già, verranno create.</span><span class="sxs-lookup"><span data-stu-id="103de-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="103de-127">**Nota:** Il percorso è obbligatorio solo se la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="103de-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="103de-128">Esempio 3:</span><span class="sxs-lookup"><span data-stu-id="103de-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="103de-129">Modifica la descrizione della specifica del modello denominata "myTemplateSpec" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="103de-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="103de-130">Se la specifica del modello non esiste già, verrà creata.</span><span class="sxs-lookup"><span data-stu-id="103de-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="103de-131">**Nota:** Il percorso è obbligatorio solo se la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="103de-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="103de-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="103de-132">PARAMETERS</span></span>

### <span data-ttu-id="103de-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103de-133">-DefaultProfile</span></span>
<span data-ttu-id="103de-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="103de-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="103de-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="103de-135">-Description</span></span>
<span data-ttu-id="103de-136">Descrizione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="103de-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="103de-137">-DisplayName</span></span>
<span data-ttu-id="103de-138">Nome visualizzato della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="103de-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-139">-Location</span><span class="sxs-lookup"><span data-stu-id="103de-139">-Location</span></span>
<span data-ttu-id="103de-140">Posizione delle specifiche del modello. Obbligatorio solo se le specifiche del modello non esistono già.</span><span class="sxs-lookup"><span data-stu-id="103de-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="103de-141">-Name</span><span class="sxs-lookup"><span data-stu-id="103de-141">-Name</span></span>
<span data-ttu-id="103de-142">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="103de-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="103de-143">-ResourceGroupName</span></span>
<span data-ttu-id="103de-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="103de-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="103de-145">-ResourceId</span></span>
<span data-ttu-id="103de-146">ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="103de-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="103de-147">-Tag</span></span>
<span data-ttu-id="103de-148">Tabella hash dei tag per la specifica e/o la versione del modello</span><span class="sxs-lookup"><span data-stu-id="103de-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="103de-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="103de-149">-TemplateFile</span></span>
<span data-ttu-id="103de-150">Percorso del file JSON del modello locale di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="103de-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="103de-151">-TemplateJson</span></span>
<span data-ttu-id="103de-152">JSON del modello Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="103de-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-153">-Version</span><span class="sxs-lookup"><span data-stu-id="103de-153">-Version</span></span>
<span data-ttu-id="103de-154">Versione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="103de-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="103de-155">-VersionDescription</span></span>
<span data-ttu-id="103de-156">Descrizione della versione.</span><span class="sxs-lookup"><span data-stu-id="103de-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="103de-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="103de-157">-Confirm</span></span>
<span data-ttu-id="103de-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103de-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103de-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103de-159">-WhatIf</span></span>
<span data-ttu-id="103de-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103de-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="103de-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="103de-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103de-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103de-162">CommonParameters</span></span>
<span data-ttu-id="103de-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103de-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103de-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="103de-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103de-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="103de-165">INPUTS</span></span>

### <span data-ttu-id="103de-166">System.String</span><span class="sxs-lookup"><span data-stu-id="103de-166">System.String</span></span>

## <span data-ttu-id="103de-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="103de-167">OUTPUTS</span></span>

### <span data-ttu-id="103de-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="103de-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="103de-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="103de-169">NOTES</span></span>

## <span data-ttu-id="103de-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="103de-170">RELATED LINKS</span></span>
