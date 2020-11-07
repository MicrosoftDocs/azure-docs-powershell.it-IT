---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865850"
---
# <span data-ttu-id="bcd5f-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="bcd5f-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="bcd5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd5f-103">Rimuove un disco di dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcd5f-104">SYNTAX</span></span>

### <span data-ttu-id="bcd5f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcd5f-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcd5f-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcd5f-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd5f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcd5f-107">DESCRIPTION</span></span>
<span data-ttu-id="bcd5f-108">Il cmdlet **Remove-AzureRmVmssDataDisk** rimuove un disco di dati dall'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="bcd5f-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="bcd5f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcd5f-109">EXAMPLES</span></span>

### <span data-ttu-id="bcd5f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcd5f-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="bcd5f-111">Questo comando rimuove il disco di dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="bcd5f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bcd5f-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="bcd5f-113">Questo comando rimuove il disco di dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="bcd5f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcd5f-114">PARAMETERS</span></span>

### <span data-ttu-id="bcd5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd5f-115">-DefaultProfile</span></span>
<span data-ttu-id="bcd5f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd5f-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="bcd5f-117">-Lun</span></span>
<span data-ttu-id="bcd5f-118">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="bcd5f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcd5f-119">-Name</span></span>
<span data-ttu-id="bcd5f-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="bcd5f-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcd5f-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bcd5f-122">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="bcd5f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcd5f-123">-Confirm</span></span>
<span data-ttu-id="bcd5f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd5f-125">-WhatIf</span></span>
<span data-ttu-id="bcd5f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd5f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd5f-128">CommonParameters</span></span>
<span data-ttu-id="bcd5f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd5f-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd5f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcd5f-131">INPUTS</span></span>

### <span data-ttu-id="bcd5f-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcd5f-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="bcd5f-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bcd5f-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bcd5f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcd5f-134">OUTPUTS</span></span>

### <span data-ttu-id="bcd5f-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcd5f-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="bcd5f-136">Note</span><span class="sxs-lookup"><span data-stu-id="bcd5f-136">NOTES</span></span>

## <span data-ttu-id="bcd5f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcd5f-137">RELATED LINKS</span></span>

