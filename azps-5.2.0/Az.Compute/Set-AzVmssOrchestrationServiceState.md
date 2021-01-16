---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358606"
---
# <span data-ttu-id="5a4d6-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="5a4d6-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="5a4d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4d6-103">Imposta lo stato del servizio di orchestrazione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="5a4d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a4d6-104">SYNTAX</span></span>

### <span data-ttu-id="5a4d6-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a4d6-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4d6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5a4d6-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4d6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5a4d6-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4d6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a4d6-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4d6-109">Imposta lo stato del servizio di orchestrazione per VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="5a4d6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a4d6-110">EXAMPLES</span></span>

### <span data-ttu-id="5a4d6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a4d6-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="5a4d6-112">Questo comando sospende il servizio di riparazione automatica nel VMSS "vmss1" nel gruppo di risorse "RG".</span><span class="sxs-lookup"><span data-stu-id="5a4d6-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="5a4d6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5a4d6-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="5a4d6-114">Questo comando riprende il servizio di riparazione automatica nel VMSS "vmss1" nel gruppo di risorse "RG".</span><span class="sxs-lookup"><span data-stu-id="5a4d6-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="5a4d6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a4d6-115">PARAMETERS</span></span>

### <span data-ttu-id="5a4d6-116">-Azione</span><span class="sxs-lookup"><span data-stu-id="5a4d6-116">-Action</span></span>
<span data-ttu-id="5a4d6-117">Azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-117">The action to be performed.</span></span>  <span data-ttu-id="5a4d6-118">I valori possibili sono: Resume, Suspend.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a4d6-119">-AsJob</span></span>
<span data-ttu-id="5a4d6-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5a4d6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a4d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4d6-121">-DefaultProfile</span></span>
<span data-ttu-id="5a4d6-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4d6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4d6-123">-InputObject</span></span>
<span data-ttu-id="5a4d6-124">Oggetto local del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a4d6-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4d6-127">-ResourceId</span></span>
<span data-ttu-id="5a4d6-128">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5a4d6-129">-ServiceName</span></span>
<span data-ttu-id="5a4d6-130">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5a4d6-131">-VMScaleSetName</span></span>
<span data-ttu-id="5a4d6-132">Nome del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-132">The name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a4d6-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a4d6-133">-Confirm</span></span>
<span data-ttu-id="5a4d6-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4d6-135">-WhatIf</span></span>
<span data-ttu-id="5a4d6-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4d6-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4d6-138">CommonParameters</span></span>
<span data-ttu-id="5a4d6-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4d6-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a4d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4d6-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a4d6-141">INPUTS</span></span>

### <span data-ttu-id="5a4d6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5a4d6-142">System.String</span></span>

### <span data-ttu-id="5a4d6-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a4d6-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5a4d6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a4d6-144">OUTPUTS</span></span>

### <span data-ttu-id="5a4d6-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5a4d6-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5a4d6-146">Note</span><span class="sxs-lookup"><span data-stu-id="5a4d6-146">NOTES</span></span>

## <span data-ttu-id="5a4d6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a4d6-147">RELATED LINKS</span></span>
