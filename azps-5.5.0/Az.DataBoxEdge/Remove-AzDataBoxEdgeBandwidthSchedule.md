---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181079"
---
# <span data-ttu-id="373a5-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="373a5-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="373a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="373a5-102">SYNOPSIS</span></span>
<span data-ttu-id="373a5-103">Rimuove una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="373a5-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="373a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="373a5-104">SYNTAX</span></span>

### <span data-ttu-id="373a5-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="373a5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373a5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="373a5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373a5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="373a5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373a5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="373a5-108">DESCRIPTION</span></span>
<span data-ttu-id="373a5-109">Il cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** rimuove la pianificazione della larghezza di banda per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="373a5-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="373a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="373a5-110">EXAMPLES</span></span>

### <span data-ttu-id="373a5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="373a5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="373a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="373a5-112">PARAMETERS</span></span>

### <span data-ttu-id="373a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="373a5-113">-AsJob</span></span>
<span data-ttu-id="373a5-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="373a5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="373a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373a5-115">-DefaultProfile</span></span>
<span data-ttu-id="373a5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="373a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373a5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="373a5-117">-DeviceName</span></span>
<span data-ttu-id="373a5-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="373a5-118">Device Name</span></span>

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

### <span data-ttu-id="373a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373a5-119">-InputObject</span></span>
<span data-ttu-id="373a5-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="373a5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="373a5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="373a5-121">-Name</span></span>
<span data-ttu-id="373a5-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="373a5-122">Resource Name</span></span>

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

### <span data-ttu-id="373a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="373a5-123">-PassThru</span></span>
<span data-ttu-id="373a5-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="373a5-124">returns true if successful</span></span>

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

### <span data-ttu-id="373a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="373a5-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="373a5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="373a5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="373a5-127">-ResourceId</span></span>
<span data-ttu-id="373a5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="373a5-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="373a5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="373a5-129">-Confirm</span></span>
<span data-ttu-id="373a5-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="373a5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373a5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373a5-131">-WhatIf</span></span>
<span data-ttu-id="373a5-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="373a5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="373a5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="373a5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373a5-134">CommonParameters</span></span>
<span data-ttu-id="373a5-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373a5-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="373a5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373a5-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="373a5-137">INPUTS</span></span>

### <span data-ttu-id="373a5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="373a5-138">System.String</span></span>

### <span data-ttu-id="373a5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="373a5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="373a5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="373a5-140">OUTPUTS</span></span>

### <span data-ttu-id="373a5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="373a5-141">System.Boolean</span></span>

## <span data-ttu-id="373a5-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="373a5-142">NOTES</span></span>

## <span data-ttu-id="373a5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="373a5-143">RELATED LINKS</span></span>
