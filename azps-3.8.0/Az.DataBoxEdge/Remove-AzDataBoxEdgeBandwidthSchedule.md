---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022533"
---
# <span data-ttu-id="4b520-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4b520-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="4b520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b520-102">SYNOPSIS</span></span>
<span data-ttu-id="4b520-103">Rimuove una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="4b520-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="4b520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b520-104">SYNTAX</span></span>

### <span data-ttu-id="4b520-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b520-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b520-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b520-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b520-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b520-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b520-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b520-108">DESCRIPTION</span></span>
<span data-ttu-id="4b520-109">Il cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** rimuove la pianificazione della larghezza di banda per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="4b520-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="4b520-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b520-110">EXAMPLES</span></span>

### <span data-ttu-id="4b520-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b520-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="4b520-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b520-112">PARAMETERS</span></span>

### <span data-ttu-id="4b520-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b520-113">-AsJob</span></span>
<span data-ttu-id="4b520-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4b520-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b520-115">-DefaultProfile</span></span>
<span data-ttu-id="4b520-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b520-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b520-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4b520-117">-DeviceName</span></span>
<span data-ttu-id="4b520-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b520-118">Device Name</span></span>

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

### <span data-ttu-id="4b520-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b520-119">-InputObject</span></span>
<span data-ttu-id="4b520-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="4b520-120">Input Object</span></span>

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

### <span data-ttu-id="4b520-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b520-121">-Name</span></span>
<span data-ttu-id="4b520-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="4b520-122">Resource Name</span></span>

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

### <span data-ttu-id="4b520-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b520-123">-PassThru</span></span>
<span data-ttu-id="4b520-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4b520-124">returns true if successful</span></span>

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

### <span data-ttu-id="4b520-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b520-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b520-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4b520-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4b520-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b520-127">-ResourceId</span></span>
<span data-ttu-id="4b520-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b520-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="4b520-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b520-129">-Confirm</span></span>
<span data-ttu-id="4b520-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b520-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b520-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b520-131">-WhatIf</span></span>
<span data-ttu-id="4b520-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b520-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b520-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b520-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b520-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b520-134">CommonParameters</span></span>
<span data-ttu-id="4b520-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b520-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b520-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b520-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b520-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b520-137">INPUTS</span></span>

### <span data-ttu-id="4b520-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4b520-138">System.String</span></span>

### <span data-ttu-id="4b520-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="4b520-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="4b520-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b520-140">OUTPUTS</span></span>

### <span data-ttu-id="4b520-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b520-141">System.Boolean</span></span>

## <span data-ttu-id="4b520-142">Note</span><span class="sxs-lookup"><span data-stu-id="4b520-142">NOTES</span></span>

## <span data-ttu-id="4b520-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b520-143">RELATED LINKS</span></span>
