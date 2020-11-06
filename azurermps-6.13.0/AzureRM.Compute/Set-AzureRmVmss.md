---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511803"
---
# <span data-ttu-id="4016b-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="4016b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4016b-102">SYNOPSIS</span></span>
<span data-ttu-id="4016b-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4016b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4016b-104">SYNTAX</span></span>

### <span data-ttu-id="4016b-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4016b-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4016b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="4016b-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4016b-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="4016b-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4016b-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="4016b-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4016b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4016b-109">DESCRIPTION</span></span>
<span data-ttu-id="4016b-110">Il cmdlet **set-AzureRmVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4016b-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4016b-111">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="4016b-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="4016b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4016b-112">EXAMPLES</span></span>

### <span data-ttu-id="4016b-113">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="4016b-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="4016b-114">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="4016b-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="4016b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4016b-115">PARAMETERS</span></span>

### <span data-ttu-id="4016b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4016b-116">-AsJob</span></span>
<span data-ttu-id="4016b-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4016b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4016b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4016b-118">-DefaultProfile</span></span>
<span data-ttu-id="4016b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4016b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4016b-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4016b-120">-InstanceId</span></span>
<span data-ttu-id="4016b-121">ID istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4016b-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4016b-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="4016b-122">-PerformMaintenance</span></span>
<span data-ttu-id="4016b-123">Indica che questo cmdlet esegue la manutenzione di una o più macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="4016b-124">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="4016b-124">-Redeploy</span></span>
<span data-ttu-id="4016b-125">Indica che il cmdlet ridistribuisce uno o più macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="4016b-126">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="4016b-126">-Reimage</span></span>
<span data-ttu-id="4016b-127">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="4016b-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="4016b-128">-ReimageAll</span></span>
<span data-ttu-id="4016b-129">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="4016b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4016b-130">-ResourceGroupName</span></span>
<span data-ttu-id="4016b-131">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="4016b-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4016b-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4016b-132">-VMScaleSetName</span></span>
<span data-ttu-id="4016b-133">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="4016b-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4016b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4016b-134">-Confirm</span></span>
<span data-ttu-id="4016b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4016b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4016b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4016b-136">-WhatIf</span></span>
<span data-ttu-id="4016b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4016b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4016b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4016b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4016b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4016b-139">CommonParameters</span></span>
<span data-ttu-id="4016b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4016b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4016b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4016b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4016b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4016b-142">INPUTS</span></span>

### <span data-ttu-id="4016b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4016b-143">System.String</span></span>

### <span data-ttu-id="4016b-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="4016b-144">System.String[]</span></span>

## <span data-ttu-id="4016b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4016b-145">OUTPUTS</span></span>

### <span data-ttu-id="4016b-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4016b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4016b-147">Note</span><span class="sxs-lookup"><span data-stu-id="4016b-147">NOTES</span></span>

## <span data-ttu-id="4016b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4016b-148">RELATED LINKS</span></span>

[<span data-ttu-id="4016b-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="4016b-150">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="4016b-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="4016b-152">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="4016b-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="4016b-154">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="4016b-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4016b-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


