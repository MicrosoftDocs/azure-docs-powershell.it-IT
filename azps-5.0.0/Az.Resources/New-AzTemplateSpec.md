---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200503"
---
# <span data-ttu-id="01d9f-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="01d9f-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="01d9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="01d9f-103">Crea una nuova specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="01d9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01d9f-104">SYNTAX</span></span>

### <span data-ttu-id="01d9f-105">FromJsonStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01d9f-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d9f-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d9f-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d9f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="01d9f-108">Crea una nuova versione spec modello con il contenuto del modello ARM specificato.</span><span class="sxs-lookup"><span data-stu-id="01d9f-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="01d9f-109">Il contenuto può provenire da una stringa JSON non elaborata (con il set di parametri **FromJsonStringParameterSet** ) o da un file JSON specificato (con il set di parametri **FromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="01d9f-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="01d9f-110">Se la specifica del modello radice non esiste già, verrà creata insieme alla versione specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="01d9f-111">Se una specifica modello esiste già con il nome specificato, la versione specificata verrà aggiornata (verranno mantenute tutte le altre versioni esistenti).</span><span class="sxs-lookup"><span data-stu-id="01d9f-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="01d9f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01d9f-112">EXAMPLES</span></span>

### <span data-ttu-id="01d9f-113">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="01d9f-113">Example 1:</span></span>
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

<span data-ttu-id="01d9f-114">Crea una nuova versione specifica del modello "v 1.0" in una specifica del modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="01d9f-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="01d9f-115">La versione specificata avrà $templateJson come contenuto del modello ARM della versione.</span><span class="sxs-lookup"><span data-stu-id="01d9f-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="01d9f-116">**Nota:** Il modello ARM nell'esempio è un no-op perché non contiene risorse effettive.</span><span class="sxs-lookup"><span data-stu-id="01d9f-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="01d9f-117">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="01d9f-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="01d9f-118">Crea una nuova versione specifica del modello "v 2.0" in una specifica del modello denominata "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="01d9f-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="01d9f-119">La versione specificata includerà il contenuto del file locale "myTemplateContent.json" come contenuto del modello ARM della versione.</span><span class="sxs-lookup"><span data-stu-id="01d9f-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="01d9f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01d9f-120">PARAMETERS</span></span>

### <span data-ttu-id="01d9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d9f-121">-DefaultProfile</span></span>
<span data-ttu-id="01d9f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01d9f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d9f-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="01d9f-123">-Description</span></span>
<span data-ttu-id="01d9f-124">Descrizione della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="01d9f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="01d9f-125">-DisplayName</span></span>
<span data-ttu-id="01d9f-126">Nome visualizzato della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="01d9f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="01d9f-127">-Force</span></span>
<span data-ttu-id="01d9f-128">Non chiedere conferma quando si sovrascrive una versione esistente.</span><span class="sxs-lookup"><span data-stu-id="01d9f-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="01d9f-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="01d9f-129">-Location</span></span>
<span data-ttu-id="01d9f-130">Posizione della specifica del modello. Obbligatorio solo se la specifica del modello non esiste già.</span><span class="sxs-lookup"><span data-stu-id="01d9f-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="01d9f-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="01d9f-131">-Name</span></span>
<span data-ttu-id="01d9f-132">Nome della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="01d9f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d9f-133">-ResourceGroupName</span></span>
<span data-ttu-id="01d9f-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01d9f-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="01d9f-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="01d9f-135">-TemplateFile</span></span>
<span data-ttu-id="01d9f-136">Percorso del file del file JSON del modello di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="01d9f-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="01d9f-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="01d9f-137">-TemplateJson</span></span>
<span data-ttu-id="01d9f-138">JSON del modello di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="01d9f-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="01d9f-139">-Versione</span><span class="sxs-lookup"><span data-stu-id="01d9f-139">-Version</span></span>
<span data-ttu-id="01d9f-140">Versione della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="01d9f-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="01d9f-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="01d9f-141">-VersionDescription</span></span>
<span data-ttu-id="01d9f-142">Descrizione della versione.</span><span class="sxs-lookup"><span data-stu-id="01d9f-142">The description of the version.</span></span>

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

### <span data-ttu-id="01d9f-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01d9f-143">-Confirm</span></span>
<span data-ttu-id="01d9f-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d9f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d9f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d9f-145">-WhatIf</span></span>
<span data-ttu-id="01d9f-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d9f-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01d9f-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d9f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d9f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d9f-148">CommonParameters</span></span>
<span data-ttu-id="01d9f-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d9f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d9f-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01d9f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d9f-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01d9f-151">INPUTS</span></span>

### <span data-ttu-id="01d9f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="01d9f-152">System.String</span></span>

## <span data-ttu-id="01d9f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01d9f-153">OUTPUTS</span></span>

### <span data-ttu-id="01d9f-154">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="01d9f-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="01d9f-155">Note</span><span class="sxs-lookup"><span data-stu-id="01d9f-155">NOTES</span></span>

## <span data-ttu-id="01d9f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01d9f-156">RELATED LINKS</span></span>
