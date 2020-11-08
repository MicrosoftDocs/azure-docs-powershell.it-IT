---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200512"
---
# <span data-ttu-id="62462-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-101">Remove-AzVmss</span></span>

## <span data-ttu-id="62462-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62462-102">SYNOPSIS</span></span>
<span data-ttu-id="62462-103">Rimuove VMSS o una macchina virtuale che si trova all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="62462-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="62462-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62462-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62462-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62462-105">DESCRIPTION</span></span>
<span data-ttu-id="62462-106">Il cmdlet **Remove-AzVmss** rimuove il set di scale della macchina virtuale (VMSS) da Azure.</span><span class="sxs-lookup"><span data-stu-id="62462-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="62462-107">Questo cmdlet può essere usato anche per rimuovere una macchina virtuale specifica all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="62462-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="62462-108">Puoi usare il parametro *InstanceID* per rimuovere una macchina virtuale specifica all'interno di vmss.</span><span class="sxs-lookup"><span data-stu-id="62462-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="62462-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62462-109">EXAMPLES</span></span>

### <span data-ttu-id="62462-110">Esempio 1: rimuovere un VMSS</span><span class="sxs-lookup"><span data-stu-id="62462-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="62462-111">Questo comando rimuove il VMSS denominato VMScaleSet001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="62462-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="62462-112">Esempio 2: rimuovere una macchina virtuale dall'interno di un VMSS</span><span class="sxs-lookup"><span data-stu-id="62462-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="62462-113">Questo comando rimuove la macchina virtuale con l'ID di istanza 3 dalla VMSS denominata VMScaleSet002 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="62462-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="62462-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62462-114">PARAMETERS</span></span>

### <span data-ttu-id="62462-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62462-115">-AsJob</span></span>
<span data-ttu-id="62462-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="62462-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62462-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62462-117">-DefaultProfile</span></span>
<span data-ttu-id="62462-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62462-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62462-119">-Force</span><span class="sxs-lookup"><span data-stu-id="62462-119">-Force</span></span>
<span data-ttu-id="62462-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="62462-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62462-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="62462-121">-InstanceId</span></span>
<span data-ttu-id="62462-122">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="62462-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="62462-123">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="62462-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62462-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62462-124">-ResourceGroupName</span></span>
<span data-ttu-id="62462-125">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="62462-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62462-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="62462-126">-VMScaleSetName</span></span>
<span data-ttu-id="62462-127">Specie il nome del VMSS rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62462-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="62462-128">Se specifichi il parametro *InstanceID* , il cmdlet rimuoverà la macchina virtuale specificata dalla vmss denominata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="62462-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62462-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62462-129">-Confirm</span></span>
<span data-ttu-id="62462-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62462-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62462-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62462-131">-WhatIf</span></span>
<span data-ttu-id="62462-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62462-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62462-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62462-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62462-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62462-134">CommonParameters</span></span>
<span data-ttu-id="62462-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62462-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62462-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62462-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62462-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62462-137">INPUTS</span></span>

### <span data-ttu-id="62462-138">System. String</span><span class="sxs-lookup"><span data-stu-id="62462-138">System.String</span></span>

### <span data-ttu-id="62462-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="62462-139">System.String[]</span></span>

## <span data-ttu-id="62462-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62462-140">OUTPUTS</span></span>

### <span data-ttu-id="62462-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="62462-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="62462-142">Note</span><span class="sxs-lookup"><span data-stu-id="62462-142">NOTES</span></span>

## <span data-ttu-id="62462-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62462-143">RELATED LINKS</span></span>

[<span data-ttu-id="62462-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="62462-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="62462-146">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="62462-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="62462-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="62462-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="62462-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="62462-150">Update-AzVmss</span></span>](./Update-AzVmss.md)

