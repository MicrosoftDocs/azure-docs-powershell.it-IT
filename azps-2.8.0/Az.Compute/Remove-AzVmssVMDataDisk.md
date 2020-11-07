---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: cd41b7f09bbcf972d28aa38e9c1f4eb622e59b2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675229"
---
# <span data-ttu-id="786eb-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="786eb-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="786eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="786eb-102">SYNOPSIS</span></span>
<span data-ttu-id="786eb-103">Rimuove un disco dati da una scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="786eb-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="786eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="786eb-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="786eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="786eb-105">DESCRIPTION</span></span>
<span data-ttu-id="786eb-106">Il cmdlet **Remove-AzVmssVMDataDisk** rimuove un disco dati da una VM con set di scala VM</span><span class="sxs-lookup"><span data-stu-id="786eb-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="786eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="786eb-107">EXAMPLES</span></span>

### <span data-ttu-id="786eb-108">Esempio 1: rimuovere un disco dati da una scala VM set VM</span><span class="sxs-lookup"><span data-stu-id="786eb-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="786eb-109">Il primo comando getsan la vmss VM esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="786eb-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="786eb-110">Il secondo comando rimuove il disco di dati lun 0 dal set di scale VM memorizzato in $VmssVM il comando finale aggiorna la VM vmss con il disco di dati rimosso.</span><span class="sxs-lookup"><span data-stu-id="786eb-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="786eb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="786eb-111">PARAMETERS</span></span>

### <span data-ttu-id="786eb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786eb-112">-DefaultProfile</span></span>
<span data-ttu-id="786eb-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="786eb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786eb-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="786eb-114">-Lun</span></span>
<span data-ttu-id="786eb-115">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="786eb-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="786eb-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="786eb-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="786eb-117">Il profilo della scala della macchina virtuale set VM.</span><span class="sxs-lookup"><span data-stu-id="786eb-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="786eb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786eb-118">CommonParameters</span></span>
<span data-ttu-id="786eb-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="786eb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786eb-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="786eb-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786eb-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="786eb-121">INPUTS</span></span>

### <span data-ttu-id="786eb-122">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="786eb-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="786eb-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="786eb-123">OUTPUTS</span></span>

### <span data-ttu-id="786eb-124">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="786eb-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="786eb-125">Note</span><span class="sxs-lookup"><span data-stu-id="786eb-125">NOTES</span></span>

## <span data-ttu-id="786eb-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="786eb-126">RELATED LINKS</span></span>
