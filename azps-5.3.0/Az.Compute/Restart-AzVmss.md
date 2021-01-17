---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488231"
---
# <span data-ttu-id="07060-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-101">Restart-AzVmss</span></span>

## <span data-ttu-id="07060-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07060-102">SYNOPSIS</span></span>
<span data-ttu-id="07060-103">Riavvia VMSS o una macchina virtuale all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="07060-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="07060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07060-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07060-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07060-105">DESCRIPTION</span></span>
<span data-ttu-id="07060-106">Il cmdlet **Restart-AzVmss riavvia** il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="07060-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="07060-107">Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .</span><span class="sxs-lookup"><span data-stu-id="07060-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="07060-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07060-108">EXAMPLES</span></span>

### <span data-ttu-id="07060-109">Esempio 1: riavviare il VMSS</span><span class="sxs-lookup"><span data-stu-id="07060-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="07060-110">Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="07060-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="07060-111">Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="07060-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="07060-112">Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="07060-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="07060-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07060-113">PARAMETERS</span></span>

### <span data-ttu-id="07060-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07060-114">-AsJob</span></span>
<span data-ttu-id="07060-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="07060-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="07060-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07060-116">-DefaultProfile</span></span>
<span data-ttu-id="07060-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07060-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07060-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="07060-118">-InstanceId</span></span>
<span data-ttu-id="07060-119">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.</span><span class="sxs-lookup"><span data-stu-id="07060-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="07060-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07060-120">-ResourceGroupName</span></span>
<span data-ttu-id="07060-121">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="07060-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="07060-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07060-122">-VMScaleSetName</span></span>
<span data-ttu-id="07060-123">Specie il nome del VMSS riavviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07060-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="07060-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07060-124">-Confirm</span></span>
<span data-ttu-id="07060-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07060-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07060-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07060-126">-WhatIf</span></span>
<span data-ttu-id="07060-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07060-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07060-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07060-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07060-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07060-129">CommonParameters</span></span>
<span data-ttu-id="07060-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07060-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07060-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07060-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07060-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07060-132">INPUTS</span></span>

### <span data-ttu-id="07060-133">System. String</span><span class="sxs-lookup"><span data-stu-id="07060-133">System.String</span></span>

### <span data-ttu-id="07060-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="07060-134">System.String[]</span></span>

## <span data-ttu-id="07060-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07060-135">OUTPUTS</span></span>

### <span data-ttu-id="07060-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="07060-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="07060-137">Note</span><span class="sxs-lookup"><span data-stu-id="07060-137">NOTES</span></span>

## <span data-ttu-id="07060-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07060-138">RELATED LINKS</span></span>

[<span data-ttu-id="07060-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="07060-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="07060-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="07060-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="07060-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="07060-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="07060-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="07060-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


