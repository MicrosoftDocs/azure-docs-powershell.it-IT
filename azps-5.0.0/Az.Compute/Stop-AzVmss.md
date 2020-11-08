---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200232"
---
# <span data-ttu-id="b03ad-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-101">Stop-AzVmss</span></span>

## <span data-ttu-id="b03ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b03ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b03ad-103">Interrompe VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="b03ad-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="b03ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b03ad-104">SYNTAX</span></span>

### <span data-ttu-id="b03ad-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b03ad-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b03ad-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b03ad-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b03ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b03ad-107">DESCRIPTION</span></span>
<span data-ttu-id="b03ad-108">Il cmdlet **Stop-AzVmss** arresta tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b03ad-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="b03ad-109">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b03ad-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="b03ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b03ad-110">EXAMPLES</span></span>

### <span data-ttu-id="b03ad-111">Esempio 1: arrestare tutte le macchine virtuali in VMSS</span><span class="sxs-lookup"><span data-stu-id="b03ad-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b03ad-112">Questo comando Arresta tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="b03ad-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="b03ad-113">Esempio 2: arrestare un set specifico di macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="b03ad-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="b03ad-114">Questo comando Arresta un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="b03ad-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b03ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b03ad-115">PARAMETERS</span></span>

### <span data-ttu-id="b03ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b03ad-116">-AsJob</span></span>
<span data-ttu-id="b03ad-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b03ad-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b03ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03ad-118">-DefaultProfile</span></span>
<span data-ttu-id="b03ad-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b03ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b03ad-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b03ad-120">-Force</span></span>
<span data-ttu-id="b03ad-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b03ad-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b03ad-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b03ad-122">-InstanceId</span></span>
<span data-ttu-id="b03ad-123">Specifica come matrice di stringhe l'ID o gli ID delle istanze della macchina virtuale arrestate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03ad-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="b03ad-124">Ad esempio: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="b03ad-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="b03ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="b03ad-126">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="b03ad-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b03ad-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="b03ad-127">-SkipShutdown</span></span>
<span data-ttu-id="b03ad-128">Per richiedere l'arresto di VM non grazioso</span><span class="sxs-lookup"><span data-stu-id="b03ad-128">To request non-graceful VM shutdown</span></span>

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

### <span data-ttu-id="b03ad-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b03ad-129">-StayProvisioned</span></span>
<span data-ttu-id="b03ad-130">Se specificato, la macchina virtuale entrerà nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="b03ad-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="b03ad-131">Se non viene specificato, la macchina virtuale immetterà lo stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="b03ad-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="b03ad-132">L'utente viene ancora addebitato per le VM nello stato Stopped ma non per le VM in stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="b03ad-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="b03ad-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b03ad-133">-VMScaleSetName</span></span>
<span data-ttu-id="b03ad-134">Specifica il nome del VMSS per cui questo cmdlet arresta le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b03ad-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="b03ad-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b03ad-135">-Confirm</span></span>
<span data-ttu-id="b03ad-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03ad-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03ad-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03ad-137">-WhatIf</span></span>
<span data-ttu-id="b03ad-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b03ad-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b03ad-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b03ad-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03ad-140">CommonParameters</span></span>
<span data-ttu-id="b03ad-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03ad-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b03ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03ad-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b03ad-143">INPUTS</span></span>

### <span data-ttu-id="b03ad-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b03ad-144">System.String</span></span>

### <span data-ttu-id="b03ad-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="b03ad-145">System.String[]</span></span>

## <span data-ttu-id="b03ad-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b03ad-146">OUTPUTS</span></span>

### <span data-ttu-id="b03ad-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b03ad-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b03ad-148">Note</span><span class="sxs-lookup"><span data-stu-id="b03ad-148">NOTES</span></span>

## <span data-ttu-id="b03ad-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b03ad-149">RELATED LINKS</span></span>

[<span data-ttu-id="b03ad-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="b03ad-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b03ad-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b03ad-153">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b03ad-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b03ad-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b03ad-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b03ad-156">Update-AzVmss</span></span>](./Update-AzVmss.md)

