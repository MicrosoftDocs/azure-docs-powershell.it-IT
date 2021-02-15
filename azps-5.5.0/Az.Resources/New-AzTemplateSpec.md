---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201879"
---
# <span data-ttu-id="f3b96-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f3b96-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="f3b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b96-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b96-103">Crea una nuova specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="f3b96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3b96-104">SYNTAX</span></span>

### <span data-ttu-id="f3b96-105">FromJsonStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3b96-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3b96-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3b96-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3b96-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3b96-107">DESCRIPTION</span></span>
<span data-ttu-id="f3b96-108">Crea una nuova versione Specifica modello con il contenuto del ARM modello specificato.</span><span class="sxs-lookup"><span data-stu-id="f3b96-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="f3b96-109">Il contenuto può essere derivato da una stringa JSON non elaborata (usando il set di parametri **FromJsonStringParameterSet)** o da un file JSON specificato (usando il set di parametri **FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="f3b96-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="f3b96-110">Se la specifica del modello radice non esiste già, verrà creata insieme alla versione Template Spec.</span><span class="sxs-lookup"><span data-stu-id="f3b96-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="f3b96-111">Se una specifica di modello esiste già con il nome specificato, verrà aggiornata e le eventuali altre versioni esistenti verranno mantenute.</span><span class="sxs-lookup"><span data-stu-id="f3b96-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="f3b96-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3b96-112">EXAMPLES</span></span>

### <span data-ttu-id="f3b96-113">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="f3b96-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="f3b96-114">Crea una nuova versione Specifica modello "v1.0" in una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="f3b96-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="f3b96-115">La versione specificata avrà $templateJson contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="f3b96-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="f3b96-116">**Nota:** Il ARM predefinito nell'esempio non ha alcuna attività perché non contiene risorse effettive.</span><span class="sxs-lookup"><span data-stu-id="f3b96-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="f3b96-117">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="f3b96-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="f3b96-118">Crea una nuova versione delle specifiche del modello "v2.0" in una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="f3b96-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="f3b96-119">La versione specificata avrà il contenuto del file locale "myTemplateContent.js" come contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="f3b96-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="f3b96-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3b96-120">PARAMETERS</span></span>

### <span data-ttu-id="f3b96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b96-121">-DefaultProfile</span></span>
<span data-ttu-id="f3b96-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b96-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b96-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3b96-123">-Description</span></span>
<span data-ttu-id="f3b96-124">Descrizione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="f3b96-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3b96-125">-DisplayName</span></span>
<span data-ttu-id="f3b96-126">Nome visualizzato della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="f3b96-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f3b96-127">-Force</span></span>
<span data-ttu-id="f3b96-128">Non chiedere conferma quando si sovrascrive una versione esistente.</span><span class="sxs-lookup"><span data-stu-id="f3b96-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="f3b96-129">-Location</span><span class="sxs-lookup"><span data-stu-id="f3b96-129">-Location</span></span>
<span data-ttu-id="f3b96-130">Posizione delle specifiche del modello. Obbligatorio solo se le specifiche del modello non esistono già.</span><span class="sxs-lookup"><span data-stu-id="f3b96-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="f3b96-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f3b96-131">-Name</span></span>
<span data-ttu-id="f3b96-132">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b96-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b96-133">-ResourceGroupName</span></span>
<span data-ttu-id="f3b96-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3b96-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b96-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3b96-135">-Tag</span></span>
<span data-ttu-id="f3b96-136">Tabella hash dei tag per le nuove risorse specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="f3b96-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f3b96-137">-TemplateFile</span></span>
<span data-ttu-id="f3b96-138">Percorso del file JSON del modello locale di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b96-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b96-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="f3b96-139">-TemplateJson</span></span>
<span data-ttu-id="f3b96-140">JSON del modello Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b96-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b96-141">-Version</span><span class="sxs-lookup"><span data-stu-id="f3b96-141">-Version</span></span>
<span data-ttu-id="f3b96-142">Versione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="f3b96-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="f3b96-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="f3b96-143">-VersionDescription</span></span>
<span data-ttu-id="f3b96-144">Descrizione della versione.</span><span class="sxs-lookup"><span data-stu-id="f3b96-144">The description of the version.</span></span>

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

### <span data-ttu-id="f3b96-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3b96-145">-Confirm</span></span>
<span data-ttu-id="f3b96-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b96-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b96-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b96-147">-WhatIf</span></span>
<span data-ttu-id="f3b96-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3b96-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3b96-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3b96-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b96-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b96-150">CommonParameters</span></span>
<span data-ttu-id="f3b96-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b96-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b96-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3b96-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b96-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3b96-153">INPUTS</span></span>

### <span data-ttu-id="f3b96-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f3b96-154">System.String</span></span>

## <span data-ttu-id="f3b96-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3b96-155">OUTPUTS</span></span>

### <span data-ttu-id="f3b96-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f3b96-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="f3b96-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3b96-157">NOTES</span></span>

## <span data-ttu-id="f3b96-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3b96-158">RELATED LINKS</span></span>
