---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507568"
---
# <span data-ttu-id="aaa1e-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="aaa1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaa1e-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa1e-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaa1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaa1e-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaa1e-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa1e-106">Il cmdlet **Start-AzureRmVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="aaa1e-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="aaa1e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaa1e-108">EXAMPLES</span></span>

### <span data-ttu-id="aaa1e-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="aaa1e-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="aaa1e-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="aaa1e-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="aaa1e-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="aaa1e-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="aaa1e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaa1e-113">PARAMETERS</span></span>

### <span data-ttu-id="aaa1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaa1e-114">-AsJob</span></span>
<span data-ttu-id="aaa1e-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aaa1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa1e-116">-DefaultProfile</span></span>
<span data-ttu-id="aaa1e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa1e-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="aaa1e-118">-InstanceId</span></span>
<span data-ttu-id="aaa1e-119">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="aaa1e-120">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="aaa1e-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaa1e-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa1e-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aaa1e-123">-VMScaleSetName</span></span>
<span data-ttu-id="aaa1e-124">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa1e-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaa1e-125">-Confirm</span></span>
<span data-ttu-id="aaa1e-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa1e-127">-WhatIf</span></span>
<span data-ttu-id="aaa1e-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaa1e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa1e-130">CommonParameters</span></span>
<span data-ttu-id="aaa1e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa1e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa1e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa1e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaa1e-133">INPUTS</span></span>

### <span data-ttu-id="aaa1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aaa1e-134">System.String</span></span>

### <span data-ttu-id="aaa1e-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="aaa1e-135">System.String[]</span></span>

## <span data-ttu-id="aaa1e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaa1e-136">OUTPUTS</span></span>

### <span data-ttu-id="aaa1e-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="aaa1e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="aaa1e-138">Note</span><span class="sxs-lookup"><span data-stu-id="aaa1e-138">NOTES</span></span>

## <span data-ttu-id="aaa1e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaa1e-139">RELATED LINKS</span></span>

[<span data-ttu-id="aaa1e-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-141">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-143">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-145">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="aaa1e-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa1e-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


