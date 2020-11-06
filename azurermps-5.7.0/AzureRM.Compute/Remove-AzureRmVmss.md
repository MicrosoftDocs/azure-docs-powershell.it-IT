---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516859"
---
# <span data-ttu-id="fcd1c-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="fcd1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd1c-103">Rimuove VMSS o una macchina virtuale che si trova all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcd1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcd1c-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd1c-106">Il cmdlet **Remove-AzureRmVmss** rimuove il set di scale della macchina virtuale (VMSS) da Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="fcd1c-107">Questo cmdlet può essere usato anche per rimuovere una macchina virtuale specifica all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="fcd1c-108">Puoi usare il parametro *InstanceID* per rimuovere una macchina virtuale specifica all'interno di vmss.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="fcd1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcd1c-109">EXAMPLES</span></span>

### <span data-ttu-id="fcd1c-110">Esempio 1: rimuovere un VMSS</span><span class="sxs-lookup"><span data-stu-id="fcd1c-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="fcd1c-111">Questo comando rimuove il VMSS denominato VMScaleSet001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="fcd1c-112">Esempio 2: rimuovere una macchina virtuale dall'interno di un VMSS</span><span class="sxs-lookup"><span data-stu-id="fcd1c-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="fcd1c-113">Questo comando rimuove la macchina virtuale con l'ID di istanza 3 dalla VMSS denominata VMScaleSet002 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="fcd1c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcd1c-114">PARAMETERS</span></span>

### <span data-ttu-id="fcd1c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fcd1c-115">-Force</span></span>
<span data-ttu-id="fcd1c-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd1c-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fcd1c-117">-InstanceId</span></span>
<span data-ttu-id="fcd1c-118">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="fcd1c-119">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="fcd1c-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="fcd1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="fcd1c-121">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="fcd1c-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fcd1c-122">-VMScaleSetName</span></span>
<span data-ttu-id="fcd1c-123">Specie il nome del VMSS rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="fcd1c-124">Se specifichi il parametro *InstanceID* , il cmdlet rimuoverà la macchina virtuale specificata dalla vmss denominata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="fcd1c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fcd1c-125">-Confirm</span></span>
<span data-ttu-id="fcd1c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-126">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="fcd1c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd1c-127">-WhatIf</span></span>
<span data-ttu-id="fcd1c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcd1c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-129">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="fcd1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd1c-130">CommonParameters</span></span>
<span data-ttu-id="fcd1c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd1c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd1c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd1c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcd1c-133">INPUTS</span></span>

### <span data-ttu-id="fcd1c-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fcd1c-134">None</span></span>
<span data-ttu-id="fcd1c-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fcd1c-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcd1c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcd1c-136">OUTPUTS</span></span>

## <span data-ttu-id="fcd1c-137">Note</span><span class="sxs-lookup"><span data-stu-id="fcd1c-137">NOTES</span></span>

## <span data-ttu-id="fcd1c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcd1c-138">RELATED LINKS</span></span>

[<span data-ttu-id="fcd1c-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-141">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="fcd1c-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fcd1c-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


