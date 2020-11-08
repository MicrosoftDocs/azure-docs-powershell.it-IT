---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200255"
---
# <span data-ttu-id="931f5-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="931f5-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="931f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="931f5-102">SYNOPSIS</span></span>
<span data-ttu-id="931f5-103">Comando Esegui nella scala macchina virtuale imposta VM.</span><span class="sxs-lookup"><span data-stu-id="931f5-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="931f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="931f5-104">SYNTAX</span></span>

### <span data-ttu-id="931f5-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="931f5-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931f5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="931f5-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="931f5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="931f5-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="931f5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="931f5-108">DESCRIPTION</span></span>
<span data-ttu-id="931f5-109">Richiamare un comando Esegui nella scala macchina virtuale set VM.</span><span class="sxs-lookup"><span data-stu-id="931f5-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="931f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="931f5-110">EXAMPLES</span></span>

### <span data-ttu-id="931f5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="931f5-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="931f5-112">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri dell'ID "0" VM nel set di scale della macchina virtuale di "vmssname" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="931f5-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="931f5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="931f5-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="931f5-114">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri dell'ID "0" VM nel set di scale della macchina virtuale di "vmssname" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="931f5-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="931f5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="931f5-115">PARAMETERS</span></span>

### <span data-ttu-id="931f5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="931f5-116">-AsJob</span></span>
<span data-ttu-id="931f5-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="931f5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="931f5-118">-CommandID</span><span class="sxs-lookup"><span data-stu-id="931f5-118">-CommandId</span></span>
<span data-ttu-id="931f5-119">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="931f5-119">The run command id.</span></span>

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

### <span data-ttu-id="931f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931f5-120">-DefaultProfile</span></span>
<span data-ttu-id="931f5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="931f5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="931f5-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="931f5-122">-InstanceId</span></span>
<span data-ttu-id="931f5-123">ID istanza della scala macchina virtuale imposta VM.</span><span class="sxs-lookup"><span data-stu-id="931f5-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="931f5-124">Parametro-</span><span class="sxs-lookup"><span data-stu-id="931f5-124">-Parameter</span></span>
<span data-ttu-id="931f5-125">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="931f5-125">The run command parameters.</span></span>

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

### <span data-ttu-id="931f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="931f5-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="931f5-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="931f5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="931f5-128">-ResourceId</span></span>
<span data-ttu-id="931f5-129">ID risorsa per la scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="931f5-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="931f5-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="931f5-130">-ScriptPath</span></span>
<span data-ttu-id="931f5-131">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="931f5-131">Path of the script to be executed.</span></span>  <span data-ttu-id="931f5-132">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="931f5-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="931f5-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="931f5-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="931f5-134">Oggetto VM della scala della macchina virtuale set PS.</span><span class="sxs-lookup"><span data-stu-id="931f5-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="931f5-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="931f5-135">-VMScaleSetName</span></span>
<span data-ttu-id="931f5-136">Il nome della scala della macchina virtuale imposta VM.</span><span class="sxs-lookup"><span data-stu-id="931f5-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="931f5-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="931f5-137">-Confirm</span></span>
<span data-ttu-id="931f5-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="931f5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931f5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931f5-139">-WhatIf</span></span>
<span data-ttu-id="931f5-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="931f5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="931f5-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="931f5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931f5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931f5-142">CommonParameters</span></span>
<span data-ttu-id="931f5-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931f5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931f5-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="931f5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931f5-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="931f5-145">INPUTS</span></span>

### <span data-ttu-id="931f5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="931f5-146">System.String</span></span>

### <span data-ttu-id="931f5-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="931f5-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="931f5-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="931f5-148">OUTPUTS</span></span>

### <span data-ttu-id="931f5-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="931f5-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="931f5-150">Note</span><span class="sxs-lookup"><span data-stu-id="931f5-150">NOTES</span></span>

## <span data-ttu-id="931f5-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="931f5-151">RELATED LINKS</span></span>
