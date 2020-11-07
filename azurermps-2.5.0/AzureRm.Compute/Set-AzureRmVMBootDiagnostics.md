---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866706"
---
# <span data-ttu-id="8b946-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8b946-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="8b946-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b946-102">SYNOPSIS</span></span>
<span data-ttu-id="8b946-103">Modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b946-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b946-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b946-104">SYNTAX</span></span>

### <span data-ttu-id="8b946-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8b946-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b946-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8b946-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b946-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b946-107">DESCRIPTION</span></span>
<span data-ttu-id="8b946-108">Il cmdlet **set-AzureRmVMBootDiagnostics** modifica le proprietà di diagnostica di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b946-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="8b946-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b946-109">EXAMPLES</span></span>

### <span data-ttu-id="8b946-110">Esempio 1: abilitare la diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="8b946-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="8b946-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="8b946-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="8b946-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="8b946-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="8b946-113">Il secondo comando consente la diagnostica di avvio per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="8b946-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="8b946-114">I dati di diagnostica vengono archiviati nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="8b946-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="8b946-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b946-115">PARAMETERS</span></span>

### <span data-ttu-id="8b946-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b946-116">-DefaultProfile</span></span>
<span data-ttu-id="8b946-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b946-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b946-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="8b946-118">-Disable</span></span>
<span data-ttu-id="8b946-119">Indica che questo cmdlet disabilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b946-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="8b946-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="8b946-120">-Enable</span></span>
<span data-ttu-id="8b946-121">Indica che questo cmdlet Abilita la diagnostica di avvio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b946-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="8b946-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b946-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b946-123">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b946-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b946-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b946-124">-StorageAccountName</span></span>
<span data-ttu-id="8b946-125">Specifica il nome dell'account di archiviazione in cui salvare i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="8b946-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="8b946-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8b946-126">-VM</span></span>
<span data-ttu-id="8b946-127">Specifica la macchina virtuale per cui questo cmdlet modifica la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="8b946-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="8b946-128">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="8b946-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="8b946-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b946-129">CommonParameters</span></span>
<span data-ttu-id="8b946-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b946-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b946-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b946-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b946-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b946-132">INPUTS</span></span>

### <span data-ttu-id="8b946-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8b946-133">PSVirtualMachine</span></span>
<span data-ttu-id="8b946-134">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8b946-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8b946-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b946-135">OUTPUTS</span></span>

### <span data-ttu-id="8b946-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8b946-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8b946-137">Note</span><span class="sxs-lookup"><span data-stu-id="8b946-137">NOTES</span></span>

## <span data-ttu-id="8b946-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b946-138">RELATED LINKS</span></span>

[<span data-ttu-id="8b946-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8b946-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8b946-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8b946-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


