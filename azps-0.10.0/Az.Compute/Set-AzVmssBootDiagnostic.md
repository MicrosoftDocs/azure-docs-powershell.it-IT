---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 482398d3ba0934f17b1381edc5dac08fb22bd75a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863334"
---
# <span data-ttu-id="705b3-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="705b3-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="705b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="705b3-102">SYNOPSIS</span></span>
<span data-ttu-id="705b3-103">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="705b3-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="705b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="705b3-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="705b3-105">DESCRIPTION</span></span>
<span data-ttu-id="705b3-106">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="705b3-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="705b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="705b3-107">EXAMPLES</span></span>

### <span data-ttu-id="705b3-108">Esempio 1: impostare la proprietà del profilo di diagnostica di avvio per un VMSS</span><span class="sxs-lookup"><span data-stu-id="705b3-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="705b3-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="705b3-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="705b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="705b3-110">PARAMETERS</span></span>

### <span data-ttu-id="705b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705b3-111">-DefaultProfile</span></span>
<span data-ttu-id="705b3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="705b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="705b3-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="705b3-113">-Enabled</span></span>
<span data-ttu-id="705b3-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="705b3-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="705b3-115">-StorageUri</span></span>
<span data-ttu-id="705b3-116">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="705b3-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="705b3-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="705b3-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="705b3-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="705b3-119">Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="705b3-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="705b3-120">-Confirm</span></span>
<span data-ttu-id="705b3-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="705b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705b3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705b3-122">-WhatIf</span></span>
<span data-ttu-id="705b3-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="705b3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="705b3-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="705b3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705b3-125">CommonParameters</span></span>
<span data-ttu-id="705b3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705b3-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705b3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705b3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="705b3-128">INPUTS</span></span>

### <span data-ttu-id="705b3-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="705b3-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="705b3-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="705b3-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="705b3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="705b3-131">OUTPUTS</span></span>

### <span data-ttu-id="705b3-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="705b3-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="705b3-133">Note</span><span class="sxs-lookup"><span data-stu-id="705b3-133">NOTES</span></span>

## <span data-ttu-id="705b3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="705b3-134">RELATED LINKS</span></span>

