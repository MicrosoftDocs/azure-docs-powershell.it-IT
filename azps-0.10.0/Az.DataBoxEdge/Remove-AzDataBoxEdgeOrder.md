---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 7ac5bce520e566208ddac18374ef01f2cff843ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863201"
---
# <span data-ttu-id="1a6cf-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1a6cf-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1a6cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6cf-103">Rimuove l'ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-103">Removes the order for a device.</span></span>

## <span data-ttu-id="1a6cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a6cf-104">SYNTAX</span></span>

### <span data-ttu-id="1a6cf-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a6cf-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6cf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a6cf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6cf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a6cf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a6cf-108">DESCRIPTION</span></span>
<span data-ttu-id="1a6cf-109">Il cmdlet **Remove-AzDataBoxEdgeOrder** Elimina un ordine esistente per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="1a6cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a6cf-110">EXAMPLES</span></span>

### <span data-ttu-id="1a6cf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a6cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="1a6cf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a6cf-112">PARAMETERS</span></span>

### <span data-ttu-id="1a6cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a6cf-113">-AsJob</span></span>
<span data-ttu-id="1a6cf-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1a6cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a6cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6cf-115">-DefaultProfile</span></span>
<span data-ttu-id="1a6cf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a6cf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1a6cf-117">-DeviceName</span></span>
<span data-ttu-id="1a6cf-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="1a6cf-118">Device Name</span></span>

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

### <span data-ttu-id="1a6cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a6cf-119">-InputObject</span></span>
<span data-ttu-id="1a6cf-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="1a6cf-120">Input Object</span></span>

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

### <span data-ttu-id="1a6cf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a6cf-121">-PassThru</span></span>
<span data-ttu-id="1a6cf-122">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1a6cf-122">returns true if successful</span></span>

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

### <span data-ttu-id="1a6cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a6cf-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1a6cf-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1a6cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6cf-125">-ResourceId</span></span>
<span data-ttu-id="1a6cf-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6cf-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1a6cf-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a6cf-127">-Confirm</span></span>
<span data-ttu-id="1a6cf-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6cf-129">-WhatIf</span></span>
<span data-ttu-id="1a6cf-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a6cf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6cf-132">CommonParameters</span></span>
<span data-ttu-id="1a6cf-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6cf-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a6cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6cf-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a6cf-135">INPUTS</span></span>

### <span data-ttu-id="1a6cf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1a6cf-136">System.String</span></span>

### <span data-ttu-id="1a6cf-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1a6cf-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1a6cf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a6cf-138">OUTPUTS</span></span>

### <span data-ttu-id="1a6cf-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1a6cf-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="1a6cf-140">Note</span><span class="sxs-lookup"><span data-stu-id="1a6cf-140">NOTES</span></span>

## <span data-ttu-id="1a6cf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a6cf-141">RELATED LINKS</span></span>
