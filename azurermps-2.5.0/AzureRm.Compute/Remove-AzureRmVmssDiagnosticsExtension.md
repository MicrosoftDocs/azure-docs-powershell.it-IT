---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866709"
---
# <span data-ttu-id="24cb1-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24cb1-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="24cb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="24cb1-103">Rimuove un'estensione di diagnostica da VMSS.</span><span class="sxs-lookup"><span data-stu-id="24cb1-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24cb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24cb1-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="24cb1-106">Il cmdlet **Remove-AzureRmVmssDiagnosticsExtension** rimuove un'estensione di diagnostica dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="24cb1-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="24cb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24cb1-107">EXAMPLES</span></span>

### <span data-ttu-id="24cb1-108">Esempio 1: rimuovere un'estensione di diagnostica da VMSS</span><span class="sxs-lookup"><span data-stu-id="24cb1-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="24cb1-109">Questo comando rimuove l'estensione di diagnostica dalla VMSS.</span><span class="sxs-lookup"><span data-stu-id="24cb1-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="24cb1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24cb1-110">PARAMETERS</span></span>

### <span data-ttu-id="24cb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cb1-111">-DefaultProfile</span></span>
<span data-ttu-id="24cb1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24cb1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cb1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="24cb1-113">-Name</span></span>
<span data-ttu-id="24cb1-114">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="24cb1-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="24cb1-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24cb1-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="24cb1-116">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="24cb1-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="24cb1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24cb1-117">-Confirm</span></span>
<span data-ttu-id="24cb1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24cb1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cb1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cb1-119">-WhatIf</span></span>
<span data-ttu-id="24cb1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24cb1-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="24cb1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24cb1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cb1-122">CommonParameters</span></span>
<span data-ttu-id="24cb1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cb1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cb1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cb1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24cb1-125">INPUTS</span></span>

### <span data-ttu-id="24cb1-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24cb1-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="24cb1-127">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="24cb1-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="24cb1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24cb1-128">OUTPUTS</span></span>

###  
<span data-ttu-id="24cb1-129">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="24cb1-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="24cb1-130">Note</span><span class="sxs-lookup"><span data-stu-id="24cb1-130">NOTES</span></span>

## <span data-ttu-id="24cb1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24cb1-131">RELATED LINKS</span></span>

[<span data-ttu-id="24cb1-132">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24cb1-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="24cb1-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24cb1-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="24cb1-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24cb1-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


