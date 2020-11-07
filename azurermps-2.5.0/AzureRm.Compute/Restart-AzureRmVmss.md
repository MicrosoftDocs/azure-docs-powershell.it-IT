---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866908"
---
# <span data-ttu-id="32e59-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="32e59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32e59-102">SYNOPSIS</span></span>
<span data-ttu-id="32e59-103">Riavvia VMSS o una macchina virtuale all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="32e59-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32e59-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32e59-105">DESCRIPTION</span></span>
<span data-ttu-id="32e59-106">Il cmdlet **Restart-AzureRmVmss riavvia** il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="32e59-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="32e59-107">Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .</span><span class="sxs-lookup"><span data-stu-id="32e59-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="32e59-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32e59-108">EXAMPLES</span></span>

### <span data-ttu-id="32e59-109">Esempio 1: riavviare il VMSS</span><span class="sxs-lookup"><span data-stu-id="32e59-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="32e59-110">Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="32e59-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="32e59-111">Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="32e59-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="32e59-112">Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="32e59-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="32e59-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32e59-113">PARAMETERS</span></span>

### <span data-ttu-id="32e59-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32e59-114">-AsJob</span></span>
<span data-ttu-id="32e59-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="32e59-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="32e59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e59-116">-DefaultProfile</span></span>
<span data-ttu-id="32e59-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32e59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e59-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="32e59-118">-InstanceId</span></span>
<span data-ttu-id="32e59-119">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.</span><span class="sxs-lookup"><span data-stu-id="32e59-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="32e59-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e59-120">-ResourceGroupName</span></span>
<span data-ttu-id="32e59-121">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="32e59-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="32e59-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="32e59-122">-VMScaleSetName</span></span>
<span data-ttu-id="32e59-123">Specie il nome del VMSS riavviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e59-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="32e59-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32e59-124">-Confirm</span></span>
<span data-ttu-id="32e59-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e59-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e59-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e59-126">-WhatIf</span></span>
<span data-ttu-id="32e59-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e59-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32e59-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e59-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e59-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e59-129">CommonParameters</span></span>
<span data-ttu-id="32e59-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e59-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e59-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e59-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e59-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32e59-132">INPUTS</span></span>

### <span data-ttu-id="32e59-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="32e59-133">None</span></span>
<span data-ttu-id="32e59-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="32e59-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="32e59-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32e59-135">OUTPUTS</span></span>

###  
<span data-ttu-id="32e59-136">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="32e59-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="32e59-137">Note</span><span class="sxs-lookup"><span data-stu-id="32e59-137">NOTES</span></span>

## <span data-ttu-id="32e59-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32e59-138">RELATED LINKS</span></span>

[<span data-ttu-id="32e59-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="32e59-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="32e59-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="32e59-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="32e59-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="32e59-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="32e59-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="32e59-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


