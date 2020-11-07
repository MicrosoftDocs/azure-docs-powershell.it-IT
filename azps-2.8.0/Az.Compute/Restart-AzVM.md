---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675225"
---
# <span data-ttu-id="f6a6c-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-101">Restart-AzVM</span></span>

## <span data-ttu-id="f6a6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a6c-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f6a6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6a6c-104">SYNTAX</span></span>

### <span data-ttu-id="f6a6c-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6a6c-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a6c-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6a6c-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a6c-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6a6c-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6a6c-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6a6c-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a6c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a6c-109">DESCRIPTION</span></span>
<span data-ttu-id="f6a6c-110">Il cmdlet **Restart-AzVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f6a6c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6a6c-111">EXAMPLES</span></span>

### <span data-ttu-id="f6a6c-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f6a6c-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f6a6c-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f6a6c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6a6c-114">PARAMETERS</span></span>

### <span data-ttu-id="f6a6c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6a6c-115">-AsJob</span></span>
<span data-ttu-id="f6a6c-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f6a6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a6c-117">-DefaultProfile</span></span>
<span data-ttu-id="f6a6c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a6c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f6a6c-119">-Id</span></span>
<span data-ttu-id="f6a6c-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a6c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6a6c-121">-Name</span></span>
<span data-ttu-id="f6a6c-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a6c-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="f6a6c-123">-NoWait</span></span>
<span data-ttu-id="f6a6c-124">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f6a6c-125">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f6a6c-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f6a6c-126">-PerformMaintenance</span></span>
<span data-ttu-id="f6a6c-127">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="f6a6c-129">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a6c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6a6c-130">-Confirm</span></span>
<span data-ttu-id="f6a6c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a6c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a6c-132">-WhatIf</span></span>
<span data-ttu-id="f6a6c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6a6c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a6c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a6c-135">CommonParameters</span></span>
<span data-ttu-id="f6a6c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a6c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a6c-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6a6c-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a6c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6a6c-138">INPUTS</span></span>

### <span data-ttu-id="f6a6c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f6a6c-139">System.String</span></span>

### <span data-ttu-id="f6a6c-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6a6c-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f6a6c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6a6c-141">OUTPUTS</span></span>

### <span data-ttu-id="f6a6c-142">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f6a6c-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="f6a6c-143">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f6a6c-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f6a6c-144">Note</span><span class="sxs-lookup"><span data-stu-id="f6a6c-144">NOTES</span></span>

## <span data-ttu-id="f6a6c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6a6c-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6a6c-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f6a6c-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f6a6c-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f6a6c-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f6a6c-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f6a6c-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6a6c-151">Update-AzVM</span></span>](./Update-AzVM.md)


