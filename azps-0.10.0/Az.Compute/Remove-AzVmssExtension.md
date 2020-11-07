---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863481"
---
# <span data-ttu-id="a982e-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a982e-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="a982e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a982e-102">SYNOPSIS</span></span>
<span data-ttu-id="a982e-103">Rimuove un'estensione da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a982e-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="a982e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a982e-104">SYNTAX</span></span>

### <span data-ttu-id="a982e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a982e-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a982e-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a982e-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a982e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a982e-107">DESCRIPTION</span></span>
<span data-ttu-id="a982e-108">Il cmdlet **Remove-AzVmssExtension** consente di rimuovere un'estensione dal set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a982e-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a982e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a982e-109">EXAMPLES</span></span>

### <span data-ttu-id="a982e-110">Esempio 1: rimuovere l'estensione da VMSS</span><span class="sxs-lookup"><span data-stu-id="a982e-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="a982e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a982e-111">PARAMETERS</span></span>

### <span data-ttu-id="a982e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a982e-112">-DefaultProfile</span></span>
<span data-ttu-id="a982e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a982e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a982e-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a982e-114">-Id</span></span>
<span data-ttu-id="a982e-115">Specifica l'ID dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a982e-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a982e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a982e-116">-Name</span></span>
<span data-ttu-id="a982e-117">Specifica il nome dell'estensione rimossa da questo cmdlet da VMSS.</span><span class="sxs-lookup"><span data-stu-id="a982e-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a982e-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a982e-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a982e-119">Specifica il VMSS da cui rimuovere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a982e-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a982e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a982e-120">-Confirm</span></span>
<span data-ttu-id="a982e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a982e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a982e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a982e-122">-WhatIf</span></span>
<span data-ttu-id="a982e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a982e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a982e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a982e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a982e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a982e-125">CommonParameters</span></span>
<span data-ttu-id="a982e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a982e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a982e-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a982e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a982e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a982e-128">INPUTS</span></span>

### <span data-ttu-id="a982e-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a982e-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a982e-130">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a982e-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a982e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a982e-131">OUTPUTS</span></span>

### <span data-ttu-id="a982e-132">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a982e-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a982e-133">Note</span><span class="sxs-lookup"><span data-stu-id="a982e-133">NOTES</span></span>

## <span data-ttu-id="a982e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a982e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a982e-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a982e-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
