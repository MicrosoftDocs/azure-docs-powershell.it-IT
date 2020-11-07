---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86fb5997c93aecbaa5aabd07255ae6bde840e91f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866909"
---
# <span data-ttu-id="e0933-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="e0933-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0933-102">SYNOPSIS</span></span>
<span data-ttu-id="e0933-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0933-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0933-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0933-104">SYNTAX</span></span>

### <span data-ttu-id="e0933-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0933-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0933-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e0933-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0933-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e0933-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0933-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e0933-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0933-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0933-109">DESCRIPTION</span></span>
<span data-ttu-id="e0933-110">Il cmdlet **Restart-AzureRmVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0933-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e0933-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0933-111">EXAMPLES</span></span>

### <span data-ttu-id="e0933-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e0933-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e0933-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e0933-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e0933-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0933-114">PARAMETERS</span></span>

### <span data-ttu-id="e0933-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0933-115">-AsJob</span></span>
<span data-ttu-id="e0933-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e0933-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0933-117">-DefaultProfile</span></span>
<span data-ttu-id="e0933-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0933-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e0933-119">-Id</span></span>
<span data-ttu-id="e0933-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0933-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0933-121">-Name</span></span>
<span data-ttu-id="e0933-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0933-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e0933-123">-PerformMaintenance</span></span>
<span data-ttu-id="e0933-124">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0933-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0933-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0933-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0933-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0933-127">-Confirm</span></span>
<span data-ttu-id="e0933-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0933-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0933-129">-WhatIf</span></span>
<span data-ttu-id="e0933-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0933-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0933-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0933-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0933-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0933-132">CommonParameters</span></span>
<span data-ttu-id="e0933-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0933-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0933-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0933-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0933-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0933-135">INPUTS</span></span>

### <span data-ttu-id="e0933-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e0933-136">None</span></span>
<span data-ttu-id="e0933-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e0933-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0933-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0933-138">OUTPUTS</span></span>

### <span data-ttu-id="e0933-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e0933-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e0933-140">Note</span><span class="sxs-lookup"><span data-stu-id="e0933-140">NOTES</span></span>

## <span data-ttu-id="e0933-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0933-141">RELATED LINKS</span></span>

[<span data-ttu-id="e0933-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e0933-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="e0933-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="e0933-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="e0933-146">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="e0933-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0933-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


