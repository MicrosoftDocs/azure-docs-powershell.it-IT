---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177463"
---
# <span data-ttu-id="22445-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-101">Stop-AzVmss</span></span>

## <span data-ttu-id="22445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22445-102">SYNOPSIS</span></span>
<span data-ttu-id="22445-103">Arresta il sistema VMSS o un set di macchine virtuali all'interno del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="22445-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="22445-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22445-104">SYNTAX</span></span>

### <span data-ttu-id="22445-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="22445-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22445-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="22445-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22445-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22445-107">DESCRIPTION</span></span>
<span data-ttu-id="22445-108">Il cmdlet **Stop-AzVmss** interrompe tutte le macchine virtuali nel set di scalabilità macchina virtuale (VMSS) o in un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="22445-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="22445-109">È possibile usare il *parametro InstanceId* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="22445-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="22445-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22445-110">EXAMPLES</span></span>

### <span data-ttu-id="22445-111">Esempio 1: Arrestare tutte le macchine virtuali nel sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="22445-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="22445-112">Questo comando arresta tutte le macchine virtuali che appartengono a VMSS denominate ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="22445-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="22445-113">Esempio 2: Arrestare un set specifico di macchine virtuali all'interno del sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="22445-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="22445-114">Questo comando interrompe un set specifico di macchine virtuali specificato dalla matrice della stringa di ID di istanza che appartengono al sistema VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="22445-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="22445-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22445-115">PARAMETERS</span></span>

### <span data-ttu-id="22445-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22445-116">-AsJob</span></span>
<span data-ttu-id="22445-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="22445-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22445-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22445-118">-DefaultProfile</span></span>
<span data-ttu-id="22445-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22445-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22445-120">-Force</span><span class="sxs-lookup"><span data-stu-id="22445-120">-Force</span></span>
<span data-ttu-id="22445-121">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="22445-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22445-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="22445-122">-InstanceId</span></span>
<span data-ttu-id="22445-123">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze della macchina virtuale arrestate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22445-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="22445-124">Ad esempio: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="22445-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22445-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22445-125">-ResourceGroupName</span></span>
<span data-ttu-id="22445-126">Specifica il nome del gruppo di risorse del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="22445-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="22445-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="22445-127">-SkipShutdown</span></span>
<span data-ttu-id="22445-128">Per richiedere l'arresto non graceful della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="22445-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22445-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="22445-129">-StayProvisioned</span></span>
<span data-ttu-id="22445-130">Se specificato, la macchina virtuale entra nello stato di interruzione.</span><span class="sxs-lookup"><span data-stu-id="22445-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="22445-131">Se non viene specificato, la macchina virtuale entra nello stato arrestato deassegnato.</span><span class="sxs-lookup"><span data-stu-id="22445-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="22445-132">L'addebito per le macchine virtuali è ancora in stato di interruzione, ma non per le macchine virtuali con stato di deassegnazione interrotta.</span><span class="sxs-lookup"><span data-stu-id="22445-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22445-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="22445-133">-VMScaleSetName</span></span>
<span data-ttu-id="22445-134">Specifica il nome del sistema VMS per cui questo cmdlet arresta le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="22445-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="22445-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22445-135">-Confirm</span></span>
<span data-ttu-id="22445-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22445-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22445-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22445-137">-WhatIf</span></span>
<span data-ttu-id="22445-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22445-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22445-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22445-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22445-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22445-140">CommonParameters</span></span>
<span data-ttu-id="22445-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22445-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22445-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22445-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22445-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="22445-143">INPUTS</span></span>

### <span data-ttu-id="22445-144">System.String</span><span class="sxs-lookup"><span data-stu-id="22445-144">System.String</span></span>

### <span data-ttu-id="22445-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22445-145">System.String[]</span></span>

## <span data-ttu-id="22445-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22445-146">OUTPUTS</span></span>

### <span data-ttu-id="22445-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="22445-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="22445-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="22445-148">NOTES</span></span>

## <span data-ttu-id="22445-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22445-149">RELATED LINKS</span></span>

[<span data-ttu-id="22445-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="22445-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="22445-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="22445-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="22445-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="22445-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="22445-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22445-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


