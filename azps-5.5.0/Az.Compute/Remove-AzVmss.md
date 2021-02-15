---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177535"
---
# <span data-ttu-id="7427f-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-101">Remove-AzVmss</span></span>

## <span data-ttu-id="7427f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7427f-102">SYNOPSIS</span></span>
<span data-ttu-id="7427f-103">Rimuove il sistema VMSS o una macchina virtuale che si trova all'interno del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="7427f-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="7427f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7427f-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7427f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7427f-105">DESCRIPTION</span></span>
<span data-ttu-id="7427f-106">Il cmdlet **Remove-AzVmss** rimuove il set di scalabilità delle macchine virtuali (VMSS) da Azure.</span><span class="sxs-lookup"><span data-stu-id="7427f-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="7427f-107">Questo cmdlet può essere usato anche per rimuovere una macchina virtuale specifica all'interno del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="7427f-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="7427f-108">È possibile usare il *parametro InstanceId* per rimuovere una macchina virtuale specifica all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="7427f-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="7427f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7427f-109">EXAMPLES</span></span>

### <span data-ttu-id="7427f-110">Esempio 1: Rimuovere un vms</span><span class="sxs-lookup"><span data-stu-id="7427f-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="7427f-111">Questo comando rimuove il sistema VMSS denominato VMScaleSet001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="7427f-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="7427f-112">Esempio 2: Rimuovere una macchina virtuale da un VMSS</span><span class="sxs-lookup"><span data-stu-id="7427f-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="7427f-113">Questo comando rimuove la macchina virtuale con ID istanza 3 dal sistema VMSS denominato VMScaleSet002 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="7427f-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="7427f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7427f-114">PARAMETERS</span></span>

### <span data-ttu-id="7427f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7427f-115">-AsJob</span></span>
<span data-ttu-id="7427f-116">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="7427f-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7427f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7427f-117">-DefaultProfile</span></span>
<span data-ttu-id="7427f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7427f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7427f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7427f-119">-Force</span></span>
<span data-ttu-id="7427f-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="7427f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7427f-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7427f-121">-InstanceId</span></span>
<span data-ttu-id="7427f-122">Specifica, come matrice di stringhe, l'ID delle istanze da iniziare.</span><span class="sxs-lookup"><span data-stu-id="7427f-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="7427f-123">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="7427f-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="7427f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7427f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7427f-125">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="7427f-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="7427f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7427f-126">-VMScaleSetName</span></span>
<span data-ttu-id="7427f-127">Specie il nome del sistema VMSS rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7427f-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="7427f-128">Se si specifica il *parametro InstanceId,* il cmdlet rimuoverà la macchina virtuale specificata dal sistema VMSS denominato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7427f-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="7427f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7427f-129">-Confirm</span></span>
<span data-ttu-id="7427f-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7427f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7427f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7427f-131">-WhatIf</span></span>
<span data-ttu-id="7427f-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7427f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7427f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7427f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7427f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7427f-134">CommonParameters</span></span>
<span data-ttu-id="7427f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7427f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7427f-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7427f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7427f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="7427f-137">INPUTS</span></span>

### <span data-ttu-id="7427f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7427f-138">System.String</span></span>

### <span data-ttu-id="7427f-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7427f-139">System.String[]</span></span>

## <span data-ttu-id="7427f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7427f-140">OUTPUTS</span></span>

### <span data-ttu-id="7427f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7427f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7427f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="7427f-142">NOTES</span></span>

## <span data-ttu-id="7427f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7427f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7427f-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7427f-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7427f-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7427f-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7427f-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7427f-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="7427f-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7427f-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


