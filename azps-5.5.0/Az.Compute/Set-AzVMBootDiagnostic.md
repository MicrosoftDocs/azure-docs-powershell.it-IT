---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199175"
---
# <span data-ttu-id="6cb13-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6cb13-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="6cb13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb13-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb13-103">Modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6cb13-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="6cb13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cb13-104">SYNTAX</span></span>

### <span data-ttu-id="6cb13-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6cb13-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cb13-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6cb13-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cb13-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6cb13-107">DESCRIPTION</span></span>
<span data-ttu-id="6cb13-108">Il cmdlet **Set-AzVMBootDiagnostic** modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6cb13-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="6cb13-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cb13-109">EXAMPLES</span></span>

### <span data-ttu-id="6cb13-110">Esempio 1: Abilitare la diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="6cb13-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="6cb13-111">Il primo comando recupera la macchina virtuale denominata ContosoVM07 **tramite Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="6cb13-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="6cb13-112">Il comando lo archivia nella $VM variabile.</span><span class="sxs-lookup"><span data-stu-id="6cb13-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="6cb13-113">Il secondo comando abilita la diagnostica di avvio per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="6cb13-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="6cb13-114">I dati di diagnostica vengono archiviati nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="6cb13-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="6cb13-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cb13-115">PARAMETERS</span></span>

### <span data-ttu-id="6cb13-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb13-116">-DefaultProfile</span></span>
<span data-ttu-id="6cb13-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cb13-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cb13-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="6cb13-118">-Disable</span></span>
<span data-ttu-id="6cb13-119">Indica che questo cmdlet disabilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6cb13-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb13-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="6cb13-120">-Enable</span></span>
<span data-ttu-id="6cb13-121">Indica che questo cmdlet abilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6cb13-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb13-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb13-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cb13-123">Specifica il nome del gruppo di risorse dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6cb13-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb13-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6cb13-124">-StorageAccountName</span></span>
<span data-ttu-id="6cb13-125">Specifica il nome dell'account di archiviazione in cui salvare i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="6cb13-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb13-126">-VM</span><span class="sxs-lookup"><span data-stu-id="6cb13-126">-VM</span></span>
<span data-ttu-id="6cb13-127">Specifica la macchina virtuale per cui questo cmdlet modifica la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="6cb13-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="6cb13-128">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6cb13-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb13-129">CommonParameters</span></span>
<span data-ttu-id="6cb13-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb13-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6cb13-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb13-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6cb13-132">INPUTS</span></span>

### <span data-ttu-id="6cb13-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6cb13-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6cb13-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb13-134">System.String</span></span>

## <span data-ttu-id="6cb13-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cb13-135">OUTPUTS</span></span>

### <span data-ttu-id="6cb13-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6cb13-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6cb13-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="6cb13-137">NOTES</span></span>

## <span data-ttu-id="6cb13-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cb13-138">RELATED LINKS</span></span>

[<span data-ttu-id="6cb13-139">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="6cb13-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6cb13-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6cb13-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


