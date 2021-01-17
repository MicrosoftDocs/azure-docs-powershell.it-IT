---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487691"
---
# <span data-ttu-id="b84fe-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="b84fe-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="b84fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b84fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b84fe-103">Rimuove l'ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b84fe-103">Removes the order for a device.</span></span>

## <span data-ttu-id="b84fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b84fe-104">SYNTAX</span></span>

### <span data-ttu-id="b84fe-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b84fe-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b84fe-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b84fe-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b84fe-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b84fe-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b84fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84fe-108">DESCRIPTION</span></span>
<span data-ttu-id="b84fe-109">Il cmdlet **Remove-AzDataBoxEdgeOrder** Elimina un ordine esistente per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="b84fe-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="b84fe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b84fe-110">EXAMPLES</span></span>

### <span data-ttu-id="b84fe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b84fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="b84fe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b84fe-112">PARAMETERS</span></span>

### <span data-ttu-id="b84fe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b84fe-113">-AsJob</span></span>
<span data-ttu-id="b84fe-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b84fe-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b84fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84fe-115">-DefaultProfile</span></span>
<span data-ttu-id="b84fe-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b84fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b84fe-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b84fe-117">-DeviceName</span></span>
<span data-ttu-id="b84fe-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="b84fe-118">Device Name</span></span>

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

### <span data-ttu-id="b84fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b84fe-119">-InputObject</span></span>
<span data-ttu-id="b84fe-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="b84fe-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84fe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b84fe-121">-PassThru</span></span>
<span data-ttu-id="b84fe-122">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b84fe-122">returns true if successful</span></span>

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

### <span data-ttu-id="b84fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b84fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="b84fe-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b84fe-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b84fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b84fe-125">-ResourceId</span></span>
<span data-ttu-id="b84fe-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b84fe-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="b84fe-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b84fe-127">-Confirm</span></span>
<span data-ttu-id="b84fe-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b84fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b84fe-129">-WhatIf</span></span>
<span data-ttu-id="b84fe-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b84fe-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b84fe-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b84fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b84fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84fe-132">CommonParameters</span></span>
<span data-ttu-id="b84fe-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b84fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84fe-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b84fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84fe-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b84fe-135">INPUTS</span></span>

### <span data-ttu-id="b84fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b84fe-136">System.String</span></span>

### <span data-ttu-id="b84fe-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="b84fe-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="b84fe-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b84fe-138">OUTPUTS</span></span>

### <span data-ttu-id="b84fe-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="b84fe-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="b84fe-140">Note</span><span class="sxs-lookup"><span data-stu-id="b84fe-140">NOTES</span></span>

## <span data-ttu-id="b84fe-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b84fe-141">RELATED LINKS</span></span>
