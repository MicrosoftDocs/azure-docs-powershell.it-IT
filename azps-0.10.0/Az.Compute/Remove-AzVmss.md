---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: c8de667ae818749e980d3e917838717ec3c85b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863510"
---
# <span data-ttu-id="632f9-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-101">Remove-AzVmss</span></span>

## <span data-ttu-id="632f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="632f9-102">SYNOPSIS</span></span>
<span data-ttu-id="632f9-103">Rimuove VMSS o una macchina virtuale che si trova all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="632f9-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="632f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="632f9-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="632f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="632f9-105">DESCRIPTION</span></span>
<span data-ttu-id="632f9-106">Il cmdlet **Remove-AzVmss** rimuove il set di scale della macchina virtuale (VMSS) da Azure.</span><span class="sxs-lookup"><span data-stu-id="632f9-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="632f9-107">Questo cmdlet può essere usato anche per rimuovere una macchina virtuale specifica all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="632f9-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="632f9-108">Puoi usare il parametro *InstanceID* per rimuovere una macchina virtuale specifica all'interno di vmss.</span><span class="sxs-lookup"><span data-stu-id="632f9-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="632f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="632f9-109">EXAMPLES</span></span>

### <span data-ttu-id="632f9-110">Esempio 1: rimuovere un VMSS</span><span class="sxs-lookup"><span data-stu-id="632f9-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="632f9-111">Questo comando rimuove il VMSS denominato VMScaleSet001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="632f9-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="632f9-112">Esempio 2: rimuovere una macchina virtuale dall'interno di un VMSS</span><span class="sxs-lookup"><span data-stu-id="632f9-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="632f9-113">Questo comando rimuove la macchina virtuale con l'ID di istanza 3 dalla VMSS denominata VMScaleSet002 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="632f9-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="632f9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="632f9-114">PARAMETERS</span></span>

### <span data-ttu-id="632f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="632f9-115">-AsJob</span></span>
<span data-ttu-id="632f9-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="632f9-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="632f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632f9-117">-DefaultProfile</span></span>
<span data-ttu-id="632f9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="632f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="632f9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="632f9-119">-Force</span></span>
<span data-ttu-id="632f9-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="632f9-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="632f9-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="632f9-121">-InstanceId</span></span>
<span data-ttu-id="632f9-122">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="632f9-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="632f9-123">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="632f9-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="632f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="632f9-125">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="632f9-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="632f9-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="632f9-126">-VMScaleSetName</span></span>
<span data-ttu-id="632f9-127">Specie il nome del VMSS rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="632f9-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="632f9-128">Se specifichi il parametro *InstanceID* , il cmdlet rimuoverà la macchina virtuale specificata dalla vmss denominata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="632f9-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="632f9-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="632f9-129">-Confirm</span></span>
<span data-ttu-id="632f9-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="632f9-130">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632f9-131">-WhatIf</span></span>
<span data-ttu-id="632f9-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="632f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="632f9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="632f9-133">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632f9-134">CommonParameters</span></span>
<span data-ttu-id="632f9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632f9-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632f9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="632f9-137">INPUTS</span></span>

### <span data-ttu-id="632f9-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="632f9-138">None</span></span>
<span data-ttu-id="632f9-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="632f9-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="632f9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="632f9-140">OUTPUTS</span></span>

### <span data-ttu-id="632f9-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="632f9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="632f9-142">Note</span><span class="sxs-lookup"><span data-stu-id="632f9-142">NOTES</span></span>

## <span data-ttu-id="632f9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="632f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="632f9-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="632f9-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="632f9-146">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="632f9-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="632f9-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="632f9-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="632f9-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="632f9-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


