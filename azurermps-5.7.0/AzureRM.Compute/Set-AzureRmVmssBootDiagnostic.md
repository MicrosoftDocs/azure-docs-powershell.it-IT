---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516851"
---
# <span data-ttu-id="130e4-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="130e4-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="130e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="130e4-102">SYNOPSIS</span></span>
<span data-ttu-id="130e4-103">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="130e4-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="130e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="130e4-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="130e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="130e4-105">DESCRIPTION</span></span>
<span data-ttu-id="130e4-106">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="130e4-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="130e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="130e4-107">EXAMPLES</span></span>

### <span data-ttu-id="130e4-108">Esempio 1: impostare la proprietà del profilo di diagnostica di avvio per un VMSS</span><span class="sxs-lookup"><span data-stu-id="130e4-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="130e4-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="130e4-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="130e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="130e4-110">PARAMETERS</span></span>

### <span data-ttu-id="130e4-111">-Enabled</span><span class="sxs-lookup"><span data-stu-id="130e4-111">-Enabled</span></span>
<span data-ttu-id="130e4-112">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="130e4-112">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="130e4-113">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="130e4-113">-StorageUri</span></span>
<span data-ttu-id="130e4-114">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="130e4-114">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="130e4-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="130e4-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="130e4-116">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="130e4-116">Specifies the VMSS object.</span></span>
<span data-ttu-id="130e4-117">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="130e4-117">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="130e4-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="130e4-118">-Confirm</span></span>
<span data-ttu-id="130e4-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="130e4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="130e4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="130e4-120">-WhatIf</span></span>
<span data-ttu-id="130e4-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="130e4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="130e4-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="130e4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="130e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130e4-123">CommonParameters</span></span>
<span data-ttu-id="130e4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="130e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130e4-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="130e4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130e4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="130e4-126">INPUTS</span></span>

### <span data-ttu-id="130e4-127">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="130e4-127">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="130e4-128">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="130e4-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="130e4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="130e4-129">OUTPUTS</span></span>

### <span data-ttu-id="130e4-130">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="130e4-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="130e4-131">Note</span><span class="sxs-lookup"><span data-stu-id="130e4-131">NOTES</span></span>

## <span data-ttu-id="130e4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="130e4-132">RELATED LINKS</span></span>

