---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863333"
---
# <span data-ttu-id="52804-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-101">Set-AzVmss</span></span>

## <span data-ttu-id="52804-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52804-102">SYNOPSIS</span></span>
<span data-ttu-id="52804-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="52804-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="52804-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52804-104">SYNTAX</span></span>

### <span data-ttu-id="52804-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52804-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52804-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="52804-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52804-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52804-107">DESCRIPTION</span></span>
<span data-ttu-id="52804-108">Il cmdlet **set-AzVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="52804-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="52804-109">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="52804-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="52804-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52804-110">EXAMPLES</span></span>

### <span data-ttu-id="52804-111">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="52804-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="52804-112">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="52804-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="52804-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52804-113">PARAMETERS</span></span>

### <span data-ttu-id="52804-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52804-114">-AsJob</span></span>
<span data-ttu-id="52804-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="52804-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="52804-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52804-116">-DefaultProfile</span></span>
<span data-ttu-id="52804-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52804-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52804-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="52804-118">-InstanceId</span></span>
<span data-ttu-id="52804-119">ID istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52804-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="52804-120">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="52804-120">-Reimage</span></span>
<span data-ttu-id="52804-121">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="52804-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="52804-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="52804-122">-ReimageAll</span></span>
<span data-ttu-id="52804-123">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="52804-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="52804-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52804-124">-ResourceGroupName</span></span>
<span data-ttu-id="52804-125">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="52804-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="52804-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="52804-126">-VMScaleSetName</span></span>
<span data-ttu-id="52804-127">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="52804-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="52804-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52804-128">-Confirm</span></span>
<span data-ttu-id="52804-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52804-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52804-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52804-130">-WhatIf</span></span>
<span data-ttu-id="52804-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52804-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52804-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52804-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52804-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52804-133">CommonParameters</span></span>
<span data-ttu-id="52804-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52804-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52804-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52804-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52804-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52804-136">INPUTS</span></span>

### <span data-ttu-id="52804-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="52804-137">None</span></span>
<span data-ttu-id="52804-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="52804-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52804-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52804-139">OUTPUTS</span></span>

### <span data-ttu-id="52804-140">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="52804-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="52804-141">Note</span><span class="sxs-lookup"><span data-stu-id="52804-141">NOTES</span></span>

## <span data-ttu-id="52804-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52804-142">RELATED LINKS</span></span>

[<span data-ttu-id="52804-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="52804-144">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="52804-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="52804-146">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="52804-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="52804-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="52804-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="52804-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


