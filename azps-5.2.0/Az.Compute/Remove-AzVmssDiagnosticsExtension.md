---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355372"
---
# <span data-ttu-id="80706-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80706-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="80706-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80706-102">SYNOPSIS</span></span>
<span data-ttu-id="80706-103">Rimuove un'estensione di diagnostica da VMSS.</span><span class="sxs-lookup"><span data-stu-id="80706-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="80706-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80706-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80706-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80706-105">DESCRIPTION</span></span>
<span data-ttu-id="80706-106">Il cmdlet **Remove-AzVmssDiagnosticsExtension** rimuove un'estensione di diagnostica dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="80706-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="80706-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80706-107">EXAMPLES</span></span>

### <span data-ttu-id="80706-108">Esempio 1: rimuovere un'estensione di diagnostica da VMSS</span><span class="sxs-lookup"><span data-stu-id="80706-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="80706-109">Questo comando rimuove l'estensione di diagnostica dalla VMSS.</span><span class="sxs-lookup"><span data-stu-id="80706-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="80706-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80706-110">PARAMETERS</span></span>

### <span data-ttu-id="80706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80706-111">-DefaultProfile</span></span>
<span data-ttu-id="80706-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80706-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80706-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="80706-113">-Name</span></span>
<span data-ttu-id="80706-114">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="80706-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80706-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="80706-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="80706-116">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="80706-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="80706-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80706-117">-Confirm</span></span>
<span data-ttu-id="80706-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80706-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80706-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80706-119">-WhatIf</span></span>
<span data-ttu-id="80706-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80706-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80706-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80706-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80706-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80706-122">CommonParameters</span></span>
<span data-ttu-id="80706-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80706-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80706-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80706-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80706-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80706-125">INPUTS</span></span>

### <span data-ttu-id="80706-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="80706-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="80706-127">System. String</span><span class="sxs-lookup"><span data-stu-id="80706-127">System.String</span></span>

## <span data-ttu-id="80706-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80706-128">OUTPUTS</span></span>

### <span data-ttu-id="80706-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="80706-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="80706-130">Note</span><span class="sxs-lookup"><span data-stu-id="80706-130">NOTES</span></span>

## <span data-ttu-id="80706-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80706-131">RELATED LINKS</span></span>

[<span data-ttu-id="80706-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80706-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="80706-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="80706-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="80706-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="80706-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


