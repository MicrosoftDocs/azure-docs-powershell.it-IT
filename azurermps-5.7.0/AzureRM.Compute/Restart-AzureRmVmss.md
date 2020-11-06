---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521082"
---
# <span data-ttu-id="5d7c2-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="5d7c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d7c2-103">Riavvia VMSS o una macchina virtuale all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d7c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d7c2-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d7c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="5d7c2-106">Il cmdlet **Restart-AzureRmVmss riavvia** il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5d7c2-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="5d7c2-107">Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .</span><span class="sxs-lookup"><span data-stu-id="5d7c2-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="5d7c2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d7c2-108">EXAMPLES</span></span>

### <span data-ttu-id="5d7c2-109">Esempio 1: riavviare il VMSS</span><span class="sxs-lookup"><span data-stu-id="5d7c2-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="5d7c2-110">Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="5d7c2-111">Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="5d7c2-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5d7c2-112">Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5d7c2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d7c2-113">PARAMETERS</span></span>

### <span data-ttu-id="5d7c2-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5d7c2-114">-InstanceId</span></span>
<span data-ttu-id="5d7c2-115">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="5d7c2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d7c2-116">-ResourceGroupName</span></span>
<span data-ttu-id="5d7c2-117">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5d7c2-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5d7c2-118">-VMScaleSetName</span></span>
<span data-ttu-id="5d7c2-119">Specie il nome del VMSS riavviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="5d7c2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d7c2-120">-Confirm</span></span>
<span data-ttu-id="5d7c2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d7c2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d7c2-122">-WhatIf</span></span>
<span data-ttu-id="5d7c2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d7c2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d7c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d7c2-125">CommonParameters</span></span>
<span data-ttu-id="5d7c2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d7c2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d7c2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d7c2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d7c2-128">INPUTS</span></span>

### <span data-ttu-id="5d7c2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5d7c2-129">None</span></span>
<span data-ttu-id="5d7c2-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d7c2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d7c2-131">OUTPUTS</span></span>

###  
<span data-ttu-id="5d7c2-132">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5d7c2-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5d7c2-133">Note</span><span class="sxs-lookup"><span data-stu-id="5d7c2-133">NOTES</span></span>

## <span data-ttu-id="5d7c2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d7c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="5d7c2-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="5d7c2-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5d7c2-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


