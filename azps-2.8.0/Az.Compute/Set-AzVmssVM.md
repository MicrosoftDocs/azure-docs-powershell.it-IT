---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675138"
---
# <span data-ttu-id="2c2e5-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2c2e5-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="2c2e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2e5-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="2c2e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c2e5-104">SYNTAX</span></span>

### <span data-ttu-id="2c2e5-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c2e5-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c2e5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2c2e5-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c2e5-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="2c2e5-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c2e5-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="2c2e5-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c2e5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c2e5-109">DESCRIPTION</span></span>
<span data-ttu-id="2c2e5-110">Il cmdlet **set-AzVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="2c2e5-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2c2e5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c2e5-111">EXAMPLES</span></span>

## <span data-ttu-id="2c2e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c2e5-112">PARAMETERS</span></span>

### <span data-ttu-id="2c2e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c2e5-113">-AsJob</span></span>
<span data-ttu-id="2c2e5-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2c2e5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c2e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2e5-115">-DefaultProfile</span></span>
<span data-ttu-id="2c2e5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2e5-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2c2e5-117">-InstanceId</span></span>
<span data-ttu-id="2c2e5-118">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2e5-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="2c2e5-119">-PerformMaintenance</span></span>
<span data-ttu-id="2c2e5-120">Indica che questo cmdlet esegue la manutenzione in una macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="2c2e5-121">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="2c2e5-121">-Redeploy</span></span>
<span data-ttu-id="2c2e5-122">Indica che questo cmdlet ridistribuisce una macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="2c2e5-123">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="2c2e5-123">-Reimage</span></span>
<span data-ttu-id="2c2e5-124">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="2c2e5-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="2c2e5-125">-ReimageAll</span></span>
<span data-ttu-id="2c2e5-126">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="2c2e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c2e5-128">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="2c2e5-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2c2e5-129">-VMScaleSetName</span></span>
<span data-ttu-id="2c2e5-130">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c2e5-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c2e5-131">-Confirm</span></span>
<span data-ttu-id="2c2e5-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c2e5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c2e5-133">-WhatIf</span></span>
<span data-ttu-id="2c2e5-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c2e5-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c2e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2e5-136">CommonParameters</span></span>
<span data-ttu-id="2c2e5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c2e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2e5-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c2e5-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2e5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c2e5-139">INPUTS</span></span>

### <span data-ttu-id="2c2e5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c2e5-140">System.String</span></span>

## <span data-ttu-id="2c2e5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c2e5-141">OUTPUTS</span></span>

### <span data-ttu-id="2c2e5-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2c2e5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2c2e5-143">Note</span><span class="sxs-lookup"><span data-stu-id="2c2e5-143">NOTES</span></span>

## <span data-ttu-id="2c2e5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c2e5-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c2e5-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2c2e5-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)