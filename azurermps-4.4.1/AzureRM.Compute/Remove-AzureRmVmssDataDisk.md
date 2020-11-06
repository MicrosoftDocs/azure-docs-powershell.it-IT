---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508675"
---
# <span data-ttu-id="0c327-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0c327-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="0c327-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c327-102">SYNOPSIS</span></span>
<span data-ttu-id="0c327-103">Rimuove un disco di dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c327-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c327-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c327-104">SYNTAX</span></span>

### <span data-ttu-id="0c327-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c327-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c327-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c327-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c327-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c327-107">DESCRIPTION</span></span>
<span data-ttu-id="0c327-108">Il cmdlet **Remove-AzureRmVmssDataDisk** rimuove un disco di dati dall'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="0c327-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0c327-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c327-109">EXAMPLES</span></span>

### <span data-ttu-id="0c327-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c327-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="0c327-111">Questo comando rimuove il disco di dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c327-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="0c327-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0c327-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="0c327-113">Questo comando rimuove il disco di dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c327-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="0c327-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c327-114">PARAMETERS</span></span>

### <span data-ttu-id="0c327-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c327-115">-DefaultProfile</span></span>
<span data-ttu-id="0c327-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c327-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c327-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="0c327-117">-Lun</span></span>
<span data-ttu-id="0c327-118">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="0c327-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c327-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c327-119">-Name</span></span>
<span data-ttu-id="0c327-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="0c327-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c327-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c327-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0c327-122">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0c327-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="0c327-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c327-123">-Confirm</span></span>
<span data-ttu-id="0c327-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c327-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c327-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c327-125">-WhatIf</span></span>
<span data-ttu-id="0c327-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c327-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c327-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c327-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c327-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c327-128">CommonParameters</span></span>
<span data-ttu-id="0c327-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c327-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c327-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c327-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c327-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c327-131">INPUTS</span></span>

### <span data-ttu-id="0c327-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c327-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="0c327-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0c327-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0c327-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c327-134">OUTPUTS</span></span>

### <span data-ttu-id="0c327-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c327-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="0c327-136">Note</span><span class="sxs-lookup"><span data-stu-id="0c327-136">NOTES</span></span>

## <span data-ttu-id="0c327-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c327-137">RELATED LINKS</span></span>

