---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022564"
---
# <span data-ttu-id="6f84f-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-101">Start-AzVmss</span></span>

## <span data-ttu-id="6f84f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f84f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f84f-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f84f-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="6f84f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f84f-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f84f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f84f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f84f-106">Il cmdlet **Start-AzVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6f84f-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="6f84f-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6f84f-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="6f84f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f84f-108">EXAMPLES</span></span>

### <span data-ttu-id="6f84f-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="6f84f-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="6f84f-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6f84f-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="6f84f-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="6f84f-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="6f84f-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6f84f-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6f84f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f84f-113">PARAMETERS</span></span>

### <span data-ttu-id="6f84f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f84f-114">-AsJob</span></span>
<span data-ttu-id="6f84f-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="6f84f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6f84f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f84f-116">-DefaultProfile</span></span>
<span data-ttu-id="6f84f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f84f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f84f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6f84f-118">-InstanceId</span></span>
<span data-ttu-id="6f84f-119">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f84f-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="6f84f-120">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="6f84f-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="6f84f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f84f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f84f-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f84f-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6f84f-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6f84f-123">-VMScaleSetName</span></span>
<span data-ttu-id="6f84f-124">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6f84f-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="6f84f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6f84f-125">-Confirm</span></span>
<span data-ttu-id="6f84f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f84f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f84f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f84f-127">-WhatIf</span></span>
<span data-ttu-id="6f84f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f84f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f84f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f84f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f84f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f84f-130">CommonParameters</span></span>
<span data-ttu-id="6f84f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f84f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f84f-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f84f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f84f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f84f-133">INPUTS</span></span>

### <span data-ttu-id="6f84f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6f84f-134">System.String</span></span>

### <span data-ttu-id="6f84f-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="6f84f-135">System.String[]</span></span>

## <span data-ttu-id="6f84f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f84f-136">OUTPUTS</span></span>

### <span data-ttu-id="6f84f-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6f84f-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6f84f-138">Note</span><span class="sxs-lookup"><span data-stu-id="6f84f-138">NOTES</span></span>

## <span data-ttu-id="6f84f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f84f-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f84f-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6f84f-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6f84f-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6f84f-143">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6f84f-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6f84f-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6f84f-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f84f-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


