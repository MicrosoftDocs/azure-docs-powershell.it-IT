---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: ce71ad0e82e7082c199d4823c3a3a59be972ec60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675154"
---
# <span data-ttu-id="cd05a-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-101">Set-AzVmss</span></span>

## <span data-ttu-id="cd05a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd05a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd05a-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="cd05a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd05a-104">SYNTAX</span></span>

### <span data-ttu-id="cd05a-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd05a-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd05a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cd05a-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd05a-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="cd05a-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd05a-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="cd05a-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd05a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd05a-109">DESCRIPTION</span></span>
<span data-ttu-id="cd05a-110">Il cmdlet **set-AzVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cd05a-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cd05a-111">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="cd05a-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="cd05a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd05a-112">EXAMPLES</span></span>

### <span data-ttu-id="cd05a-113">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="cd05a-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="cd05a-114">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="cd05a-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="cd05a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd05a-115">PARAMETERS</span></span>

### <span data-ttu-id="cd05a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd05a-116">-AsJob</span></span>
<span data-ttu-id="cd05a-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="cd05a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cd05a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd05a-118">-DefaultProfile</span></span>
<span data-ttu-id="cd05a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd05a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd05a-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cd05a-120">-InstanceId</span></span>
<span data-ttu-id="cd05a-121">ID istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd05a-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="cd05a-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="cd05a-122">-PerformMaintenance</span></span>
<span data-ttu-id="cd05a-123">Indica che questo cmdlet esegue la manutenzione di una o più macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd05a-124">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="cd05a-124">-Redeploy</span></span>
<span data-ttu-id="cd05a-125">Indica che il cmdlet ridistribuisce uno o più macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd05a-126">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="cd05a-126">-Reimage</span></span>
<span data-ttu-id="cd05a-127">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd05a-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="cd05a-128">-ReimageAll</span></span>
<span data-ttu-id="cd05a-129">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="cd05a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd05a-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd05a-131">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="cd05a-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="cd05a-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="cd05a-132">-TempDisk</span></span>
<span data-ttu-id="cd05a-133">Specifica se riimmagine del disco Temp.</span><span class="sxs-lookup"><span data-stu-id="cd05a-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd05a-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd05a-134">-VMScaleSetName</span></span>
<span data-ttu-id="cd05a-135">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="cd05a-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="cd05a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd05a-136">-Confirm</span></span>
<span data-ttu-id="cd05a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd05a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd05a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd05a-138">-WhatIf</span></span>
<span data-ttu-id="cd05a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd05a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd05a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd05a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd05a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd05a-141">CommonParameters</span></span>
<span data-ttu-id="cd05a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd05a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd05a-143">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd05a-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd05a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd05a-144">INPUTS</span></span>

### <span data-ttu-id="cd05a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cd05a-145">System.String</span></span>

### <span data-ttu-id="cd05a-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="cd05a-146">System.String[]</span></span>

## <span data-ttu-id="cd05a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd05a-147">OUTPUTS</span></span>

### <span data-ttu-id="cd05a-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cd05a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd05a-149">Note</span><span class="sxs-lookup"><span data-stu-id="cd05a-149">NOTES</span></span>

## <span data-ttu-id="cd05a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd05a-150">RELATED LINKS</span></span>

[<span data-ttu-id="cd05a-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="cd05a-152">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="cd05a-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="cd05a-154">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="cd05a-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="cd05a-156">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="cd05a-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd05a-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


