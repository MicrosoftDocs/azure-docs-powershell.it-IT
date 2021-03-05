---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: bf0c995081e98f3c3e79af2aec8da5144c3e2e32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998547"
---
# <span data-ttu-id="27171-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="27171-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="27171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27171-102">SYNOPSIS</span></span>
<span data-ttu-id="27171-103">Rimuove il ruolo IoT associato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27171-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="27171-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27171-104">SYNTAX</span></span>

### <span data-ttu-id="27171-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27171-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27171-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27171-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27171-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27171-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27171-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27171-108">DESCRIPTION</span></span>
<span data-ttu-id="27171-109">Il cmdlet **Remove-AzDataBoxEdgeRole** rimuove il ruolo IoT associato per un dispositivo Microsoft Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="27171-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="27171-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27171-110">EXAMPLES</span></span>

### <span data-ttu-id="27171-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27171-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="27171-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27171-112">PARAMETERS</span></span>

### <span data-ttu-id="27171-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27171-113">-AsJob</span></span>
<span data-ttu-id="27171-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27171-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27171-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27171-115">-DefaultProfile</span></span>
<span data-ttu-id="27171-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27171-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27171-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="27171-117">-DeviceName</span></span>
<span data-ttu-id="27171-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="27171-118">Device Name</span></span>

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

### <span data-ttu-id="27171-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27171-119">-InputObject</span></span>
<span data-ttu-id="27171-120">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="27171-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27171-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27171-121">-Name</span></span>
<span data-ttu-id="27171-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="27171-122">Resource Name</span></span>

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

### <span data-ttu-id="27171-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27171-123">-PassThru</span></span>
<span data-ttu-id="27171-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="27171-124">returns true if successful</span></span>

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

### <span data-ttu-id="27171-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27171-125">-ResourceGroupName</span></span>
<span data-ttu-id="27171-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="27171-126">Resource Group Name</span></span>

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

### <span data-ttu-id="27171-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27171-127">-ResourceId</span></span>
<span data-ttu-id="27171-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="27171-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27171-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27171-129">-Confirm</span></span>
<span data-ttu-id="27171-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27171-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27171-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27171-131">-WhatIf</span></span>
<span data-ttu-id="27171-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27171-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27171-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27171-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27171-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27171-134">CommonParameters</span></span>
<span data-ttu-id="27171-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27171-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27171-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27171-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27171-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="27171-137">INPUTS</span></span>

### <span data-ttu-id="27171-138">System.String</span><span class="sxs-lookup"><span data-stu-id="27171-138">System.String</span></span>

### <span data-ttu-id="27171-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="27171-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="27171-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27171-140">OUTPUTS</span></span>

### <span data-ttu-id="27171-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="27171-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="27171-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="27171-142">NOTES</span></span>

## <span data-ttu-id="27171-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27171-143">RELATED LINKS</span></span>
