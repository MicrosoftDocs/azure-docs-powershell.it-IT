---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 0371dd5ba008089ff8d8731e0ebb30e6b3caf8fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983278"
---
# <span data-ttu-id="baac9-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="baac9-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="baac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baac9-102">SYNOPSIS</span></span>
<span data-ttu-id="baac9-103">Annulla l'aggiornamento del set di scalabilità delle macchine virtuali corrente.</span><span class="sxs-lookup"><span data-stu-id="baac9-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="baac9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="baac9-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baac9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="baac9-105">DESCRIPTION</span></span>
<span data-ttu-id="baac9-106">Annulla l'aggiornamento del set di scalabilità delle macchine virtuali corrente.</span><span class="sxs-lookup"><span data-stu-id="baac9-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="baac9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="baac9-107">EXAMPLES</span></span>

### <span data-ttu-id="baac9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="baac9-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="baac9-109">Questo comando annulla l'aggiornamento in corso del set di scalabilità della macchina virtuale "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="baac9-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="baac9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baac9-110">PARAMETERS</span></span>

### <span data-ttu-id="baac9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baac9-111">-AsJob</span></span>
<span data-ttu-id="baac9-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="baac9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baac9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baac9-113">-DefaultProfile</span></span>
<span data-ttu-id="baac9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="baac9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baac9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="baac9-115">-Force</span></span>
<span data-ttu-id="baac9-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="baac9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="baac9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baac9-117">-ResourceGroupName</span></span>
<span data-ttu-id="baac9-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="baac9-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baac9-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="baac9-119">-VMScaleSetName</span></span>
<span data-ttu-id="baac9-120">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="baac9-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baac9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baac9-121">-Confirm</span></span>
<span data-ttu-id="baac9-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baac9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baac9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baac9-123">-WhatIf</span></span>
<span data-ttu-id="baac9-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baac9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baac9-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baac9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baac9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baac9-126">CommonParameters</span></span>
<span data-ttu-id="baac9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baac9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baac9-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="baac9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baac9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="baac9-129">INPUTS</span></span>

### <span data-ttu-id="baac9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="baac9-130">System.String</span></span>

## <span data-ttu-id="baac9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="baac9-131">OUTPUTS</span></span>

### <span data-ttu-id="baac9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="baac9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="baac9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="baac9-133">NOTES</span></span>

## <span data-ttu-id="baac9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="baac9-134">RELATED LINKS</span></span>
