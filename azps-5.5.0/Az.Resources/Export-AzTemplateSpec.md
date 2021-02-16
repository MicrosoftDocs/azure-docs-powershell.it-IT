---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178918"
---
# <span data-ttu-id="acd6c-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="acd6c-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="acd6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="acd6c-103">Esporta una specifica del modello nel file system locale</span><span class="sxs-lookup"><span data-stu-id="acd6c-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="acd6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acd6c-104">SYNTAX</span></span>

### <span data-ttu-id="acd6c-105">ExportByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acd6c-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd6c-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd6c-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd6c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acd6c-107">DESCRIPTION</span></span>
<span data-ttu-id="acd6c-108">Esporta una specifica versione Delle specifiche del modello nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="acd6c-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="acd6c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acd6c-109">EXAMPLES</span></span>

### <span data-ttu-id="acd6c-110">Esempio 1: Esportare in base al nome</span><span class="sxs-lookup"><span data-stu-id="acd6c-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="acd6c-111">Esporta la versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG" nella cartella di output locale "v1".</span><span class="sxs-lookup"><span data-stu-id="acd6c-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="acd6c-112">Esempio 2: Esportare in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="acd6c-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="acd6c-113">Esporta la versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse 'myRG' dell'id secondario della sottoscrizione nella cartella di output locale \{ \} "v1".</span><span class="sxs-lookup"><span data-stu-id="acd6c-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="acd6c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd6c-114">PARAMETERS</span></span>

### <span data-ttu-id="acd6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd6c-115">-DefaultProfile</span></span>
<span data-ttu-id="acd6c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acd6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd6c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="acd6c-117">-Name</span></span>
<span data-ttu-id="acd6c-118">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="acd6c-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd6c-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="acd6c-119">-OutputFolder</span></span>
<span data-ttu-id="acd6c-120">Percorso della cartella in cui verrà restituita la versione specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="acd6c-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="acd6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="acd6c-122">Nome del gruppo di risorse delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="acd6c-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd6c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd6c-123">-ResourceId</span></span>
<span data-ttu-id="acd6c-124">ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="acd6c-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd6c-125">-Version</span><span class="sxs-lookup"><span data-stu-id="acd6c-125">-Version</span></span>
<span data-ttu-id="acd6c-126">Versione delle specifiche del modello da esportare.</span><span class="sxs-lookup"><span data-stu-id="acd6c-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="acd6c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acd6c-127">-Confirm</span></span>
<span data-ttu-id="acd6c-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd6c-129">-WhatIf</span></span>
<span data-ttu-id="acd6c-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acd6c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acd6c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acd6c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd6c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd6c-132">CommonParameters</span></span>
<span data-ttu-id="acd6c-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd6c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd6c-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acd6c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd6c-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="acd6c-135">INPUTS</span></span>

### <span data-ttu-id="acd6c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="acd6c-136">System.String</span></span>

## <span data-ttu-id="acd6c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acd6c-137">OUTPUTS</span></span>

### <span data-ttu-id="acd6c-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="acd6c-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="acd6c-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="acd6c-139">NOTES</span></span>

## <span data-ttu-id="acd6c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acd6c-140">RELATED LINKS</span></span>
