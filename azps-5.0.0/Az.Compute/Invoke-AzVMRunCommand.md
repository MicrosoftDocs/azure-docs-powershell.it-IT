---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200257"
---
# <span data-ttu-id="ba406-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ba406-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="ba406-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba406-102">SYNOPSIS</span></span>
<span data-ttu-id="ba406-103">Eseguire un comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="ba406-103">Run a command on the VM.</span></span>

## <span data-ttu-id="ba406-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba406-104">SYNTAX</span></span>

### <span data-ttu-id="ba406-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba406-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba406-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ba406-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba406-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="ba406-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba406-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba406-108">DESCRIPTION</span></span>
<span data-ttu-id="ba406-109">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="ba406-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="ba406-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba406-110">EXAMPLES</span></span>

### <span data-ttu-id="ba406-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba406-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="ba406-112">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="ba406-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="ba406-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba406-113">PARAMETERS</span></span>

### <span data-ttu-id="ba406-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba406-114">-AsJob</span></span>
<span data-ttu-id="ba406-115">Esegui cmdlet in background e restituisci un oggetto processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ba406-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="ba406-116">-CommandID</span><span class="sxs-lookup"><span data-stu-id="ba406-116">-CommandId</span></span>
<span data-ttu-id="ba406-117">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="ba406-117">The run command ID.</span></span>

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

### <span data-ttu-id="ba406-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba406-118">-DefaultProfile</span></span>
<span data-ttu-id="ba406-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba406-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba406-120">Parametro-</span><span class="sxs-lookup"><span data-stu-id="ba406-120">-Parameter</span></span>
<span data-ttu-id="ba406-121">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="ba406-121">The run command parameters.</span></span>

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

### <span data-ttu-id="ba406-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba406-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba406-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba406-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba406-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba406-124">-ResourceId</span></span>
<span data-ttu-id="ba406-125">ID risorsa per la VM.</span><span class="sxs-lookup"><span data-stu-id="ba406-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="ba406-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ba406-126">-ScriptPath</span></span>
<span data-ttu-id="ba406-127">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ba406-127">Path of the script to be executed.</span></span>  <span data-ttu-id="ba406-128">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="ba406-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="ba406-129">-VM</span><span class="sxs-lookup"><span data-stu-id="ba406-129">-VM</span></span>
<span data-ttu-id="ba406-130">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="ba406-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba406-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba406-131">-VMName</span></span>
<span data-ttu-id="ba406-132">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba406-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="ba406-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba406-133">-Confirm</span></span>
<span data-ttu-id="ba406-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba406-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba406-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba406-135">-WhatIf</span></span>
<span data-ttu-id="ba406-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba406-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba406-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba406-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba406-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba406-138">CommonParameters</span></span>
<span data-ttu-id="ba406-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba406-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba406-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba406-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba406-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba406-141">INPUTS</span></span>

### <span data-ttu-id="ba406-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ba406-142">System.String</span></span>

### <span data-ttu-id="ba406-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba406-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ba406-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba406-144">OUTPUTS</span></span>

### <span data-ttu-id="ba406-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="ba406-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="ba406-146">Note</span><span class="sxs-lookup"><span data-stu-id="ba406-146">NOTES</span></span>

## <span data-ttu-id="ba406-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba406-147">RELATED LINKS</span></span>
