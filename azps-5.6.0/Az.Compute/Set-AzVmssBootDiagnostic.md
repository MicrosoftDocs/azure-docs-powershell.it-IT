---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 58a45d6f9e3a24ca11c298935fc0d9676617737e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986158"
---
# <span data-ttu-id="d7d96-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d7d96-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="d7d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7d96-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d96-103">Imposta il profilo di diagnostica di avvio impostato per la scala delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d7d96-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d7d96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7d96-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d96-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7d96-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d96-106">Imposta il profilo di diagnostica di avvio impostato per la scala delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d7d96-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d7d96-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7d96-107">EXAMPLES</span></span>

### <span data-ttu-id="d7d96-108">Esempio 1: Impostare la proprietà del profilo di diagnostica di avvio per un sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="d7d96-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="d7d96-109">Questo comando imposta la proprietà del profilo di diagnostica di avvio per il sistema VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d7d96-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d7d96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7d96-110">PARAMETERS</span></span>

### <span data-ttu-id="d7d96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d96-111">-DefaultProfile</span></span>
<span data-ttu-id="d7d96-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d96-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d96-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d7d96-113">-Enabled</span></span>
<span data-ttu-id="d7d96-114">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d7d96-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d7d96-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d7d96-115">-StorageUri</span></span>
<span data-ttu-id="d7d96-116">URI dell'account di archiviazione da usare per l'inserimento dell'output della console e dello screenshot.</span><span class="sxs-lookup"><span data-stu-id="d7d96-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="d7d96-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7d96-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d7d96-118">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7d96-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="d7d96-119">È possibile usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d96-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d7d96-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d96-120">-Confirm</span></span>
<span data-ttu-id="d7d96-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7d96-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d96-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d96-122">-WhatIf</span></span>
<span data-ttu-id="d7d96-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7d96-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d96-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7d96-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d96-125">CommonParameters</span></span>
<span data-ttu-id="d7d96-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d96-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7d96-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d96-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7d96-128">INPUTS</span></span>

### <span data-ttu-id="d7d96-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7d96-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d7d96-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7d96-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d7d96-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d7d96-131">System.String</span></span>

## <span data-ttu-id="d7d96-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7d96-132">OUTPUTS</span></span>

### <span data-ttu-id="d7d96-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7d96-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d7d96-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7d96-134">NOTES</span></span>

## <span data-ttu-id="d7d96-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7d96-135">RELATED LINKS</span></span>
