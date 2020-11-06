---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512699"
---
# <span data-ttu-id="a134d-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a134d-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="a134d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a134d-102">SYNOPSIS</span></span>
<span data-ttu-id="a134d-103">Modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a134d-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a134d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a134d-104">SYNTAX</span></span>

### <span data-ttu-id="a134d-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a134d-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="a134d-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a134d-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="a134d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a134d-107">DESCRIPTION</span></span>
<span data-ttu-id="a134d-108">Il cmdlet **set-AzureRmVMBootDiagnostics** modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a134d-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="a134d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a134d-109">EXAMPLES</span></span>

### <span data-ttu-id="a134d-110">Esempio 1: abilitare la diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="a134d-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="a134d-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="a134d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="a134d-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="a134d-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="a134d-113">Il secondo comando consente la diagnostica di avvio per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="a134d-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="a134d-114">I dati di diagnostica vengono archiviati nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="a134d-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="a134d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a134d-115">PARAMETERS</span></span>

### <span data-ttu-id="a134d-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="a134d-116">-Disable</span></span>
<span data-ttu-id="a134d-117">Indica che questo cmdlet disabilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a134d-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a134d-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="a134d-118">-Enable</span></span>
<span data-ttu-id="a134d-119">Indica che questo cmdlet Abilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a134d-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a134d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a134d-120">-ResourceGroupName</span></span>
<span data-ttu-id="a134d-121">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a134d-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a134d-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a134d-122">-StorageAccountName</span></span>
<span data-ttu-id="a134d-123">Specifica il nome dell'account di archiviazione in cui salvare i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="a134d-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a134d-124">-VM</span><span class="sxs-lookup"><span data-stu-id="a134d-124">-VM</span></span>
<span data-ttu-id="a134d-125">Specifica la macchina virtuale per cui questo cmdlet modifica la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="a134d-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="a134d-126">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a134d-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a134d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a134d-127">CommonParameters</span></span>
<span data-ttu-id="a134d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a134d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a134d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a134d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a134d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a134d-130">INPUTS</span></span>

### <span data-ttu-id="a134d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a134d-131">None</span></span>
<span data-ttu-id="a134d-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a134d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a134d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a134d-133">OUTPUTS</span></span>

## <span data-ttu-id="a134d-134">Note</span><span class="sxs-lookup"><span data-stu-id="a134d-134">NOTES</span></span>

## <span data-ttu-id="a134d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a134d-135">RELATED LINKS</span></span>

[<span data-ttu-id="a134d-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a134d-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a134d-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a134d-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


