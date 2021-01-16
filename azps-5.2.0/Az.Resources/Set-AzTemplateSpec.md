---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354031"
---
# <span data-ttu-id="d68e9-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d68e9-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="d68e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d68e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d68e9-103">Modifica una specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="d68e9-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="d68e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d68e9-104">SYNTAX</span></span>

### <span data-ttu-id="d68e9-105">FromJsonStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d68e9-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d68e9-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68e9-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68e9-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68e9-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68e9-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68e9-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68e9-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d68e9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d68e9-112">DESCRIPTION</span></span>
<span data-ttu-id="d68e9-113">Modifica una specifica Templace. Se la specifica del modello con il nome specificato e/o la versione specifica non esiste già, verrà creata.</span><span class="sxs-lookup"><span data-stu-id="d68e9-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="d68e9-114">Quando modifichi il contenuto del modello ARM della versione specifica del modello, il contenuto può provenire da una stringa JSON non elaborata (usando il set di parametri **UpdateVersionByNameFromJsonParameterSet** ) o da un file JSON specificato (usando il set di parametri **UpdateVersionByNameFromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="d68e9-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="d68e9-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d68e9-115">EXAMPLES</span></span>

### <span data-ttu-id="d68e9-116">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d68e9-116">Example 1:</span></span>
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

<span data-ttu-id="d68e9-117">Modifica la versione "v 1.0" di una specifica del modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="d68e9-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="d68e9-118">La versione specificata avrà $templateJson come contenuto del modello ARM della versione.</span><span class="sxs-lookup"><span data-stu-id="d68e9-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="d68e9-119">Se le specifiche e/o la versione del modello radice non esistono già, verranno create.</span><span class="sxs-lookup"><span data-stu-id="d68e9-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="d68e9-120">**Note**</span><span class="sxs-lookup"><span data-stu-id="d68e9-120">**Notes:**</span></span> 

* <span data-ttu-id="d68e9-121">Il modello ARM nell'esempio è un no-op perché non contiene risorse effettive.</span><span class="sxs-lookup"><span data-stu-id="d68e9-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="d68e9-122">La posizione è necessaria solo quando la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="d68e9-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="d68e9-123">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="d68e9-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="d68e9-124">Modifica la versione "v 2.0" di una specifica del modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="d68e9-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="d68e9-125">La versione specificata includerà il contenuto del file locale "myTemplateContent.json" come contenuto del modello ARM della versione.</span><span class="sxs-lookup"><span data-stu-id="d68e9-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="d68e9-126">Se le specifiche e/o la versione del modello radice non esistono già, verranno create.</span><span class="sxs-lookup"><span data-stu-id="d68e9-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="d68e9-127">**Nota:** La posizione è necessaria solo quando la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="d68e9-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="d68e9-128">Esempio 3:</span><span class="sxs-lookup"><span data-stu-id="d68e9-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="d68e9-129">Modifica la descrizione della specifica del modello denominata "myTemplateSpec" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="d68e9-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="d68e9-130">Se la specifica del modello non esiste già, verrà creata.</span><span class="sxs-lookup"><span data-stu-id="d68e9-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="d68e9-131">**Nota:** La posizione è necessaria solo quando la specifica del modello non esiste già</span><span class="sxs-lookup"><span data-stu-id="d68e9-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="d68e9-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d68e9-132">PARAMETERS</span></span>

### <span data-ttu-id="d68e9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68e9-133">-DefaultProfile</span></span>
<span data-ttu-id="d68e9-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d68e9-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68e9-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d68e9-135">-Description</span></span>
<span data-ttu-id="d68e9-136">Descrizione della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="d68e9-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="d68e9-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d68e9-137">-DisplayName</span></span>
<span data-ttu-id="d68e9-138">Nome visualizzato della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="d68e9-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="d68e9-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d68e9-139">-Location</span></span>
<span data-ttu-id="d68e9-140">Posizione della specifica del modello. Obbligatorio solo se la specifica del modello non esiste già.</span><span class="sxs-lookup"><span data-stu-id="d68e9-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="d68e9-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="d68e9-141">-Name</span></span>
<span data-ttu-id="d68e9-142">Nome della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="d68e9-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="d68e9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68e9-143">-ResourceGroupName</span></span>
<span data-ttu-id="d68e9-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d68e9-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="d68e9-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d68e9-145">-ResourceId</span></span>
<span data-ttu-id="d68e9-146">ID risorsa completo del modello spec. esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="d68e9-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="d68e9-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="d68e9-147">-Tag</span></span>
<span data-ttu-id="d68e9-148">Hashtable di tag per la specifica e/o la versione del modello</span><span class="sxs-lookup"><span data-stu-id="d68e9-148">Hashtable of tags for the template spec and/or version</span></span>

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

### <span data-ttu-id="d68e9-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d68e9-149">-TemplateFile</span></span>
<span data-ttu-id="d68e9-150">Percorso del file del file JSON del modello di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d68e9-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="d68e9-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="d68e9-151">-TemplateJson</span></span>
<span data-ttu-id="d68e9-152">JSON del modello di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="d68e9-152">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="d68e9-153">-Versione</span><span class="sxs-lookup"><span data-stu-id="d68e9-153">-Version</span></span>
<span data-ttu-id="d68e9-154">Versione della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="d68e9-154">The version of the template spec.</span></span>

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

### <span data-ttu-id="d68e9-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="d68e9-155">-VersionDescription</span></span>
<span data-ttu-id="d68e9-156">Descrizione della versione.</span><span class="sxs-lookup"><span data-stu-id="d68e9-156">The description of the version.</span></span>

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

### <span data-ttu-id="d68e9-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d68e9-157">-Confirm</span></span>
<span data-ttu-id="d68e9-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d68e9-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68e9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68e9-159">-WhatIf</span></span>
<span data-ttu-id="d68e9-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68e9-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d68e9-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d68e9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68e9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68e9-162">CommonParameters</span></span>
<span data-ttu-id="d68e9-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d68e9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68e9-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d68e9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68e9-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d68e9-165">INPUTS</span></span>

### <span data-ttu-id="d68e9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d68e9-166">System.String</span></span>

## <span data-ttu-id="d68e9-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d68e9-167">OUTPUTS</span></span>

### <span data-ttu-id="d68e9-168">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d68e9-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="d68e9-169">Note</span><span class="sxs-lookup"><span data-stu-id="d68e9-169">NOTES</span></span>

## <span data-ttu-id="d68e9-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d68e9-170">RELATED LINKS</span></span>
