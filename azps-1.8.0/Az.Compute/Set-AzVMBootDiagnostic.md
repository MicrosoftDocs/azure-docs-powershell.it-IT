---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 407119856fa670bc4561e06adae32ee806437b1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836663"
---
# <span data-ttu-id="08e7a-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="08e7a-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="08e7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="08e7a-103">Modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="08e7a-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="08e7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08e7a-104">SYNTAX</span></span>

### <span data-ttu-id="08e7a-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="08e7a-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e7a-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="08e7a-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08e7a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="08e7a-108">Il cmdlet **set-AzVMBootDiagnostic** modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="08e7a-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="08e7a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="08e7a-110">Esempio 1: abilitare la diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="08e7a-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="08e7a-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="08e7a-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="08e7a-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="08e7a-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="08e7a-113">Il secondo comando consente la diagnostica di avvio per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="08e7a-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="08e7a-114">I dati di diagnostica vengono archiviati nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="08e7a-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="08e7a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08e7a-115">PARAMETERS</span></span>

### <span data-ttu-id="08e7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e7a-116">-DefaultProfile</span></span>
<span data-ttu-id="08e7a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08e7a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e7a-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="08e7a-118">-Disable</span></span>
<span data-ttu-id="08e7a-119">Indica che questo cmdlet disabilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="08e7a-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="08e7a-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="08e7a-120">-Enable</span></span>
<span data-ttu-id="08e7a-121">Indica che questo cmdlet Abilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="08e7a-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="08e7a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e7a-122">-ResourceGroupName</span></span>
<span data-ttu-id="08e7a-123">Specifica il nome del gruppo di risorse dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08e7a-123">Specifies the name of the resource group of storage account.</span></span>

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

### <span data-ttu-id="08e7a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="08e7a-124">-StorageAccountName</span></span>
<span data-ttu-id="08e7a-125">Specifica il nome dell'account di archiviazione in cui salvare i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="08e7a-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="08e7a-126">-VM</span><span class="sxs-lookup"><span data-stu-id="08e7a-126">-VM</span></span>
<span data-ttu-id="08e7a-127">Specifica la macchina virtuale per cui questo cmdlet modifica la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="08e7a-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="08e7a-128">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="08e7a-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="08e7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e7a-129">CommonParameters</span></span>
<span data-ttu-id="08e7a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e7a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e7a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e7a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08e7a-132">INPUTS</span></span>

### <span data-ttu-id="08e7a-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08e7a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="08e7a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="08e7a-134">System.String</span></span>

## <span data-ttu-id="08e7a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08e7a-135">OUTPUTS</span></span>

### <span data-ttu-id="08e7a-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="08e7a-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="08e7a-137">Note</span><span class="sxs-lookup"><span data-stu-id="08e7a-137">NOTES</span></span>

## <span data-ttu-id="08e7a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08e7a-138">RELATED LINKS</span></span>

[<span data-ttu-id="08e7a-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="08e7a-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="08e7a-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="08e7a-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


