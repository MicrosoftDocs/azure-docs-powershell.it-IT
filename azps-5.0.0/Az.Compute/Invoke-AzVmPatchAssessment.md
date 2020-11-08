---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200256"
---
# <span data-ttu-id="765f1-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="765f1-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="765f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="765f1-102">SYNOPSIS</span></span>
<span data-ttu-id="765f1-103">Valutare lo stato di patch di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="765f1-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="765f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="765f1-104">SYNTAX</span></span>

### <span data-ttu-id="765f1-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="765f1-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="765f1-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="765f1-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="765f1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="765f1-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="765f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="765f1-108">DESCRIPTION</span></span>
<span data-ttu-id="765f1-109">Valuta lo stato della patch di una VM e riporta tutte le patch rilevate disponibili per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="765f1-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="765f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="765f1-110">EXAMPLES</span></span>

### <span data-ttu-id="765f1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="765f1-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="765f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="765f1-112">PARAMETERS</span></span>

### <span data-ttu-id="765f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="765f1-113">-AsJob</span></span>
<span data-ttu-id="765f1-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="765f1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="765f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765f1-115">-DefaultProfile</span></span>
<span data-ttu-id="765f1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="765f1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="765f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="765f1-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="765f1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="765f1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="765f1-119">-ResourceId</span></span>
<span data-ttu-id="765f1-120">ID risorsa per la tua macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="765f1-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="765f1-121">-VM</span><span class="sxs-lookup"><span data-stu-id="765f1-121">-VM</span></span>
<span data-ttu-id="765f1-122">Oggetto macchina virtuale di PowerShell</span><span class="sxs-lookup"><span data-stu-id="765f1-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="765f1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="765f1-123">-VMName</span></span>
<span data-ttu-id="765f1-124">Nome macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="765f1-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="765f1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="765f1-125">-Confirm</span></span>
<span data-ttu-id="765f1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="765f1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="765f1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765f1-127">-WhatIf</span></span>
<span data-ttu-id="765f1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="765f1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="765f1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="765f1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="765f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765f1-130">CommonParameters</span></span>
<span data-ttu-id="765f1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765f1-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="765f1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765f1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="765f1-133">INPUTS</span></span>

### <span data-ttu-id="765f1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="765f1-134">System.String</span></span>

## <span data-ttu-id="765f1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="765f1-135">OUTPUTS</span></span>

### <span data-ttu-id="765f1-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="765f1-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="765f1-137">Note</span><span class="sxs-lookup"><span data-stu-id="765f1-137">NOTES</span></span>

## <span data-ttu-id="765f1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="765f1-138">RELATED LINKS</span></span>
