---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514544"
---
# <span data-ttu-id="65f71-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65f71-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="65f71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65f71-102">SYNOPSIS</span></span>
<span data-ttu-id="65f71-103">Rimuove un'estensione di diagnostica da VMSS.</span><span class="sxs-lookup"><span data-stu-id="65f71-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65f71-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65f71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65f71-105">DESCRIPTION</span></span>
<span data-ttu-id="65f71-106">Il cmdlet **Remove-AzureRmVmssDiagnosticsExtension** rimuove un'estensione di diagnostica dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="65f71-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="65f71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65f71-107">EXAMPLES</span></span>

### <span data-ttu-id="65f71-108">Esempio 1: rimuovere un'estensione di diagnostica da VMSS</span><span class="sxs-lookup"><span data-stu-id="65f71-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="65f71-109">Questo comando rimuove l'estensione di diagnostica dalla VMSS.</span><span class="sxs-lookup"><span data-stu-id="65f71-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="65f71-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65f71-110">PARAMETERS</span></span>

### <span data-ttu-id="65f71-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="65f71-111">-Name</span></span>
<span data-ttu-id="65f71-112">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="65f71-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f71-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65f71-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="65f71-114">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="65f71-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="65f71-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65f71-115">-Confirm</span></span>
<span data-ttu-id="65f71-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65f71-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f71-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f71-117">-WhatIf</span></span>
<span data-ttu-id="65f71-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65f71-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="65f71-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65f71-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f71-120">CommonParameters</span></span>
<span data-ttu-id="65f71-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f71-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65f71-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f71-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65f71-123">INPUTS</span></span>

### <span data-ttu-id="65f71-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="65f71-124">None</span></span>
<span data-ttu-id="65f71-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="65f71-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65f71-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65f71-126">OUTPUTS</span></span>

###  
<span data-ttu-id="65f71-127">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="65f71-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="65f71-128">Note</span><span class="sxs-lookup"><span data-stu-id="65f71-128">NOTES</span></span>

## <span data-ttu-id="65f71-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65f71-129">RELATED LINKS</span></span>

[<span data-ttu-id="65f71-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65f71-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="65f71-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65f71-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="65f71-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="65f71-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


