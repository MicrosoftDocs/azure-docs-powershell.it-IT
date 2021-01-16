---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355051"
---
# <span data-ttu-id="b9236-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b9236-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b9236-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9236-102">SYNOPSIS</span></span>
<span data-ttu-id="b9236-103">Rimuove una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="b9236-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b9236-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9236-104">SYNTAX</span></span>

### <span data-ttu-id="b9236-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9236-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9236-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9236-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9236-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9236-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9236-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9236-108">DESCRIPTION</span></span>
<span data-ttu-id="b9236-109">Il cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** rimuove la pianificazione della larghezza di banda per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="b9236-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="b9236-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9236-110">EXAMPLES</span></span>

### <span data-ttu-id="b9236-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9236-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="b9236-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9236-112">PARAMETERS</span></span>

### <span data-ttu-id="b9236-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9236-113">-AsJob</span></span>
<span data-ttu-id="b9236-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b9236-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9236-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9236-115">-DefaultProfile</span></span>
<span data-ttu-id="b9236-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9236-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9236-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b9236-117">-DeviceName</span></span>
<span data-ttu-id="b9236-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="b9236-118">Device Name</span></span>

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

### <span data-ttu-id="b9236-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9236-119">-InputObject</span></span>
<span data-ttu-id="b9236-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="b9236-120">Input Object</span></span>

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

### <span data-ttu-id="b9236-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9236-121">-Name</span></span>
<span data-ttu-id="b9236-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="b9236-122">Resource Name</span></span>

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

### <span data-ttu-id="b9236-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9236-123">-PassThru</span></span>
<span data-ttu-id="b9236-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="b9236-124">returns true if successful</span></span>

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

### <span data-ttu-id="b9236-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9236-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9236-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b9236-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b9236-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9236-127">-ResourceId</span></span>
<span data-ttu-id="b9236-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9236-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b9236-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9236-129">-Confirm</span></span>
<span data-ttu-id="b9236-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9236-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9236-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9236-131">-WhatIf</span></span>
<span data-ttu-id="b9236-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9236-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9236-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9236-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9236-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9236-134">CommonParameters</span></span>
<span data-ttu-id="b9236-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9236-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9236-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9236-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9236-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9236-137">INPUTS</span></span>

### <span data-ttu-id="b9236-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9236-138">System.String</span></span>

### <span data-ttu-id="b9236-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b9236-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b9236-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9236-140">OUTPUTS</span></span>

### <span data-ttu-id="b9236-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9236-141">System.Boolean</span></span>

## <span data-ttu-id="b9236-142">Note</span><span class="sxs-lookup"><span data-stu-id="b9236-142">NOTES</span></span>

## <span data-ttu-id="b9236-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9236-143">RELATED LINKS</span></span>
