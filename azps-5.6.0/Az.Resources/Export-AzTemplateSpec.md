---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: eb6311dacd05f539cf508657e52637524ea98ea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974478"
---
# <span data-ttu-id="a6676-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="a6676-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="a6676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6676-102">SYNOPSIS</span></span>
<span data-ttu-id="a6676-103">Esporta una specifica del modello nel file system locale</span><span class="sxs-lookup"><span data-stu-id="a6676-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="a6676-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6676-104">SYNTAX</span></span>

### <span data-ttu-id="a6676-105">ExportByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6676-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6676-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6676-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6676-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6676-107">DESCRIPTION</span></span>
<span data-ttu-id="a6676-108">Esporta una specifica versione Delle specifiche del modello nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="a6676-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="a6676-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6676-109">EXAMPLES</span></span>

### <span data-ttu-id="a6676-110">Esempio 1: Esportare in base al nome</span><span class="sxs-lookup"><span data-stu-id="a6676-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="a6676-111">Esporta la versione 'v1.0' della specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse 'myRG' nella cartella di output locale "v1".</span><span class="sxs-lookup"><span data-stu-id="a6676-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="a6676-112">Esempio 2: Esportare in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a6676-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="a6676-113">Esporta la versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse 'myRG' dell'id secondario della sottoscrizione nella cartella di output locale \{ \} "v1".</span><span class="sxs-lookup"><span data-stu-id="a6676-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="a6676-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6676-114">PARAMETERS</span></span>

### <span data-ttu-id="a6676-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6676-115">-DefaultProfile</span></span>
<span data-ttu-id="a6676-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6676-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6676-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a6676-117">-Name</span></span>
<span data-ttu-id="a6676-118">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="a6676-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="a6676-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="a6676-119">-OutputFolder</span></span>
<span data-ttu-id="a6676-120">Percorso della cartella in cui verrà restituita la versione specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="a6676-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="a6676-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6676-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6676-122">Nome del gruppo di risorse delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="a6676-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="a6676-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6676-123">-ResourceId</span></span>
<span data-ttu-id="a6676-124">ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="a6676-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="a6676-125">-Version</span><span class="sxs-lookup"><span data-stu-id="a6676-125">-Version</span></span>
<span data-ttu-id="a6676-126">Versione delle specifiche del modello da esportare.</span><span class="sxs-lookup"><span data-stu-id="a6676-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="a6676-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6676-127">-Confirm</span></span>
<span data-ttu-id="a6676-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6676-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6676-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6676-129">-WhatIf</span></span>
<span data-ttu-id="a6676-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6676-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6676-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6676-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6676-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6676-132">CommonParameters</span></span>
<span data-ttu-id="a6676-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6676-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6676-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6676-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6676-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6676-135">INPUTS</span></span>

### <span data-ttu-id="a6676-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a6676-136">System.String</span></span>

## <span data-ttu-id="a6676-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6676-137">OUTPUTS</span></span>

### <span data-ttu-id="a6676-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a6676-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a6676-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6676-139">NOTES</span></span>

## <span data-ttu-id="a6676-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6676-140">RELATED LINKS</span></span>
