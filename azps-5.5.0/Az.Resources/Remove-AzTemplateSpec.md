---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189215"
---
# <span data-ttu-id="cef52-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="cef52-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="cef52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef52-102">SYNOPSIS</span></span>
<span data-ttu-id="cef52-103">Rimuove una specifica del modello</span><span class="sxs-lookup"><span data-stu-id="cef52-103">Removes a Template Spec</span></span>

## <span data-ttu-id="cef52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cef52-104">SYNTAX</span></span>

### <span data-ttu-id="cef52-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cef52-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef52-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef52-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef52-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cef52-107">DESCRIPTION</span></span>
<span data-ttu-id="cef52-108">Rimuove una specifica specifica specifica del modello. Se viene fornito **il parametro version -Version,** verrà rimossa solo la versione specificata.</span><span class="sxs-lookup"><span data-stu-id="cef52-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="cef52-109">Se non viene fornita alcuna versione specifica, le specifiche del modello e tutte le relative versioni verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="cef52-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="cef52-110">Se il **contrassegno -Force** è presente, non verrà visualizzata alcuna richiesta di conferma per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="cef52-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="cef52-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cef52-111">EXAMPLES</span></span>

### <span data-ttu-id="cef52-112">Esempio 1: Rimozione di una versione specifica in base al nome</span><span class="sxs-lookup"><span data-stu-id="cef52-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="cef52-113">Rimuove la versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="cef52-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="cef52-114">Esempio 2: Rimozione di una versione specifica in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cef52-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="cef52-115">Rimuove la versione 'v1.0' della specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG" del \{ subId della \} sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cef52-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="cef52-116">Esempio 3: Rimozione di una specifica di modello e di tutte le versioni in base al nome</span><span class="sxs-lookup"><span data-stu-id="cef52-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="cef52-117">Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni all'interno del gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="cef52-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="cef52-118">Esempio 3: Rimozione di una specifica del modello e di tutte le versioni in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cef52-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="cef52-119">Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni all'interno del gruppo di risorse 'myRG' di \{ subscription \} subId.</span><span class="sxs-lookup"><span data-stu-id="cef52-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="cef52-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef52-120">PARAMETERS</span></span>

### <span data-ttu-id="cef52-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef52-121">-DefaultProfile</span></span>
<span data-ttu-id="cef52-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cef52-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef52-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cef52-123">-Force</span></span>
<span data-ttu-id="cef52-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cef52-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cef52-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cef52-125">-Name</span></span>
<span data-ttu-id="cef52-126">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="cef52-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef52-127">-ResourceGroupName</span></span>
<span data-ttu-id="cef52-128">Nome del gruppo di risorse delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="cef52-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef52-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef52-129">-ResourceId</span></span>
<span data-ttu-id="cef52-130">ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="cef52-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef52-131">-Version</span><span class="sxs-lookup"><span data-stu-id="cef52-131">-Version</span></span>
<span data-ttu-id="cef52-132">Versione delle specifiche del modello da eliminare.</span><span class="sxs-lookup"><span data-stu-id="cef52-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef52-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef52-133">-Confirm</span></span>
<span data-ttu-id="cef52-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef52-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef52-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef52-135">-WhatIf</span></span>
<span data-ttu-id="cef52-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef52-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cef52-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef52-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef52-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef52-138">CommonParameters</span></span>
<span data-ttu-id="cef52-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef52-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef52-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cef52-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef52-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="cef52-141">INPUTS</span></span>

### <span data-ttu-id="cef52-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cef52-142">System.String</span></span>

## <span data-ttu-id="cef52-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cef52-143">OUTPUTS</span></span>

### <span data-ttu-id="cef52-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cef52-144">System.Boolean</span></span>

## <span data-ttu-id="cef52-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="cef52-145">NOTES</span></span>

## <span data-ttu-id="cef52-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cef52-146">RELATED LINKS</span></span>
