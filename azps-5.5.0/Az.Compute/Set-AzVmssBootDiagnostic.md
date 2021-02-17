---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196951"
---
# <span data-ttu-id="aa9cd-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="aa9cd-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="aa9cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9cd-103">Imposta il profilo di diagnostica di avvio impostato per la scala delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="aa9cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa9cd-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa9cd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa9cd-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9cd-106">Imposta il profilo di diagnostica di avvio impostato per la scala delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="aa9cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa9cd-107">EXAMPLES</span></span>

### <span data-ttu-id="aa9cd-108">Esempio 1: Impostare la proprietà del profilo di diagnostica di avvio per un sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="aa9cd-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="aa9cd-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per il sistema VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="aa9cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa9cd-110">PARAMETERS</span></span>

### <span data-ttu-id="aa9cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9cd-111">-DefaultProfile</span></span>
<span data-ttu-id="aa9cd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa9cd-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="aa9cd-113">-Enabled</span></span>
<span data-ttu-id="aa9cd-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="aa9cd-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="aa9cd-115">-StorageUri</span></span>
<span data-ttu-id="aa9cd-116">URI dell'account di archiviazione da usare per l'inserimento dell'output della console e dello screenshot.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="aa9cd-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa9cd-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aa9cd-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="aa9cd-119">È possibile usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="aa9cd-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa9cd-120">-Confirm</span></span>
<span data-ttu-id="aa9cd-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa9cd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa9cd-122">-WhatIf</span></span>
<span data-ttu-id="aa9cd-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa9cd-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa9cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9cd-125">CommonParameters</span></span>
<span data-ttu-id="aa9cd-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9cd-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa9cd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9cd-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa9cd-128">INPUTS</span></span>

### <span data-ttu-id="aa9cd-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa9cd-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="aa9cd-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aa9cd-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aa9cd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aa9cd-131">System.String</span></span>

## <span data-ttu-id="aa9cd-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa9cd-132">OUTPUTS</span></span>

### <span data-ttu-id="aa9cd-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aa9cd-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="aa9cd-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa9cd-134">NOTES</span></span>

## <span data-ttu-id="aa9cd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa9cd-135">RELATED LINKS</span></span>
