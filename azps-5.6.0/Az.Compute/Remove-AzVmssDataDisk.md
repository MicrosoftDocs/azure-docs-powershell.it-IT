---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998870"
---
# <span data-ttu-id="2ef34-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ef34-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="2ef34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef34-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef34-103">Rimuove un disco dati da VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ef34-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="2ef34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ef34-104">SYNTAX</span></span>

### <span data-ttu-id="2ef34-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef34-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef34-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef34-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef34-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ef34-107">DESCRIPTION</span></span>
<span data-ttu-id="2ef34-108">Il cmdlet **Remove-AzVmssDataDisk** rimuove un disco dati dall'istanza di VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="2ef34-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2ef34-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ef34-109">EXAMPLES</span></span>

### <span data-ttu-id="2ef34-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ef34-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="2ef34-111">Questo comando rimuove il disco dati denominato "DataDisk1" dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ef34-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="2ef34-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2ef34-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="2ef34-113">Questo comando rimuove il disco dati di LUN 0 dall'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ef34-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="2ef34-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ef34-114">PARAMETERS</span></span>

### <span data-ttu-id="2ef34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef34-115">-DefaultProfile</span></span>
<span data-ttu-id="2ef34-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ef34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ef34-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="2ef34-117">-Lun</span></span>
<span data-ttu-id="2ef34-118">Specifica il numero di unità logiche del disco.</span><span class="sxs-lookup"><span data-stu-id="2ef34-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="2ef34-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ef34-119">-Name</span></span>
<span data-ttu-id="2ef34-120">Specifica il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="2ef34-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="2ef34-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ef34-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2ef34-122">Specificare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ef34-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="2ef34-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ef34-123">-Confirm</span></span>
<span data-ttu-id="2ef34-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ef34-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef34-125">-WhatIf</span></span>
<span data-ttu-id="2ef34-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef34-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef34-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef34-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef34-128">CommonParameters</span></span>
<span data-ttu-id="2ef34-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef34-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ef34-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef34-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ef34-131">INPUTS</span></span>

### <span data-ttu-id="2ef34-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ef34-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2ef34-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2ef34-133">System.String</span></span>

### <span data-ttu-id="2ef34-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ef34-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2ef34-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ef34-135">OUTPUTS</span></span>

### <span data-ttu-id="2ef34-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ef34-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2ef34-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ef34-137">NOTES</span></span>

## <span data-ttu-id="2ef34-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ef34-138">RELATED LINKS</span></span>
