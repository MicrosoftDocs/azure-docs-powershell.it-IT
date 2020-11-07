---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867132"
---
# <span data-ttu-id="4ad5e-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="4ad5e-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="4ad5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ad5e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad5e-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ad5e-104">SYNTAX</span></span>

### <span data-ttu-id="4ad5e-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ad5e-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ad5e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="4ad5e-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad5e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad5e-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad5e-108">Il cmdlet **set-AzureRmVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="4ad5e-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="4ad5e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ad5e-109">EXAMPLES</span></span>

## <span data-ttu-id="4ad5e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ad5e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad5e-111">-AsJob</span></span>
<span data-ttu-id="4ad5e-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4ad5e-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad5e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad5e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad5e-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4ad5e-115">-InstanceId</span></span>
<span data-ttu-id="4ad5e-116">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5e-117">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="4ad5e-117">-Reimage</span></span>
<span data-ttu-id="4ad5e-118">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5e-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="4ad5e-119">-ReimageAll</span></span>
<span data-ttu-id="4ad5e-120">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad5e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ad5e-122">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="4ad5e-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ad5e-123">-VMScaleSetName</span></span>
<span data-ttu-id="4ad5e-124">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5e-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ad5e-125">-Confirm</span></span>
<span data-ttu-id="4ad5e-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad5e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad5e-127">-WhatIf</span></span>
<span data-ttu-id="4ad5e-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ad5e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad5e-130">CommonParameters</span></span>
<span data-ttu-id="4ad5e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad5e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad5e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad5e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ad5e-133">INPUTS</span></span>

### <span data-ttu-id="4ad5e-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4ad5e-134">None</span></span>
<span data-ttu-id="4ad5e-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ad5e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ad5e-136">OUTPUTS</span></span>

### <span data-ttu-id="4ad5e-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4ad5e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4ad5e-138">Note</span><span class="sxs-lookup"><span data-stu-id="4ad5e-138">NOTES</span></span>

## <span data-ttu-id="4ad5e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ad5e-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ad5e-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="4ad5e-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
