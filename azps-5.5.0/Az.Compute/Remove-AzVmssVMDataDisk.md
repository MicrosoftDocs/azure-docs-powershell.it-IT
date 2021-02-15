---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177487"
---
# <span data-ttu-id="1b880-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1b880-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="1b880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b880-102">SYNOPSIS</span></span>
<span data-ttu-id="1b880-103">Rimuove un disco dati da una macchina virtuale impostata per il set di scalabilità</span><span class="sxs-lookup"><span data-stu-id="1b880-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="1b880-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b880-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b880-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b880-105">DESCRIPTION</span></span>
<span data-ttu-id="1b880-106">Il cmdlet **Remove-AzVmssVMDataDisk** rimuove un disco dati da una MACCHINA virtuale impostata per il set di scalabilità</span><span class="sxs-lookup"><span data-stu-id="1b880-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="1b880-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b880-107">EXAMPLES</span></span>

### <span data-ttu-id="1b880-108">Esempio 1: Rimuovere un disco di dati da una macchina virtuale impostata per il set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="1b880-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="1b880-109">Il primo comando ottiene una VM Vmss esistente specificata dal nome del gruppo di risorse, dal nome della macchina virtuale e dall'ID dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1b880-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1b880-110">Il secondo comando rimuove il disco dati lun 0 dalla macchina virtuale impostata per il set di scala in $VmssVM Il comando finale aggiorna la VM Vmss con il disco dati rimosso.</span><span class="sxs-lookup"><span data-stu-id="1b880-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="1b880-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b880-111">PARAMETERS</span></span>

### <span data-ttu-id="1b880-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b880-112">-DefaultProfile</span></span>
<span data-ttu-id="1b880-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b880-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b880-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="1b880-114">-Lun</span></span>
<span data-ttu-id="1b880-115">Specifica il numero di unità logiche del disco.</span><span class="sxs-lookup"><span data-stu-id="1b880-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b880-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1b880-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1b880-117">Profilo DELLA MACCHINA virtuale per il set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b880-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b880-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b880-118">CommonParameters</span></span>
<span data-ttu-id="1b880-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b880-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b880-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b880-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b880-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b880-121">INPUTS</span></span>

### <span data-ttu-id="1b880-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1b880-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1b880-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b880-123">OUTPUTS</span></span>

### <span data-ttu-id="1b880-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1b880-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1b880-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b880-125">NOTES</span></span>

## <span data-ttu-id="1b880-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b880-126">RELATED LINKS</span></span>
