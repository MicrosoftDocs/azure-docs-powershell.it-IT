---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: ea4674adaf1069a4681ab4943ad16685540378ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980894"
---
# <span data-ttu-id="2df63-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2df63-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="2df63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2df63-102">SYNOPSIS</span></span>
<span data-ttu-id="2df63-103">Comando Esegui nella macchina virtuale per il set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2df63-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2df63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2df63-104">SYNTAX</span></span>

### <span data-ttu-id="2df63-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="2df63-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2df63-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2df63-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2df63-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2df63-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df63-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2df63-108">DESCRIPTION</span></span>
<span data-ttu-id="2df63-109">Richiamare un comando Esegui nella macchina virtuale per il set di scalabilità delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2df63-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2df63-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2df63-110">EXAMPLES</span></span>

### <span data-ttu-id="2df63-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2df63-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2df63-112">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script 'sample.ps1' e dei parametri per la macchina virtuale '0' nel set di scala della macchina virtuale di 'vmssname' nel gruppo di risorse 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="2df63-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="2df63-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2df63-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2df63-114">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script 'sample.ps1' e dei parametri per la macchina virtuale '0' nel set di scala della macchina virtuale di 'vmssname' nel gruppo di risorse 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="2df63-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="2df63-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2df63-115">PARAMETERS</span></span>

### <span data-ttu-id="2df63-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2df63-116">-AsJob</span></span>
<span data-ttu-id="2df63-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2df63-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2df63-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2df63-118">-CommandId</span></span>
<span data-ttu-id="2df63-119">ID del comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="2df63-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df63-120">-DefaultProfile</span></span>
<span data-ttu-id="2df63-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2df63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df63-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2df63-122">-InstanceId</span></span>
<span data-ttu-id="2df63-123">ID istanza della macchina virtuale impostata per il set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2df63-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df63-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2df63-124">-Parameter</span></span>
<span data-ttu-id="2df63-125">I parametri del comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="2df63-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df63-126">-ResourceGroupName</span></span>
<span data-ttu-id="2df63-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2df63-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2df63-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2df63-128">-ResourceId</span></span>
<span data-ttu-id="2df63-129">ID risorsa per la macchina virtuale impostata per il set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2df63-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="2df63-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="2df63-130">-ScriptPath</span></span>
<span data-ttu-id="2df63-131">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2df63-131">Path of the script to be executed.</span></span>  <span data-ttu-id="2df63-132">Quando viene assegnato questo valore, lo script specificato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="2df63-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df63-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2df63-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2df63-134">Oggetto VM set di scalabilità della macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="2df63-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2df63-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2df63-135">-VMScaleSetName</span></span>
<span data-ttu-id="2df63-136">Nome della macchina virtuale per il set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2df63-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="2df63-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2df63-137">-Confirm</span></span>
<span data-ttu-id="2df63-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df63-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df63-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df63-139">-WhatIf</span></span>
<span data-ttu-id="2df63-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2df63-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df63-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2df63-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df63-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df63-142">CommonParameters</span></span>
<span data-ttu-id="2df63-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df63-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df63-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2df63-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df63-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="2df63-145">INPUTS</span></span>

### <span data-ttu-id="2df63-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2df63-146">System.String</span></span>

### <span data-ttu-id="2df63-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2df63-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2df63-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2df63-148">OUTPUTS</span></span>

### <span data-ttu-id="2df63-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="2df63-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="2df63-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="2df63-150">NOTES</span></span>

## <span data-ttu-id="2df63-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2df63-151">RELATED LINKS</span></span>
