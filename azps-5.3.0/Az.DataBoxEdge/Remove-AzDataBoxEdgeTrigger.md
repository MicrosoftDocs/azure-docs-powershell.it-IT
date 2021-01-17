---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487680"
---
# <span data-ttu-id="dcbdd-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dcbdd-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dcbdd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcbdd-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbdd-103">Rimuove un trigger esistente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="dcbdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcbdd-104">SYNTAX</span></span>

### <span data-ttu-id="dcbdd-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcbdd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcbdd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbdd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcbdd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbdd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcbdd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcbdd-108">DESCRIPTION</span></span>
<span data-ttu-id="dcbdd-109">Il cmdlet **Remove-AzDataBoxEdgeTrigger** rimuove un trigger esistente nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="dcbdd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcbdd-110">EXAMPLES</span></span>

### <span data-ttu-id="dcbdd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dcbdd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="dcbdd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcbdd-112">PARAMETERS</span></span>

### <span data-ttu-id="dcbdd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcbdd-113">-AsJob</span></span>
<span data-ttu-id="dcbdd-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dcbdd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcbdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbdd-115">-DefaultProfile</span></span>
<span data-ttu-id="dcbdd-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcbdd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dcbdd-117">-DeviceName</span></span>
<span data-ttu-id="dcbdd-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="dcbdd-118">Device Name</span></span>

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

### <span data-ttu-id="dcbdd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcbdd-119">-InputObject</span></span>
<span data-ttu-id="dcbdd-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="dcbdd-120">Input Object</span></span>

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

### <span data-ttu-id="dcbdd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcbdd-121">-Name</span></span>
<span data-ttu-id="dcbdd-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="dcbdd-122">Resource Name</span></span>

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

### <span data-ttu-id="dcbdd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcbdd-123">-PassThru</span></span>
<span data-ttu-id="dcbdd-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="dcbdd-124">returns true if successful</span></span>

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

### <span data-ttu-id="dcbdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="dcbdd-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dcbdd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dcbdd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbdd-127">-ResourceId</span></span>
<span data-ttu-id="dcbdd-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbdd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="dcbdd-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dcbdd-129">-Confirm</span></span>
<span data-ttu-id="dcbdd-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcbdd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcbdd-131">-WhatIf</span></span>
<span data-ttu-id="dcbdd-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcbdd-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcbdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbdd-134">CommonParameters</span></span>
<span data-ttu-id="dcbdd-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbdd-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcbdd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbdd-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcbdd-137">INPUTS</span></span>

### <span data-ttu-id="dcbdd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dcbdd-138">System.String</span></span>

### <span data-ttu-id="dcbdd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dcbdd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dcbdd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcbdd-140">OUTPUTS</span></span>

### <span data-ttu-id="dcbdd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dcbdd-141">System.Boolean</span></span>

## <span data-ttu-id="dcbdd-142">Note</span><span class="sxs-lookup"><span data-stu-id="dcbdd-142">NOTES</span></span>

## <span data-ttu-id="dcbdd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcbdd-143">RELATED LINKS</span></span>
