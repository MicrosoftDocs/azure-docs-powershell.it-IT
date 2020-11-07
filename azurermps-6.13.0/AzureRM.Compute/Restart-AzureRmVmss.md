---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 9f4727fc9bc5a735f837d3bec5eced9cd20e9254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688140"
---
# <span data-ttu-id="56d98-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="56d98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56d98-102">SYNOPSIS</span></span>
<span data-ttu-id="56d98-103">Riavvia VMSS o una macchina virtuale all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="56d98-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56d98-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56d98-105">DESCRIPTION</span></span>
<span data-ttu-id="56d98-106">Il cmdlet **Restart-AzureRmVmss riavvia** il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="56d98-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="56d98-107">Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .</span><span class="sxs-lookup"><span data-stu-id="56d98-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="56d98-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56d98-108">EXAMPLES</span></span>

### <span data-ttu-id="56d98-109">Esempio 1: riavviare il VMSS</span><span class="sxs-lookup"><span data-stu-id="56d98-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="56d98-110">Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="56d98-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="56d98-111">Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="56d98-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="56d98-112">Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="56d98-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="56d98-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56d98-113">PARAMETERS</span></span>

### <span data-ttu-id="56d98-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56d98-114">-AsJob</span></span>
<span data-ttu-id="56d98-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="56d98-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="56d98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d98-116">-DefaultProfile</span></span>
<span data-ttu-id="56d98-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56d98-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d98-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="56d98-118">-InstanceId</span></span>
<span data-ttu-id="56d98-119">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.</span><span class="sxs-lookup"><span data-stu-id="56d98-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="56d98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d98-120">-ResourceGroupName</span></span>
<span data-ttu-id="56d98-121">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="56d98-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="56d98-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56d98-122">-VMScaleSetName</span></span>
<span data-ttu-id="56d98-123">Specie il nome del VMSS riavviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d98-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="56d98-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56d98-124">-Confirm</span></span>
<span data-ttu-id="56d98-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d98-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d98-126">-WhatIf</span></span>
<span data-ttu-id="56d98-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56d98-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56d98-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56d98-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d98-129">CommonParameters</span></span>
<span data-ttu-id="56d98-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d98-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d98-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d98-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56d98-132">INPUTS</span></span>

### <span data-ttu-id="56d98-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56d98-133">System.String</span></span>

### <span data-ttu-id="56d98-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="56d98-134">System.String[]</span></span>

## <span data-ttu-id="56d98-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56d98-135">OUTPUTS</span></span>

### <span data-ttu-id="56d98-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="56d98-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="56d98-137">Note</span><span class="sxs-lookup"><span data-stu-id="56d98-137">NOTES</span></span>

## <span data-ttu-id="56d98-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56d98-138">RELATED LINKS</span></span>

[<span data-ttu-id="56d98-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="56d98-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="56d98-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="56d98-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="56d98-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="56d98-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="56d98-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56d98-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


