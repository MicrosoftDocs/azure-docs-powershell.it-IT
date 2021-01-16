---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334195"
---
# <span data-ttu-id="6c392-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6c392-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="6c392-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c392-102">SYNOPSIS</span></span>
<span data-ttu-id="6c392-103">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c392-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="6c392-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c392-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c392-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c392-105">DESCRIPTION</span></span>
<span data-ttu-id="6c392-106">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c392-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="6c392-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c392-107">EXAMPLES</span></span>

### <span data-ttu-id="6c392-108">Esempio 1: impostare la proprietà del profilo di diagnostica di avvio per un VMSS</span><span class="sxs-lookup"><span data-stu-id="6c392-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="6c392-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6c392-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6c392-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c392-110">PARAMETERS</span></span>

### <span data-ttu-id="6c392-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c392-111">-DefaultProfile</span></span>
<span data-ttu-id="6c392-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c392-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c392-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6c392-113">-Enabled</span></span>
<span data-ttu-id="6c392-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6c392-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="6c392-115">-StorageUri</span></span>
<span data-ttu-id="6c392-116">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="6c392-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c392-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6c392-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="6c392-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="6c392-119">Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c392-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c392-120">-Confirm</span></span>
<span data-ttu-id="6c392-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c392-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c392-122">-WhatIf</span></span>
<span data-ttu-id="6c392-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c392-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c392-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c392-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c392-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c392-125">CommonParameters</span></span>
<span data-ttu-id="6c392-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c392-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c392-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c392-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c392-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c392-128">INPUTS</span></span>

### <span data-ttu-id="6c392-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c392-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6c392-130">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6c392-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6c392-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6c392-131">System.String</span></span>

## <span data-ttu-id="6c392-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c392-132">OUTPUTS</span></span>

### <span data-ttu-id="6c392-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c392-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6c392-134">Note</span><span class="sxs-lookup"><span data-stu-id="6c392-134">NOTES</span></span>

## <span data-ttu-id="6c392-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c392-135">RELATED LINKS</span></span>
