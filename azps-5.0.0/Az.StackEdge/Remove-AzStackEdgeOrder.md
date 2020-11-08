---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199975"
---
# <span data-ttu-id="456df-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="456df-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="456df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="456df-102">SYNOPSIS</span></span>
<span data-ttu-id="456df-103">Rimuove l'ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="456df-103">Removes the order for a device.</span></span>

## <span data-ttu-id="456df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="456df-104">SYNTAX</span></span>

### <span data-ttu-id="456df-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="456df-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="456df-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456df-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="456df-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="456df-108">DESCRIPTION</span></span>
<span data-ttu-id="456df-109">Il cmdlet **Remove-AzStackEdgeOrder** Elimina un ordine esistente per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="456df-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="456df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="456df-110">EXAMPLES</span></span>

### <span data-ttu-id="456df-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="456df-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="456df-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="456df-112">PARAMETERS</span></span>

### <span data-ttu-id="456df-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456df-113">-AsJob</span></span>
<span data-ttu-id="456df-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="456df-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="456df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456df-115">-DefaultProfile</span></span>
<span data-ttu-id="456df-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="456df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456df-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="456df-117">-DeviceName</span></span>
<span data-ttu-id="456df-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="456df-118">Device Name</span></span>

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

### <span data-ttu-id="456df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="456df-119">-InputObject</span></span>
<span data-ttu-id="456df-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="456df-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="456df-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="456df-121">-PassThru</span></span>
<span data-ttu-id="456df-122">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="456df-122">returns true if successful</span></span>

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

### <span data-ttu-id="456df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456df-123">-ResourceGroupName</span></span>
<span data-ttu-id="456df-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="456df-124">Resource Group Name</span></span>

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

### <span data-ttu-id="456df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-125">-ResourceId</span></span>
<span data-ttu-id="456df-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="456df-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="456df-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="456df-127">-Confirm</span></span>
<span data-ttu-id="456df-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="456df-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456df-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456df-129">-WhatIf</span></span>
<span data-ttu-id="456df-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="456df-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="456df-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="456df-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456df-132">CommonParameters</span></span>
<span data-ttu-id="456df-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456df-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="456df-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456df-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="456df-135">INPUTS</span></span>

### <span data-ttu-id="456df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="456df-136">System.String</span></span>

### <span data-ttu-id="456df-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="456df-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="456df-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="456df-138">OUTPUTS</span></span>

### <span data-ttu-id="456df-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="456df-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="456df-140">Note</span><span class="sxs-lookup"><span data-stu-id="456df-140">NOTES</span></span>

## <span data-ttu-id="456df-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="456df-141">RELATED LINKS</span></span>
