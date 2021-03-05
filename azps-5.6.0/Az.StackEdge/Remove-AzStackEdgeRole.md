---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: d34893ef00fd0e7fb799c2bc0569e818f78a4185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005150"
---
# <span data-ttu-id="3b8f8-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3b8f8-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="3b8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8f8-103">Rimuove il ruolo IoT associato per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="3b8f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b8f8-104">SYNTAX</span></span>

### <span data-ttu-id="3b8f8-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b8f8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b8f8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b8f8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b8f8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b8f8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8f8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b8f8-108">DESCRIPTION</span></span>
<span data-ttu-id="3b8f8-109">Il cmdlet **Remove-AzStackEdgeRole** rimuove il ruolo IoT associato per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="3b8f8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b8f8-110">EXAMPLES</span></span>

### <span data-ttu-id="3b8f8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b8f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="3b8f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b8f8-112">PARAMETERS</span></span>

### <span data-ttu-id="3b8f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b8f8-113">-AsJob</span></span>
<span data-ttu-id="3b8f8-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b8f8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b8f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8f8-115">-DefaultProfile</span></span>
<span data-ttu-id="3b8f8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b8f8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3b8f8-117">-DeviceName</span></span>
<span data-ttu-id="3b8f8-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="3b8f8-118">Device Name</span></span>

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

### <span data-ttu-id="3b8f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b8f8-119">-InputObject</span></span>
<span data-ttu-id="3b8f8-120">Oggetto input</span><span class="sxs-lookup"><span data-stu-id="3b8f8-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3b8f8-121">-Name</span></span>
<span data-ttu-id="3b8f8-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="3b8f8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b8f8-123">-PassThru</span></span>
<span data-ttu-id="3b8f8-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="3b8f8-124">returns true if successful</span></span>

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

### <span data-ttu-id="3b8f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b8f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b8f8-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3b8f8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3b8f8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b8f8-127">-ResourceId</span></span>
<span data-ttu-id="3b8f8-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b8f8-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3b8f8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b8f8-129">-Confirm</span></span>
<span data-ttu-id="3b8f8-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b8f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8f8-131">-WhatIf</span></span>
<span data-ttu-id="3b8f8-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b8f8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b8f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8f8-134">CommonParameters</span></span>
<span data-ttu-id="3b8f8-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8f8-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b8f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8f8-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b8f8-137">INPUTS</span></span>

### <span data-ttu-id="3b8f8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3b8f8-138">System.String</span></span>

### <span data-ttu-id="3b8f8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3b8f8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3b8f8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b8f8-140">OUTPUTS</span></span>

### <span data-ttu-id="3b8f8-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3b8f8-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="3b8f8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b8f8-142">NOTES</span></span>

## <span data-ttu-id="3b8f8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b8f8-143">RELATED LINKS</span></span>
