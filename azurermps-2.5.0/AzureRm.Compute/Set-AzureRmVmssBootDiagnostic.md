---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
ms.openlocfilehash: cca99d994380483465f9026ba8023cd92afc7e37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865846"
---
# <span data-ttu-id="9455e-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9455e-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="9455e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9455e-102">SYNOPSIS</span></span>
<span data-ttu-id="9455e-103">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9455e-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9455e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9455e-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9455e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9455e-105">DESCRIPTION</span></span>
<span data-ttu-id="9455e-106">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9455e-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="9455e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9455e-107">EXAMPLES</span></span>

### <span data-ttu-id="9455e-108">Esempio 1: impostare la proprietà del profilo di diagnostica di avvio per un VMSS</span><span class="sxs-lookup"><span data-stu-id="9455e-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="9455e-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="9455e-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="9455e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9455e-110">PARAMETERS</span></span>

### <span data-ttu-id="9455e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9455e-111">-DefaultProfile</span></span>
<span data-ttu-id="9455e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9455e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9455e-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9455e-113">-Enabled</span></span>
<span data-ttu-id="9455e-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9455e-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9455e-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="9455e-115">-StorageUri</span></span>
<span data-ttu-id="9455e-116">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="9455e-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="9455e-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9455e-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9455e-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9455e-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="9455e-119">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9455e-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9455e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9455e-120">-Confirm</span></span>
<span data-ttu-id="9455e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9455e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9455e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9455e-122">-WhatIf</span></span>
<span data-ttu-id="9455e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9455e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9455e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9455e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9455e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9455e-125">CommonParameters</span></span>
<span data-ttu-id="9455e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9455e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9455e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9455e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9455e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9455e-128">INPUTS</span></span>

### <span data-ttu-id="9455e-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9455e-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="9455e-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="9455e-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="9455e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9455e-131">OUTPUTS</span></span>

### <span data-ttu-id="9455e-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9455e-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="9455e-133">Note</span><span class="sxs-lookup"><span data-stu-id="9455e-133">NOTES</span></span>

## <span data-ttu-id="9455e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9455e-134">RELATED LINKS</span></span>

