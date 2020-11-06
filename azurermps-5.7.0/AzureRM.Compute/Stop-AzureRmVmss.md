---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521075"
---
# <span data-ttu-id="327aa-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="327aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="327aa-102">SYNOPSIS</span></span>
<span data-ttu-id="327aa-103">Interrompe VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="327aa-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="327aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="327aa-104">SYNTAX</span></span>

### <span data-ttu-id="327aa-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="327aa-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327aa-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="327aa-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="327aa-107">DESCRIPTION</span></span>
<span data-ttu-id="327aa-108">Il cmdlet **Stop-AzureRmVmss** arresta tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="327aa-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="327aa-109">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="327aa-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="327aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="327aa-110">EXAMPLES</span></span>

### <span data-ttu-id="327aa-111">Esempio 1: arrestare tutte le macchine virtuali in VMSS</span><span class="sxs-lookup"><span data-stu-id="327aa-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="327aa-112">Questo comando Arresta tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="327aa-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="327aa-113">Esempio 2: arrestare un set specifico di macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="327aa-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="327aa-114">Questo comando Arresta un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="327aa-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="327aa-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="327aa-115">PARAMETERS</span></span>

### <span data-ttu-id="327aa-116">-Force</span><span class="sxs-lookup"><span data-stu-id="327aa-116">-Force</span></span>
<span data-ttu-id="327aa-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="327aa-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327aa-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="327aa-118">-InstanceId</span></span>
<span data-ttu-id="327aa-119">Specifica come matrice di stringhe l'ID o gli ID delle istanze della macchina virtuale arrestate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="327aa-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="327aa-120">Ad esempio: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="327aa-120">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="327aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="327aa-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="327aa-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="327aa-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="327aa-123">-StayProvisioned</span></span>
<span data-ttu-id="327aa-124">Se specificato, la macchina virtuale entrerà nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="327aa-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="327aa-125">Se non viene specificato, la macchina virtuale immetterà lo stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="327aa-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="327aa-126">L'utente viene ancora addebitato per le VM nello stato Stopped ma non per le VM in stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="327aa-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327aa-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="327aa-127">-VMScaleSetName</span></span>
<span data-ttu-id="327aa-128">Specifica il nome del VMSS per cui questo cmdlet arresta le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="327aa-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="327aa-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="327aa-129">-Confirm</span></span>
<span data-ttu-id="327aa-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="327aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="327aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="327aa-131">-WhatIf</span></span>
<span data-ttu-id="327aa-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="327aa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="327aa-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="327aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="327aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327aa-134">CommonParameters</span></span>
<span data-ttu-id="327aa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327aa-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="327aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327aa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="327aa-137">INPUTS</span></span>

### <span data-ttu-id="327aa-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="327aa-138">None</span></span>
<span data-ttu-id="327aa-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="327aa-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="327aa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="327aa-140">OUTPUTS</span></span>

## <span data-ttu-id="327aa-141">Note</span><span class="sxs-lookup"><span data-stu-id="327aa-141">NOTES</span></span>

## <span data-ttu-id="327aa-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="327aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="327aa-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="327aa-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="327aa-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="327aa-146">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="327aa-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="327aa-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="327aa-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="327aa-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


