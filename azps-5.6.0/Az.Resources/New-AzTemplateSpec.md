---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 72c668f195024ac88e6d8ed67c08c6db6d0e3445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974446"
---
# <span data-ttu-id="1f0e2-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="1f0e2-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="1f0e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0e2-103">Crea una nuova specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="1f0e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f0e2-104">SYNTAX</span></span>

### <span data-ttu-id="1f0e2-105">FromJsonStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f0e2-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f0e2-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f0e2-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f0e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f0e2-107">DESCRIPTION</span></span>
<span data-ttu-id="1f0e2-108">Crea una nuova versione Specifica modello con il contenuto del ARM modello specificato.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="1f0e2-109">Il contenuto può essere derivato da una stringa JSON non elaborata (usando il set di parametri **FromJsonStringParameterSet)** o da un file JSON specificato (usando il set di parametri **FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="1f0e2-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="1f0e2-110">Se la specifica del modello radice non esiste già, verrà creata insieme alla versione Template Spec.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="1f0e2-111">Se una specifica di modello esiste già con il nome specificato, verrà aggiornata e le eventuali altre versioni esistenti verranno mantenute.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="1f0e2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f0e2-112">EXAMPLES</span></span>

### <span data-ttu-id="1f0e2-113">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="1f0e2-113">Example 1:</span></span>
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

<span data-ttu-id="1f0e2-114">Crea una nuova versione delle specifiche del modello "v1.0" in una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="1f0e2-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="1f0e2-115">La versione specificata avrà $templateJson contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="1f0e2-116">**Nota:** Il ARM predefinito nell'esempio non ha alcuna attività perché non contiene risorse effettive.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="1f0e2-117">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="1f0e2-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="1f0e2-118">Crea una nuova versione delle specifiche del modello "v2.0" in una specifica di modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="1f0e2-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="1f0e2-119">La versione specificata avrà il contenuto del file locale "myTemplateContent.js" come contenuto del modello ARM versione.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="1f0e2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f0e2-120">PARAMETERS</span></span>

### <span data-ttu-id="1f0e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0e2-121">-DefaultProfile</span></span>
<span data-ttu-id="1f0e2-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f0e2-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f0e2-123">-Description</span></span>
<span data-ttu-id="1f0e2-124">Descrizione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="1f0e2-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f0e2-125">-DisplayName</span></span>
<span data-ttu-id="1f0e2-126">Nome visualizzato delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="1f0e2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1f0e2-127">-Force</span></span>
<span data-ttu-id="1f0e2-128">Non chiedere conferma quando si sovrascrive una versione esistente.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="1f0e2-129">-Location</span><span class="sxs-lookup"><span data-stu-id="1f0e2-129">-Location</span></span>
<span data-ttu-id="1f0e2-130">Posizione delle specifiche del modello. Obbligatorio solo se le specifiche del modello non esistono già.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="1f0e2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1f0e2-131">-Name</span></span>
<span data-ttu-id="1f0e2-132">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="1f0e2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0e2-133">-ResourceGroupName</span></span>
<span data-ttu-id="1f0e2-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f0e2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f0e2-135">-Tag</span></span>
<span data-ttu-id="1f0e2-136">Tabella hash dei tag per le risorse specifiche del nuovo modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="1f0e2-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1f0e2-137">-TemplateFile</span></span>
<span data-ttu-id="1f0e2-138">Percorso del file JSON del modello locale di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="1f0e2-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="1f0e2-139">-TemplateJson</span></span>
<span data-ttu-id="1f0e2-140">JSON del modello Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-140">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="1f0e2-141">-Version</span><span class="sxs-lookup"><span data-stu-id="1f0e2-141">-Version</span></span>
<span data-ttu-id="1f0e2-142">Versione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="1f0e2-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="1f0e2-143">-VersionDescription</span></span>
<span data-ttu-id="1f0e2-144">Descrizione della versione.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-144">The description of the version.</span></span>

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

### <span data-ttu-id="1f0e2-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f0e2-145">-Confirm</span></span>
<span data-ttu-id="1f0e2-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f0e2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f0e2-147">-WhatIf</span></span>
<span data-ttu-id="1f0e2-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f0e2-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f0e2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0e2-150">CommonParameters</span></span>
<span data-ttu-id="1f0e2-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0e2-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f0e2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0e2-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f0e2-153">INPUTS</span></span>

### <span data-ttu-id="1f0e2-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1f0e2-154">System.String</span></span>

## <span data-ttu-id="1f0e2-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f0e2-155">OUTPUTS</span></span>

### <span data-ttu-id="1f0e2-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="1f0e2-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="1f0e2-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f0e2-157">NOTES</span></span>

## <span data-ttu-id="1f0e2-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f0e2-158">RELATED LINKS</span></span>
