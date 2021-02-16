---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204826"
---
# <span data-ttu-id="f2407-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f2407-101">Restart-AzVM</span></span>

## <span data-ttu-id="f2407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2407-102">SYNOPSIS</span></span>
<span data-ttu-id="f2407-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2407-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f2407-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2407-104">SYNTAX</span></span>

### <span data-ttu-id="f2407-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2407-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2407-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f2407-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2407-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f2407-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2407-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f2407-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2407-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2407-109">DESCRIPTION</span></span>
<span data-ttu-id="f2407-110">Il cmdlet **Restart-AzVM** riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2407-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f2407-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2407-111">EXAMPLES</span></span>

### <span data-ttu-id="f2407-112">Esempio 1: Riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f2407-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f2407-113">Questo comando riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2407-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f2407-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2407-114">PARAMETERS</span></span>

### <span data-ttu-id="f2407-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2407-115">-AsJob</span></span>
<span data-ttu-id="f2407-116">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f2407-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f2407-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2407-117">-DefaultProfile</span></span>
<span data-ttu-id="f2407-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2407-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2407-119">-Id</span><span class="sxs-lookup"><span data-stu-id="f2407-119">-Id</span></span>
<span data-ttu-id="f2407-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2407-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f2407-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f2407-121">-Name</span></span>
<span data-ttu-id="f2407-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2407-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="f2407-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2407-123">-NoWait</span></span>
<span data-ttu-id="f2407-124">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f2407-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f2407-125">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="f2407-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f2407-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f2407-126">-PerformMaintenance</span></span>
<span data-ttu-id="f2407-127">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2407-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="f2407-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2407-128">-ResourceGroupName</span></span>
<span data-ttu-id="f2407-129">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2407-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f2407-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2407-130">-Confirm</span></span>
<span data-ttu-id="f2407-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2407-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2407-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2407-132">-WhatIf</span></span>
<span data-ttu-id="f2407-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2407-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2407-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2407-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2407-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2407-135">CommonParameters</span></span>
<span data-ttu-id="f2407-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2407-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2407-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2407-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2407-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2407-138">INPUTS</span></span>

### <span data-ttu-id="f2407-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f2407-139">System.String</span></span>

### <span data-ttu-id="f2407-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f2407-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2407-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2407-141">OUTPUTS</span></span>

### <span data-ttu-id="f2407-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f2407-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="f2407-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2407-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2407-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2407-144">NOTES</span></span>

## <span data-ttu-id="f2407-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2407-145">RELATED LINKS</span></span>

[<span data-ttu-id="f2407-146">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="f2407-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f2407-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f2407-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f2407-148">Remove-AZVM</span><span class="sxs-lookup"><span data-stu-id="f2407-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f2407-149">Start-AZVM</span><span class="sxs-lookup"><span data-stu-id="f2407-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f2407-150">Stop-AZVM</span><span class="sxs-lookup"><span data-stu-id="f2407-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f2407-151">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="f2407-151">Update-AzVM</span></span>](./Update-AzVM.md)


