---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8e8b26ac8bdb097ac87135f764e1dfc4f4450f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972862"
---
# <span data-ttu-id="547d0-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="547d0-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="547d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="547d0-102">SYNOPSIS</span></span>
<span data-ttu-id="547d0-103">Rimuove una condivisione dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="547d0-103">Removes a share from the device.</span></span>

## <span data-ttu-id="547d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="547d0-104">SYNTAX</span></span>

### <span data-ttu-id="547d0-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="547d0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547d0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="547d0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547d0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="547d0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547d0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="547d0-108">DESCRIPTION</span></span>
<span data-ttu-id="547d0-109">Il cmdlet **Remove-AzDataBoxEdgeEdgeShare** rimuove le condivisioni edge associate per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="547d0-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="547d0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="547d0-110">EXAMPLES</span></span>

### <span data-ttu-id="547d0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="547d0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="547d0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="547d0-112">PARAMETERS</span></span>

### <span data-ttu-id="547d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="547d0-113">-AsJob</span></span>
<span data-ttu-id="547d0-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="547d0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="547d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547d0-115">-DefaultProfile</span></span>
<span data-ttu-id="547d0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="547d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547d0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="547d0-117">-DeviceName</span></span>
<span data-ttu-id="547d0-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="547d0-118">Device Name</span></span>

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

### <span data-ttu-id="547d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="547d0-119">-InputObject</span></span>
<span data-ttu-id="547d0-120">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="547d0-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="547d0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="547d0-121">-Name</span></span>
<span data-ttu-id="547d0-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="547d0-122">Resource Name</span></span>

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

### <span data-ttu-id="547d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="547d0-123">-PassThru</span></span>
<span data-ttu-id="547d0-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="547d0-124">returns true if successful</span></span>

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

### <span data-ttu-id="547d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="547d0-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="547d0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="547d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="547d0-127">-ResourceId</span></span>
<span data-ttu-id="547d0-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="547d0-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="547d0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="547d0-129">-Confirm</span></span>
<span data-ttu-id="547d0-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="547d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547d0-131">-WhatIf</span></span>
<span data-ttu-id="547d0-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="547d0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="547d0-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="547d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547d0-134">CommonParameters</span></span>
<span data-ttu-id="547d0-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547d0-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="547d0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547d0-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="547d0-137">INPUTS</span></span>

### <span data-ttu-id="547d0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="547d0-138">System.String</span></span>

### <span data-ttu-id="547d0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="547d0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="547d0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="547d0-140">OUTPUTS</span></span>

### <span data-ttu-id="547d0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="547d0-141">System.Boolean</span></span>

## <span data-ttu-id="547d0-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="547d0-142">NOTES</span></span>

## <span data-ttu-id="547d0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="547d0-143">RELATED LINKS</span></span>
