---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355324"
---
# <span data-ttu-id="97751-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="97751-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="97751-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97751-102">SYNOPSIS</span></span>
<span data-ttu-id="97751-103">Rimuove un disco dati da una scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="97751-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="97751-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97751-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97751-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97751-105">DESCRIPTION</span></span>
<span data-ttu-id="97751-106">Il cmdlet **Remove-AzVmssVMDataDisk** rimuove un disco dati da una VM con set di scala VM</span><span class="sxs-lookup"><span data-stu-id="97751-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="97751-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97751-107">EXAMPLES</span></span>

### <span data-ttu-id="97751-108">Esempio 1: rimuovere un disco dati da una scala VM set VM</span><span class="sxs-lookup"><span data-stu-id="97751-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="97751-109">Il primo comando getsan la vmss VM esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="97751-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="97751-110">Il secondo comando rimuove il disco di dati lun 0 dal set di scale VM memorizzato in $VmssVM il comando finale aggiorna la VM vmss con il disco di dati rimosso.</span><span class="sxs-lookup"><span data-stu-id="97751-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="97751-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97751-111">PARAMETERS</span></span>

### <span data-ttu-id="97751-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97751-112">-DefaultProfile</span></span>
<span data-ttu-id="97751-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97751-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97751-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="97751-114">-Lun</span></span>
<span data-ttu-id="97751-115">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="97751-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="97751-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="97751-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="97751-117">Il profilo della scala della macchina virtuale set VM.</span><span class="sxs-lookup"><span data-stu-id="97751-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="97751-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97751-118">CommonParameters</span></span>
<span data-ttu-id="97751-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97751-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97751-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97751-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97751-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97751-121">INPUTS</span></span>

### <span data-ttu-id="97751-122">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="97751-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="97751-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97751-123">OUTPUTS</span></span>

### <span data-ttu-id="97751-124">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="97751-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="97751-125">Note</span><span class="sxs-lookup"><span data-stu-id="97751-125">NOTES</span></span>

## <span data-ttu-id="97751-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97751-126">RELATED LINKS</span></span>
