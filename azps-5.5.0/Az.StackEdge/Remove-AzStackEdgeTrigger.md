---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176679"
---
# <span data-ttu-id="14d47-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="14d47-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="14d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d47-102">SYNOPSIS</span></span>
<span data-ttu-id="14d47-103">Rimuove un trigger esistente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14d47-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="14d47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14d47-104">SYNTAX</span></span>

### <span data-ttu-id="14d47-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14d47-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d47-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d47-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d47-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d47-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d47-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14d47-108">DESCRIPTION</span></span>
<span data-ttu-id="14d47-109">Il cmdlet **Remove-AzStackEdgeTrigger** rimuove un trigger esistente nel dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="14d47-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="14d47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14d47-110">EXAMPLES</span></span>

### <span data-ttu-id="14d47-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14d47-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="14d47-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d47-112">PARAMETERS</span></span>

### <span data-ttu-id="14d47-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14d47-113">-AsJob</span></span>
<span data-ttu-id="14d47-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14d47-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14d47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d47-115">-DefaultProfile</span></span>
<span data-ttu-id="14d47-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14d47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d47-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14d47-117">-DeviceName</span></span>
<span data-ttu-id="14d47-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="14d47-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d47-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14d47-119">-InputObject</span></span>
<span data-ttu-id="14d47-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="14d47-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d47-121">-Name</span><span class="sxs-lookup"><span data-stu-id="14d47-121">-Name</span></span>
<span data-ttu-id="14d47-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="14d47-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d47-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14d47-123">-PassThru</span></span>
<span data-ttu-id="14d47-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="14d47-124">returns true if successful</span></span>

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

### <span data-ttu-id="14d47-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d47-125">-ResourceGroupName</span></span>
<span data-ttu-id="14d47-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="14d47-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d47-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14d47-127">-ResourceId</span></span>
<span data-ttu-id="14d47-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14d47-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="14d47-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14d47-129">-Confirm</span></span>
<span data-ttu-id="14d47-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d47-131">-WhatIf</span></span>
<span data-ttu-id="14d47-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d47-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14d47-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d47-134">CommonParameters</span></span>
<span data-ttu-id="14d47-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d47-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14d47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d47-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="14d47-137">INPUTS</span></span>

### <span data-ttu-id="14d47-138">System.String</span><span class="sxs-lookup"><span data-stu-id="14d47-138">System.String</span></span>

### <span data-ttu-id="14d47-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="14d47-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="14d47-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14d47-140">OUTPUTS</span></span>

### <span data-ttu-id="14d47-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14d47-141">System.Boolean</span></span>

## <span data-ttu-id="14d47-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="14d47-142">NOTES</span></span>

## <span data-ttu-id="14d47-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14d47-143">RELATED LINKS</span></span>
