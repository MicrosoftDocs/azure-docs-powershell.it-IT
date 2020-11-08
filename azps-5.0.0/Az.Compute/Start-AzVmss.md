---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200236"
---
# <span data-ttu-id="fb974-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-101">Start-AzVmss</span></span>

## <span data-ttu-id="fb974-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb974-102">SYNOPSIS</span></span>
<span data-ttu-id="fb974-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb974-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="fb974-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb974-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb974-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb974-105">DESCRIPTION</span></span>
<span data-ttu-id="fb974-106">Il cmdlet **Start-AzVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="fb974-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="fb974-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="fb974-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="fb974-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb974-108">EXAMPLES</span></span>

### <span data-ttu-id="fb974-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="fb974-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="fb974-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="fb974-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="fb974-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="fb974-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="fb974-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="fb974-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="fb974-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb974-113">PARAMETERS</span></span>

### <span data-ttu-id="fb974-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb974-114">-AsJob</span></span>
<span data-ttu-id="fb974-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="fb974-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb974-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb974-116">-DefaultProfile</span></span>
<span data-ttu-id="fb974-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb974-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb974-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fb974-118">-InstanceId</span></span>
<span data-ttu-id="fb974-119">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb974-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="fb974-120">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="fb974-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="fb974-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb974-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb974-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb974-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="fb974-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fb974-123">-VMScaleSetName</span></span>
<span data-ttu-id="fb974-124">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="fb974-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="fb974-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb974-125">-Confirm</span></span>
<span data-ttu-id="fb974-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb974-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb974-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb974-127">-WhatIf</span></span>
<span data-ttu-id="fb974-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb974-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb974-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb974-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb974-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb974-130">CommonParameters</span></span>
<span data-ttu-id="fb974-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb974-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb974-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb974-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb974-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb974-133">INPUTS</span></span>

### <span data-ttu-id="fb974-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fb974-134">System.String</span></span>

### <span data-ttu-id="fb974-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="fb974-135">System.String[]</span></span>

## <span data-ttu-id="fb974-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb974-136">OUTPUTS</span></span>

### <span data-ttu-id="fb974-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fb974-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fb974-138">Note</span><span class="sxs-lookup"><span data-stu-id="fb974-138">NOTES</span></span>

## <span data-ttu-id="fb974-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb974-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb974-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fb974-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="fb974-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fb974-143">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fb974-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fb974-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fb974-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb974-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


