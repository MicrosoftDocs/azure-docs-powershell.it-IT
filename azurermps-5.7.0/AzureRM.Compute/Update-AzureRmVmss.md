---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508276"
---
# <span data-ttu-id="fb736-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="fb736-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb736-102">SYNOPSIS</span></span>
<span data-ttu-id="fb736-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb736-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb736-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb736-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb736-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb736-105">DESCRIPTION</span></span>
<span data-ttu-id="fb736-106">Il cmdlet **Update-AzureRmVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="fb736-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="fb736-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb736-107">EXAMPLES</span></span>

### <span data-ttu-id="fb736-108">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="fb736-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="fb736-109">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale denominato LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="fb736-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="fb736-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb736-110">PARAMETERS</span></span>

### <span data-ttu-id="fb736-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb736-111">-ResourceGroupName</span></span>
<span data-ttu-id="fb736-112">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb736-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb736-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb736-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fb736-114">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="fb736-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="fb736-115">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="fb736-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="fb736-116">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb736-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb736-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fb736-117">-VMScaleSetName</span></span>
<span data-ttu-id="fb736-118">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb736-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb736-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb736-119">-Confirm</span></span>
<span data-ttu-id="fb736-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb736-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb736-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb736-121">-WhatIf</span></span>
<span data-ttu-id="fb736-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb736-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fb736-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb736-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb736-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb736-124">CommonParameters</span></span>
<span data-ttu-id="fb736-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb736-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb736-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb736-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb736-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb736-127">INPUTS</span></span>

### <span data-ttu-id="fb736-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fb736-128">None</span></span>
<span data-ttu-id="fb736-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fb736-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb736-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb736-130">OUTPUTS</span></span>

## <span data-ttu-id="fb736-131">Note</span><span class="sxs-lookup"><span data-stu-id="fb736-131">NOTES</span></span>

## <span data-ttu-id="fb736-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb736-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb736-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fb736-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fb736-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fb736-136">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fb736-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fb736-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fb736-139">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fb736-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


