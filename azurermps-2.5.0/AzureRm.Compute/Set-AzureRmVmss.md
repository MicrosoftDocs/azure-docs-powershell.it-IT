---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866368"
---
# <span data-ttu-id="de186-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="de186-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de186-102">SYNOPSIS</span></span>
<span data-ttu-id="de186-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="de186-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de186-104">SYNTAX</span></span>

### <span data-ttu-id="de186-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de186-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de186-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="de186-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de186-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de186-107">DESCRIPTION</span></span>
<span data-ttu-id="de186-108">Il cmdlet **set-AzureRmVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="de186-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="de186-109">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="de186-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="de186-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de186-110">EXAMPLES</span></span>

### <span data-ttu-id="de186-111">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="de186-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="de186-112">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="de186-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="de186-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de186-113">PARAMETERS</span></span>

### <span data-ttu-id="de186-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de186-114">-AsJob</span></span>
<span data-ttu-id="de186-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="de186-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="de186-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de186-116">-DefaultProfile</span></span>
<span data-ttu-id="de186-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de186-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de186-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="de186-118">-InstanceId</span></span>
<span data-ttu-id="de186-119">ID istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de186-119">The instance ID of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de186-120">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="de186-120">-Reimage</span></span>
<span data-ttu-id="de186-121">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="de186-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="de186-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="de186-122">-ReimageAll</span></span>
<span data-ttu-id="de186-123">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="de186-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="de186-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de186-124">-ResourceGroupName</span></span>
<span data-ttu-id="de186-125">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="de186-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="de186-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="de186-126">-VMScaleSetName</span></span>
<span data-ttu-id="de186-127">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="de186-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="de186-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de186-128">-Confirm</span></span>
<span data-ttu-id="de186-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de186-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de186-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de186-130">-WhatIf</span></span>
<span data-ttu-id="de186-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de186-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de186-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de186-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de186-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de186-133">CommonParameters</span></span>
<span data-ttu-id="de186-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de186-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de186-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de186-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de186-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de186-136">INPUTS</span></span>

### <span data-ttu-id="de186-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de186-137">None</span></span>
<span data-ttu-id="de186-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="de186-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de186-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de186-139">OUTPUTS</span></span>

### <span data-ttu-id="de186-140">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="de186-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="de186-141">Note</span><span class="sxs-lookup"><span data-stu-id="de186-141">NOTES</span></span>

## <span data-ttu-id="de186-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de186-142">RELATED LINKS</span></span>

[<span data-ttu-id="de186-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="de186-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="de186-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="de186-146">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="de186-147">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="de186-148">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="de186-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de186-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


