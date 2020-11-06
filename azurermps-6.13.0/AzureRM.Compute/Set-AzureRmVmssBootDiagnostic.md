---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: e50b9b1a99c770ca8d9bb88c114a4c80f25283da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509264"
---
# <span data-ttu-id="92ea8-101">Set-AzureRmVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="92ea8-101">Set-AzureRmVmssBootDiagnostic</span></span>

## <span data-ttu-id="92ea8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="92ea8-103">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92ea8-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92ea8-104">SYNTAX</span></span>

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92ea8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="92ea8-106">Imposta il profilo di diagnostica di avvio della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92ea8-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="92ea8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92ea8-107">EXAMPLES</span></span>

### <span data-ttu-id="92ea8-108">Esempio 1: impostare la proprietà del profilo di diagnostica di avvio per un VMSS</span><span class="sxs-lookup"><span data-stu-id="92ea8-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="92ea8-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="92ea8-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="92ea8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92ea8-110">PARAMETERS</span></span>

### <span data-ttu-id="92ea8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ea8-111">-DefaultProfile</span></span>
<span data-ttu-id="92ea8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92ea8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ea8-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="92ea8-113">-Enabled</span></span>
<span data-ttu-id="92ea8-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="92ea8-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="92ea8-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="92ea8-115">-StorageUri</span></span>
<span data-ttu-id="92ea8-116">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="92ea8-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="92ea8-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="92ea8-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="92ea8-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="92ea8-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="92ea8-119">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="92ea8-119">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="92ea8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92ea8-120">-Confirm</span></span>
<span data-ttu-id="92ea8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92ea8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ea8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ea8-122">-WhatIf</span></span>
<span data-ttu-id="92ea8-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92ea8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92ea8-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92ea8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ea8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ea8-125">CommonParameters</span></span>
<span data-ttu-id="92ea8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92ea8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ea8-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ea8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ea8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92ea8-128">INPUTS</span></span>

### <span data-ttu-id="92ea8-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="92ea8-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="92ea8-130">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="92ea8-130">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="92ea8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92ea8-131">System.String</span></span>

## <span data-ttu-id="92ea8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92ea8-132">OUTPUTS</span></span>

### <span data-ttu-id="92ea8-133">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="92ea8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="92ea8-134">Note</span><span class="sxs-lookup"><span data-stu-id="92ea8-134">NOTES</span></span>

## <span data-ttu-id="92ea8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92ea8-135">RELATED LINKS</span></span>
