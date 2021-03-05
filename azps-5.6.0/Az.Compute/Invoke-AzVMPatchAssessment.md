---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985303"
---
# <span data-ttu-id="e430e-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="e430e-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="e430e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e430e-102">SYNOPSIS</span></span>
<span data-ttu-id="e430e-103">Valutare lo stato delle patch di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e430e-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="e430e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e430e-104">SYNTAX</span></span>

### <span data-ttu-id="e430e-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e430e-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e430e-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="e430e-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e430e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e430e-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e430e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e430e-108">DESCRIPTION</span></span>
<span data-ttu-id="e430e-109">Valuta lo stato delle patch di una macchina virtuale e segnala tutte le patch rilevate disponibili per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e430e-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="e430e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e430e-110">EXAMPLES</span></span>

### <span data-ttu-id="e430e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e430e-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="e430e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e430e-112">PARAMETERS</span></span>

### <span data-ttu-id="e430e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e430e-113">-AsJob</span></span>
<span data-ttu-id="e430e-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e430e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e430e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e430e-115">-DefaultProfile</span></span>
<span data-ttu-id="e430e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e430e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e430e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e430e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e430e-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e430e-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e430e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e430e-119">-ResourceId</span></span>
<span data-ttu-id="e430e-120">ID risorsa per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e430e-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e430e-121">-VM</span><span class="sxs-lookup"><span data-stu-id="e430e-121">-VM</span></span>
<span data-ttu-id="e430e-122">Oggetto Macchina virtuale di PowerShell</span><span class="sxs-lookup"><span data-stu-id="e430e-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e430e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="e430e-123">-VMName</span></span>
<span data-ttu-id="e430e-124">Nome della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e430e-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e430e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e430e-125">-Confirm</span></span>
<span data-ttu-id="e430e-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e430e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e430e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e430e-127">-WhatIf</span></span>
<span data-ttu-id="e430e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e430e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e430e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e430e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e430e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e430e-130">CommonParameters</span></span>
<span data-ttu-id="e430e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e430e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e430e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e430e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e430e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e430e-133">INPUTS</span></span>

### <span data-ttu-id="e430e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e430e-134">System.String</span></span>

## <span data-ttu-id="e430e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e430e-135">OUTPUTS</span></span>

### <span data-ttu-id="e430e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="e430e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="e430e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e430e-137">NOTES</span></span>

## <span data-ttu-id="e430e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e430e-138">RELATED LINKS</span></span>
