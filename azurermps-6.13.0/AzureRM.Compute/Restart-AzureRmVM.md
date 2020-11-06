---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511816"
---
# <span data-ttu-id="10a65-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="10a65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10a65-102">SYNOPSIS</span></span>
<span data-ttu-id="10a65-103">Riavvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="10a65-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10a65-104">SYNTAX</span></span>

### <span data-ttu-id="10a65-105">RestartResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10a65-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a65-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10a65-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a65-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10a65-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a65-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10a65-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a65-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10a65-109">DESCRIPTION</span></span>
<span data-ttu-id="10a65-110">Il cmdlet **Restart-AzureRmVM riavvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="10a65-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="10a65-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10a65-111">EXAMPLES</span></span>

### <span data-ttu-id="10a65-112">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="10a65-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="10a65-113">Questo comando Riavvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="10a65-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="10a65-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10a65-114">PARAMETERS</span></span>

### <span data-ttu-id="10a65-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10a65-115">-AsJob</span></span>
<span data-ttu-id="10a65-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="10a65-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="10a65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a65-117">-DefaultProfile</span></span>
<span data-ttu-id="10a65-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10a65-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a65-119">-ID</span><span class="sxs-lookup"><span data-stu-id="10a65-119">-Id</span></span>
<span data-ttu-id="10a65-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10a65-120">The resource group name.</span></span>

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

### <span data-ttu-id="10a65-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="10a65-121">-Name</span></span>
<span data-ttu-id="10a65-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10a65-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="10a65-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="10a65-123">-PerformMaintenance</span></span>
<span data-ttu-id="10a65-124">Per eseguire la manutenzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10a65-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="10a65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a65-125">-ResourceGroupName</span></span>
<span data-ttu-id="10a65-126">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10a65-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="10a65-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10a65-127">-Confirm</span></span>
<span data-ttu-id="10a65-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a65-129">-WhatIf</span></span>
<span data-ttu-id="10a65-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a65-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10a65-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10a65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a65-132">CommonParameters</span></span>
<span data-ttu-id="10a65-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a65-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a65-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a65-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10a65-135">INPUTS</span></span>

### <span data-ttu-id="10a65-136">System. String</span><span class="sxs-lookup"><span data-stu-id="10a65-136">System.String</span></span>

### <span data-ttu-id="10a65-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10a65-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10a65-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10a65-138">OUTPUTS</span></span>

### <span data-ttu-id="10a65-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="10a65-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="10a65-140">Note</span><span class="sxs-lookup"><span data-stu-id="10a65-140">NOTES</span></span>

## <span data-ttu-id="10a65-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10a65-141">RELATED LINKS</span></span>

[<span data-ttu-id="10a65-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="10a65-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="10a65-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="10a65-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="10a65-146">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="10a65-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="10a65-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


