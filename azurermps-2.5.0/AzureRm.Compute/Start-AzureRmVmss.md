---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866894"
---
# <span data-ttu-id="13973-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="13973-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13973-102">SYNOPSIS</span></span>
<span data-ttu-id="13973-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="13973-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13973-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13973-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13973-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13973-105">DESCRIPTION</span></span>
<span data-ttu-id="13973-106">Il cmdlet **Start-AzureRmVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="13973-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="13973-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="13973-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="13973-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13973-108">EXAMPLES</span></span>

### <span data-ttu-id="13973-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="13973-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="13973-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="13973-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="13973-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="13973-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="13973-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="13973-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="13973-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13973-113">PARAMETERS</span></span>

### <span data-ttu-id="13973-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13973-114">-AsJob</span></span>
<span data-ttu-id="13973-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="13973-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="13973-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13973-116">-DefaultProfile</span></span>
<span data-ttu-id="13973-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13973-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13973-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="13973-118">-InstanceId</span></span>
<span data-ttu-id="13973-119">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13973-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="13973-120">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="13973-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="13973-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13973-121">-ResourceGroupName</span></span>
<span data-ttu-id="13973-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="13973-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="13973-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13973-123">-VMScaleSetName</span></span>
<span data-ttu-id="13973-124">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="13973-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="13973-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13973-125">-Confirm</span></span>
<span data-ttu-id="13973-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13973-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13973-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13973-127">-WhatIf</span></span>
<span data-ttu-id="13973-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13973-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13973-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13973-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13973-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13973-130">CommonParameters</span></span>
<span data-ttu-id="13973-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13973-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13973-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13973-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13973-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13973-133">INPUTS</span></span>

### <span data-ttu-id="13973-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="13973-134">None</span></span>
<span data-ttu-id="13973-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="13973-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13973-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13973-136">OUTPUTS</span></span>

###  
<span data-ttu-id="13973-137">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="13973-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="13973-138">Note</span><span class="sxs-lookup"><span data-stu-id="13973-138">NOTES</span></span>

## <span data-ttu-id="13973-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13973-139">RELATED LINKS</span></span>

[<span data-ttu-id="13973-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="13973-141">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="13973-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="13973-143">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="13973-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="13973-145">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="13973-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13973-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


