---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863502"
---
# <span data-ttu-id="9ded2-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="9ded2-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="9ded2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ded2-102">SYNOPSIS</span></span>
<span data-ttu-id="9ded2-103">Rimuove un disco di dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="9ded2-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="9ded2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ded2-104">SYNTAX</span></span>

### <span data-ttu-id="9ded2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ded2-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ded2-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ded2-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ded2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ded2-107">DESCRIPTION</span></span>
<span data-ttu-id="9ded2-108">Il cmdlet **Remove-AzVmssDataDisk** rimuove un disco di dati dall'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="9ded2-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9ded2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ded2-109">EXAMPLES</span></span>

### <span data-ttu-id="9ded2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ded2-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="9ded2-111">Questo comando rimuove il disco di dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9ded2-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="9ded2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9ded2-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="9ded2-113">Questo comando rimuove il disco di dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9ded2-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="9ded2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ded2-114">PARAMETERS</span></span>

### <span data-ttu-id="9ded2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ded2-115">-DefaultProfile</span></span>
<span data-ttu-id="9ded2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ded2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ded2-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="9ded2-117">-Lun</span></span>
<span data-ttu-id="9ded2-118">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="9ded2-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ded2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ded2-119">-Name</span></span>
<span data-ttu-id="9ded2-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="9ded2-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="9ded2-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ded2-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9ded2-122">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9ded2-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="9ded2-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ded2-123">-Confirm</span></span>
<span data-ttu-id="9ded2-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ded2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ded2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ded2-125">-WhatIf</span></span>
<span data-ttu-id="9ded2-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ded2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ded2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ded2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ded2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ded2-128">CommonParameters</span></span>
<span data-ttu-id="9ded2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ded2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ded2-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ded2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ded2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ded2-131">INPUTS</span></span>

### <span data-ttu-id="9ded2-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ded2-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="9ded2-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9ded2-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9ded2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ded2-134">OUTPUTS</span></span>

### <span data-ttu-id="9ded2-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9ded2-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="9ded2-136">Note</span><span class="sxs-lookup"><span data-stu-id="9ded2-136">NOTES</span></span>

## <span data-ttu-id="9ded2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ded2-137">RELATED LINKS</span></span>

