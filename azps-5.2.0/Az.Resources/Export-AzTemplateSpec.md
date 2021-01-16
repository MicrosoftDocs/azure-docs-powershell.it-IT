---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352324"
---
# <span data-ttu-id="cda08-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="cda08-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="cda08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cda08-102">SYNOPSIS</span></span>
<span data-ttu-id="cda08-103">Esporta una specifica del modello nel file system locale</span><span class="sxs-lookup"><span data-stu-id="cda08-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="cda08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cda08-104">SYNTAX</span></span>

### <span data-ttu-id="cda08-105">ExportByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cda08-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cda08-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda08-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda08-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cda08-107">DESCRIPTION</span></span>
<span data-ttu-id="cda08-108">Esporta una specifica versione di spec modello nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="cda08-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="cda08-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cda08-109">EXAMPLES</span></span>

### <span data-ttu-id="cda08-110">Esempio 1: esportare per nome</span><span class="sxs-lookup"><span data-stu-id="cda08-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="cda08-111">Esporta la versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" nella cartella di output locale "V1".</span><span class="sxs-lookup"><span data-stu-id="cda08-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="cda08-112">Esempio 2: esportare in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="cda08-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="cda08-113">Esporta la versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" di subId di sottoscrizione nella \{ \} cartella di output locale "V1".</span><span class="sxs-lookup"><span data-stu-id="cda08-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="cda08-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cda08-114">PARAMETERS</span></span>

### <span data-ttu-id="cda08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda08-115">-DefaultProfile</span></span>
<span data-ttu-id="cda08-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cda08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda08-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cda08-117">-Name</span></span>
<span data-ttu-id="cda08-118">Nome della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="cda08-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="cda08-119">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="cda08-119">-OutputFolder</span></span>
<span data-ttu-id="cda08-120">Percorso della cartella in cui verrà restituita la versione specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="cda08-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="cda08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda08-121">-ResourceGroupName</span></span>
<span data-ttu-id="cda08-122">Nome del gruppo di risorse della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="cda08-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="cda08-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cda08-123">-ResourceId</span></span>
<span data-ttu-id="cda08-124">ID risorsa completo del modello spec. esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="cda08-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="cda08-125">-Versione</span><span class="sxs-lookup"><span data-stu-id="cda08-125">-Version</span></span>
<span data-ttu-id="cda08-126">La versione della specifica del modello da esportare.</span><span class="sxs-lookup"><span data-stu-id="cda08-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="cda08-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cda08-127">-Confirm</span></span>
<span data-ttu-id="cda08-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cda08-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda08-129">-WhatIf</span></span>
<span data-ttu-id="cda08-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cda08-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cda08-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cda08-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda08-132">CommonParameters</span></span>
<span data-ttu-id="cda08-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda08-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cda08-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda08-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cda08-135">INPUTS</span></span>

### <span data-ttu-id="cda08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cda08-136">System.String</span></span>

## <span data-ttu-id="cda08-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cda08-137">OUTPUTS</span></span>

### <span data-ttu-id="cda08-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cda08-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cda08-139">Note</span><span class="sxs-lookup"><span data-stu-id="cda08-139">NOTES</span></span>

## <span data-ttu-id="cda08-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cda08-140">RELATED LINKS</span></span>
