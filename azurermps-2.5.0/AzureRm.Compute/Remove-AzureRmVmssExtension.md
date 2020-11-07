---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865849"
---
# <span data-ttu-id="4c5a0-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4c5a0-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="4c5a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c5a0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5a0-103">Rimuove un'estensione da VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c5a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c5a0-104">SYNTAX</span></span>

### <span data-ttu-id="4c5a0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5a0-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5a0-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5a0-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c5a0-107">DESCRIPTION</span></span>
<span data-ttu-id="4c5a0-108">Il cmdlet **Remove-AzureRmVmssExtension** consente di rimuovere un'estensione dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4c5a0-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4c5a0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c5a0-109">EXAMPLES</span></span>

## <span data-ttu-id="4c5a0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c5a0-110">PARAMETERS</span></span>

### <span data-ttu-id="4c5a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5a0-111">-DefaultProfile</span></span>
<span data-ttu-id="4c5a0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c5a0-113">-ID</span><span class="sxs-lookup"><span data-stu-id="4c5a0-113">-Id</span></span>
<span data-ttu-id="4c5a0-114">Specifica l'ID dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c5a0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c5a0-115">-Name</span></span>
<span data-ttu-id="4c5a0-116">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c5a0-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c5a0-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4c5a0-118">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="4c5a0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c5a0-119">-Confirm</span></span>
<span data-ttu-id="4c5a0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c5a0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5a0-121">-WhatIf</span></span>
<span data-ttu-id="4c5a0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c5a0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c5a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5a0-124">CommonParameters</span></span>
<span data-ttu-id="4c5a0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5a0-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c5a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5a0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c5a0-127">INPUTS</span></span>

### <span data-ttu-id="4c5a0-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c5a0-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="4c5a0-129">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4c5a0-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="4c5a0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c5a0-130">OUTPUTS</span></span>

### <span data-ttu-id="4c5a0-131">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4c5a0-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4c5a0-132">Note</span><span class="sxs-lookup"><span data-stu-id="4c5a0-132">NOTES</span></span>

## <span data-ttu-id="4c5a0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c5a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c5a0-134">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4c5a0-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
