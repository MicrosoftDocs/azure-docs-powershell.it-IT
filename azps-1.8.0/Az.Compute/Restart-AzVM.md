---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 5f2c7d4c3a047a4893158e7f1a12b375106d640b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684726"
---
# <span data-ttu-id="e93dc-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-101">Restart-AzVM</span></span>

## <span data-ttu-id="e93dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e93dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e93dc-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e93dc-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e93dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e93dc-104">SYNTAX</span></span>

### <span data-ttu-id="e93dc-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e93dc-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93dc-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e93dc-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93dc-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e93dc-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93dc-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e93dc-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93dc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e93dc-109">DESCRIPTION</span></span>
<span data-ttu-id="e93dc-110">Il cmdlet **Restart-AzVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e93dc-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e93dc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e93dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e93dc-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e93dc-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e93dc-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e93dc-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e93dc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e93dc-114">PARAMETERS</span></span>

### <span data-ttu-id="e93dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e93dc-115">-AsJob</span></span>
<span data-ttu-id="e93dc-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e93dc-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e93dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93dc-117">-DefaultProfile</span></span>
<span data-ttu-id="e93dc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e93dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93dc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e93dc-119">-Id</span></span>
<span data-ttu-id="e93dc-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e93dc-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e93dc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e93dc-121">-Name</span></span>
<span data-ttu-id="e93dc-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e93dc-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93dc-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e93dc-123">-PerformMaintenance</span></span>
<span data-ttu-id="e93dc-124">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e93dc-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="e93dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="e93dc-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e93dc-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e93dc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e93dc-127">-Confirm</span></span>
<span data-ttu-id="e93dc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93dc-129">-WhatIf</span></span>
<span data-ttu-id="e93dc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e93dc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e93dc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e93dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93dc-132">CommonParameters</span></span>
<span data-ttu-id="e93dc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e93dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93dc-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93dc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e93dc-135">INPUTS</span></span>

### <span data-ttu-id="e93dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e93dc-136">System.String</span></span>

### <span data-ttu-id="e93dc-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e93dc-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e93dc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e93dc-138">OUTPUTS</span></span>

### <span data-ttu-id="e93dc-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e93dc-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e93dc-140">Note</span><span class="sxs-lookup"><span data-stu-id="e93dc-140">NOTES</span></span>

## <span data-ttu-id="e93dc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e93dc-141">RELATED LINKS</span></span>

[<span data-ttu-id="e93dc-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e93dc-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e93dc-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e93dc-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e93dc-146">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e93dc-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e93dc-147">Update-AzVM</span></span>](./Update-AzVM.md)


