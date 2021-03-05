---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 2e1b3e3db319f724e22673e4139b4cb290879d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004286"
---
# <span data-ttu-id="6c298-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6c298-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="6c298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c298-102">SYNOPSIS</span></span>
<span data-ttu-id="6c298-103">Rimuove un trigger esistente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c298-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="6c298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c298-104">SYNTAX</span></span>

### <span data-ttu-id="6c298-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c298-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c298-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c298-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c298-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c298-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c298-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c298-108">DESCRIPTION</span></span>
<span data-ttu-id="6c298-109">Il cmdlet **Remove-AzDataBoxEdgeTrigger** rimuove un trigger esistente nel dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="6c298-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="6c298-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c298-110">EXAMPLES</span></span>

### <span data-ttu-id="6c298-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c298-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="6c298-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c298-112">PARAMETERS</span></span>

### <span data-ttu-id="6c298-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c298-113">-AsJob</span></span>
<span data-ttu-id="6c298-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6c298-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c298-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c298-115">-DefaultProfile</span></span>
<span data-ttu-id="6c298-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c298-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c298-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c298-117">-DeviceName</span></span>
<span data-ttu-id="6c298-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="6c298-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c298-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c298-119">-InputObject</span></span>
<span data-ttu-id="6c298-120">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="6c298-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c298-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c298-121">-Name</span></span>
<span data-ttu-id="6c298-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="6c298-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c298-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c298-123">-PassThru</span></span>
<span data-ttu-id="6c298-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6c298-124">returns true if successful</span></span>

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

### <span data-ttu-id="6c298-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c298-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c298-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6c298-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c298-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c298-127">-ResourceId</span></span>
<span data-ttu-id="6c298-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c298-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c298-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c298-129">-Confirm</span></span>
<span data-ttu-id="6c298-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c298-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c298-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c298-131">-WhatIf</span></span>
<span data-ttu-id="6c298-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c298-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c298-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c298-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c298-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c298-134">CommonParameters</span></span>
<span data-ttu-id="6c298-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c298-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c298-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c298-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c298-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c298-137">INPUTS</span></span>

### <span data-ttu-id="6c298-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6c298-138">System.String</span></span>

### <span data-ttu-id="6c298-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6c298-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="6c298-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c298-140">OUTPUTS</span></span>

### <span data-ttu-id="6c298-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c298-141">System.Boolean</span></span>

## <span data-ttu-id="6c298-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c298-142">NOTES</span></span>

## <span data-ttu-id="6c298-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c298-143">RELATED LINKS</span></span>
