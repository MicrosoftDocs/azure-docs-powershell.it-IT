---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479208"
---
# <span data-ttu-id="9d74a-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9d74a-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="9d74a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d74a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d74a-103">Rimuove una specifica modello</span><span class="sxs-lookup"><span data-stu-id="9d74a-103">Removes a Template Spec</span></span>

## <span data-ttu-id="9d74a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d74a-104">SYNTAX</span></span>

### <span data-ttu-id="9d74a-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d74a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d74a-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d74a-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d74a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d74a-107">DESCRIPTION</span></span>
<span data-ttu-id="9d74a-108">Rimuove una specifica del modello specificata. Se il parametro version **-Version** viene specificato, solo la versione specificata verrà rimossa.</span><span class="sxs-lookup"><span data-stu-id="9d74a-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="9d74a-109">Se non è disponibile una versione specifica, la specifica del modello e tutte le relative versioni verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="9d74a-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="9d74a-110">Se il contrassegno di forza è presente **,** non verrà visualizzata alcuna richiesta di conferma per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="9d74a-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="9d74a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d74a-111">EXAMPLES</span></span>

### <span data-ttu-id="9d74a-112">Esempio 1: rimozione di una versione specifica per nome</span><span class="sxs-lookup"><span data-stu-id="9d74a-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="9d74a-113">Rimuove la versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="9d74a-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="9d74a-114">Esempio 2: rimozione di una versione specifica tramite ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9d74a-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="9d74a-115">Rimuove la versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" dell'abbonamento \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="9d74a-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="9d74a-116">Esempio 3: rimozione di una specifica modello e di tutte le versioni per nome</span><span class="sxs-lookup"><span data-stu-id="9d74a-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="9d74a-117">Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="9d74a-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="9d74a-118">Esempio 3: rimozione di una specifica modello e di tutte le versioni per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9d74a-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="9d74a-119">Rimuove la specifica del modello denominata "MyTemplateSpec" e tutte le relative versioni nel gruppo di risorse "myRG" dell'abbonamento \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="9d74a-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="9d74a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d74a-120">PARAMETERS</span></span>

### <span data-ttu-id="9d74a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d74a-121">-DefaultProfile</span></span>
<span data-ttu-id="9d74a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d74a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d74a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9d74a-123">-Force</span></span>
<span data-ttu-id="9d74a-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9d74a-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9d74a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d74a-125">-Name</span></span>
<span data-ttu-id="9d74a-126">Nome della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="9d74a-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="9d74a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d74a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d74a-128">Nome del gruppo di risorse della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="9d74a-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="9d74a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d74a-129">-ResourceId</span></span>
<span data-ttu-id="9d74a-130">ID risorsa completo del modello spec. esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="9d74a-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="9d74a-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="9d74a-131">-Version</span></span>
<span data-ttu-id="9d74a-132">La versione della specifica del modello da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9d74a-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="9d74a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d74a-133">-Confirm</span></span>
<span data-ttu-id="9d74a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d74a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d74a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d74a-135">-WhatIf</span></span>
<span data-ttu-id="9d74a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d74a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d74a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d74a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d74a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d74a-138">CommonParameters</span></span>
<span data-ttu-id="9d74a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d74a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d74a-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d74a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d74a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d74a-141">INPUTS</span></span>

### <span data-ttu-id="9d74a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9d74a-142">System.String</span></span>

## <span data-ttu-id="9d74a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d74a-143">OUTPUTS</span></span>

### <span data-ttu-id="9d74a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d74a-144">System.Boolean</span></span>

## <span data-ttu-id="9d74a-145">Note</span><span class="sxs-lookup"><span data-stu-id="9d74a-145">NOTES</span></span>

## <span data-ttu-id="9d74a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d74a-146">RELATED LINKS</span></span>
