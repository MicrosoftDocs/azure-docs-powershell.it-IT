---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: f71e827769015b7abe4d503064d97ec1d3c1228b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520253"
---
# <span data-ttu-id="021e0-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="021e0-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="021e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="021e0-102">SYNOPSIS</span></span>
<span data-ttu-id="021e0-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="021e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="021e0-104">SYNTAX</span></span>

### <span data-ttu-id="021e0-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="021e0-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021e0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="021e0-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021e0-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="021e0-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021e0-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="021e0-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="021e0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021e0-109">DESCRIPTION</span></span>
<span data-ttu-id="021e0-110">Il cmdlet **set-AzureRmVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="021e0-110">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="021e0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="021e0-111">EXAMPLES</span></span>

## <span data-ttu-id="021e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="021e0-112">PARAMETERS</span></span>

### <span data-ttu-id="021e0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="021e0-113">-AsJob</span></span>
<span data-ttu-id="021e0-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="021e0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="021e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021e0-115">-DefaultProfile</span></span>
<span data-ttu-id="021e0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="021e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="021e0-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="021e0-117">-InstanceId</span></span>
<span data-ttu-id="021e0-118">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="021e0-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021e0-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="021e0-119">-PerformMaintenance</span></span>
<span data-ttu-id="021e0-120">Indica che questo cmdlet esegue la manutenzione in una macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="021e0-121">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="021e0-121">-Redeploy</span></span>
<span data-ttu-id="021e0-122">Indica che questo cmdlet ridistribuisce una macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="021e0-123">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="021e0-123">-Reimage</span></span>
<span data-ttu-id="021e0-124">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="021e0-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="021e0-125">-ReimageAll</span></span>
<span data-ttu-id="021e0-126">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="021e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="021e0-128">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="021e0-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="021e0-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="021e0-129">-VMScaleSetName</span></span>
<span data-ttu-id="021e0-130">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021e0-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="021e0-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="021e0-131">-Confirm</span></span>
<span data-ttu-id="021e0-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021e0-133">-WhatIf</span></span>
<span data-ttu-id="021e0-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021e0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="021e0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="021e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021e0-136">CommonParameters</span></span>
<span data-ttu-id="021e0-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021e0-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021e0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021e0-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="021e0-139">INPUTS</span></span>

### <span data-ttu-id="021e0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="021e0-140">System.String</span></span>

## <span data-ttu-id="021e0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="021e0-141">OUTPUTS</span></span>

### <span data-ttu-id="021e0-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="021e0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="021e0-143">Note</span><span class="sxs-lookup"><span data-stu-id="021e0-143">NOTES</span></span>

## <span data-ttu-id="021e0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="021e0-144">RELATED LINKS</span></span>

[<span data-ttu-id="021e0-145">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="021e0-145">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
