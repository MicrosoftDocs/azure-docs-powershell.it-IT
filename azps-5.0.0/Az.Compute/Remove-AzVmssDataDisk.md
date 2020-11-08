---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202216"
---
# <span data-ttu-id="f264e-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f264e-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="f264e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f264e-102">SYNOPSIS</span></span>
<span data-ttu-id="f264e-103">Rimuove un disco di dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="f264e-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="f264e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f264e-104">SYNTAX</span></span>

### <span data-ttu-id="f264e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f264e-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f264e-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="f264e-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f264e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f264e-107">DESCRIPTION</span></span>
<span data-ttu-id="f264e-108">Il cmdlet **Remove-AzVmssDataDisk** rimuove un disco di dati dall'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="f264e-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f264e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f264e-109">EXAMPLES</span></span>

### <span data-ttu-id="f264e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f264e-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="f264e-111">Questo comando rimuove il disco di dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f264e-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="f264e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f264e-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="f264e-113">Questo comando rimuove il disco di dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f264e-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="f264e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f264e-114">PARAMETERS</span></span>

### <span data-ttu-id="f264e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f264e-115">-DefaultProfile</span></span>
<span data-ttu-id="f264e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f264e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f264e-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="f264e-117">-Lun</span></span>
<span data-ttu-id="f264e-118">Specifica il numero di unità logica del disco.</span><span class="sxs-lookup"><span data-stu-id="f264e-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="f264e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f264e-119">-Name</span></span>
<span data-ttu-id="f264e-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="f264e-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="f264e-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f264e-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f264e-122">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f264e-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="f264e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f264e-123">-Confirm</span></span>
<span data-ttu-id="f264e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f264e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f264e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f264e-125">-WhatIf</span></span>
<span data-ttu-id="f264e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f264e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f264e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f264e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f264e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f264e-128">CommonParameters</span></span>
<span data-ttu-id="f264e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f264e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f264e-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f264e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f264e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f264e-131">INPUTS</span></span>

### <span data-ttu-id="f264e-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f264e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f264e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f264e-133">System.String</span></span>

### <span data-ttu-id="f264e-134">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f264e-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f264e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f264e-135">OUTPUTS</span></span>

### <span data-ttu-id="f264e-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f264e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f264e-137">Note</span><span class="sxs-lookup"><span data-stu-id="f264e-137">NOTES</span></span>

## <span data-ttu-id="f264e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f264e-138">RELATED LINKS</span></span>
