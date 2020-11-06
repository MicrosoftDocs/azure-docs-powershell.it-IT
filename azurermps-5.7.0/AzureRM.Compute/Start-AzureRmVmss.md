---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516831"
---
# <span data-ttu-id="2bd2a-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="2bd2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd2a-103">Avvia VMSS o un set di macchine virtuali all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bd2a-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd2a-106">Il cmdlet **Start-AzureRmVmss** avvia tutte le macchine virtuali all'interno del set di scale della macchina virtuale (VMSS) o un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="2bd2a-107">Puoi usare il parametro *InstanceID* per selezionare un set di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="2bd2a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bd2a-108">EXAMPLES</span></span>

### <span data-ttu-id="2bd2a-109">Esempio 1: avviare un set specifico di macchine virtuali all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="2bd2a-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="2bd2a-110">Questo comando avvia un set specifico di macchine virtuali specificato dalla matrice di stringhe di ID istanza che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="2bd2a-111">Esempio 2: avviare tutte le macchine virtuali all'interno del VMSS</span><span class="sxs-lookup"><span data-stu-id="2bd2a-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="2bd2a-112">Questo comando avvia tutte le macchine virtuali che appartengono alla VMSS denominata ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="2bd2a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bd2a-113">PARAMETERS</span></span>

### <span data-ttu-id="2bd2a-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2bd2a-114">-InstanceId</span></span>
<span data-ttu-id="2bd2a-115">Specifica, come matrice di stringhe, l'ID o gli ID delle istanze avviate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="2bd2a-116">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="2bd2a-116">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="2bd2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="2bd2a-118">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-118">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="2bd2a-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2bd2a-119">-VMScaleSetName</span></span>
<span data-ttu-id="2bd2a-120">Specifica il nome del VMSS che questo cmdlet avvia le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="2bd2a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bd2a-121">-Confirm</span></span>
<span data-ttu-id="2bd2a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd2a-123">-WhatIf</span></span>
<span data-ttu-id="2bd2a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd2a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd2a-126">CommonParameters</span></span>
<span data-ttu-id="2bd2a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd2a-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd2a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd2a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bd2a-129">INPUTS</span></span>

### <span data-ttu-id="2bd2a-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2bd2a-130">None</span></span>
<span data-ttu-id="2bd2a-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bd2a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bd2a-132">OUTPUTS</span></span>

###  
<span data-ttu-id="2bd2a-133">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2bd2a-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2bd2a-134">Note</span><span class="sxs-lookup"><span data-stu-id="2bd2a-134">NOTES</span></span>

## <span data-ttu-id="2bd2a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bd2a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2bd2a-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-139">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-141">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="2bd2a-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2bd2a-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


