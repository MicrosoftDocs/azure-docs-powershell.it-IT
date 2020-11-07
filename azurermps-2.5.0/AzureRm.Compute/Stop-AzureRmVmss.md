---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 50fd6447448968527b942e163f520142f594b7a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866115"
---
# <span data-ttu-id="bd7a1-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="bd7a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7a1-103">Interrompe VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd7a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd7a1-104">SYNTAX</span></span>

### <span data-ttu-id="bd7a1-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd7a1-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd7a1-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="bd7a1-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd7a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd7a1-107">DESCRIPTION</span></span>
<span data-ttu-id="bd7a1-108">Il cmdlet **Stop-AzureRmVmss** arresta tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="bd7a1-109">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="bd7a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd7a1-110">EXAMPLES</span></span>

### <span data-ttu-id="bd7a1-111">Esempio 1: arrestare tutte le macchine virtuali in VMSS</span><span class="sxs-lookup"><span data-stu-id="bd7a1-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="bd7a1-112">Questo comando Arresta tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="bd7a1-113">Esempio 2: arrestare un set specifico di macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="bd7a1-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="bd7a1-114">Questo comando Arresta un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bd7a1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd7a1-115">PARAMETERS</span></span>

### <span data-ttu-id="bd7a1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd7a1-116">-AsJob</span></span>
<span data-ttu-id="bd7a1-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bd7a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7a1-118">-DefaultProfile</span></span>
<span data-ttu-id="bd7a1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bd7a1-120">-Force</span></span>
<span data-ttu-id="bd7a1-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd7a1-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bd7a1-122">-InstanceId</span></span>
<span data-ttu-id="bd7a1-123">Specifica come matrice di stringhe l'ID o gli ID delle istanze della macchina virtuale arrestate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="bd7a1-124">Ad esempio: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="bd7a1-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="bd7a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd7a1-126">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bd7a1-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="bd7a1-127">-StayProvisioned</span></span>
<span data-ttu-id="bd7a1-128">Se specificato, la macchina virtuale entrerà nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="bd7a1-129">Se non viene specificato, la macchina virtuale immetterà lo stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="bd7a1-130">L'utente viene ancora addebitato per le VM nello stato Stopped ma non per le VM in stato deallocato interrotto.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="bd7a1-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bd7a1-131">-VMScaleSetName</span></span>
<span data-ttu-id="bd7a1-132">Specifica il nome del VMSS per cui questo cmdlet arresta le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="bd7a1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd7a1-133">-Confirm</span></span>
<span data-ttu-id="bd7a1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7a1-135">-WhatIf</span></span>
<span data-ttu-id="bd7a1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd7a1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7a1-138">CommonParameters</span></span>
<span data-ttu-id="bd7a1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7a1-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7a1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd7a1-141">INPUTS</span></span>

### <span data-ttu-id="bd7a1-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd7a1-142">None</span></span>
<span data-ttu-id="bd7a1-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bd7a1-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd7a1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd7a1-144">OUTPUTS</span></span>

### <span data-ttu-id="bd7a1-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bd7a1-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bd7a1-146">Note</span><span class="sxs-lookup"><span data-stu-id="bd7a1-146">NOTES</span></span>

## <span data-ttu-id="bd7a1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd7a1-147">RELATED LINKS</span></span>

[<span data-ttu-id="bd7a1-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-149">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-151">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="bd7a1-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bd7a1-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


