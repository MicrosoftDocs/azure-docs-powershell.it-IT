---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 54c6f9f399cfabf7a418939b4662c9bcfdc83d34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520258"
---
# <span data-ttu-id="82ba8-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="82ba8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="82ba8-103">Rimuove VMSS o una macchina virtuale che si trova all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="82ba8-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ba8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82ba8-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ba8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="82ba8-106">Il cmdlet **Remove-AzureRmVmss** rimuove il set di scale della macchina virtuale (VMSS) da Azure.</span><span class="sxs-lookup"><span data-stu-id="82ba8-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="82ba8-107">Questo cmdlet può essere usato anche per rimuovere una macchina virtuale specifica all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="82ba8-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="82ba8-108">Puoi usare il parametro *InstanceID* per rimuovere una macchina virtuale specifica all'interno di vmss.</span><span class="sxs-lookup"><span data-stu-id="82ba8-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="82ba8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82ba8-109">EXAMPLES</span></span>

### <span data-ttu-id="82ba8-110">Esempio 1: rimuovere un VMSS</span><span class="sxs-lookup"><span data-stu-id="82ba8-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="82ba8-111">Questo comando rimuove il VMSS denominato VMScaleSet001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="82ba8-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="82ba8-112">Esempio 2: rimuovere una macchina virtuale dall'interno di un VMSS</span><span class="sxs-lookup"><span data-stu-id="82ba8-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="82ba8-113">Questo comando rimuove la macchina virtuale con l'ID di istanza 3 dalla VMSS denominata VMScaleSet002 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="82ba8-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="82ba8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82ba8-114">PARAMETERS</span></span>

### <span data-ttu-id="82ba8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82ba8-115">-AsJob</span></span>
<span data-ttu-id="82ba8-116">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="82ba8-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="82ba8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ba8-117">-DefaultProfile</span></span>
<span data-ttu-id="82ba8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82ba8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ba8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="82ba8-119">-Force</span></span>
<span data-ttu-id="82ba8-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82ba8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82ba8-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="82ba8-121">-InstanceId</span></span>
<span data-ttu-id="82ba8-122">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="82ba8-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="82ba8-123">Ad esempio: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="82ba8-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="82ba8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ba8-124">-ResourceGroupName</span></span>
<span data-ttu-id="82ba8-125">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="82ba8-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="82ba8-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="82ba8-126">-VMScaleSetName</span></span>
<span data-ttu-id="82ba8-127">Specie il nome del VMSS rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ba8-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="82ba8-128">Se specifichi il parametro *InstanceID* , il cmdlet rimuoverà la macchina virtuale specificata dalla vmss denominata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82ba8-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="82ba8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82ba8-129">-Confirm</span></span>
<span data-ttu-id="82ba8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ba8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ba8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ba8-131">-WhatIf</span></span>
<span data-ttu-id="82ba8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82ba8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82ba8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82ba8-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ba8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ba8-134">CommonParameters</span></span>
<span data-ttu-id="82ba8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ba8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ba8-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ba8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ba8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82ba8-137">INPUTS</span></span>

### <span data-ttu-id="82ba8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="82ba8-138">System.String</span></span>

### <span data-ttu-id="82ba8-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="82ba8-139">System.String[]</span></span>

## <span data-ttu-id="82ba8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82ba8-140">OUTPUTS</span></span>

### <span data-ttu-id="82ba8-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="82ba8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="82ba8-142">Note</span><span class="sxs-lookup"><span data-stu-id="82ba8-142">NOTES</span></span>

## <span data-ttu-id="82ba8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82ba8-143">RELATED LINKS</span></span>

[<span data-ttu-id="82ba8-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="82ba8-145">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="82ba8-146">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="82ba8-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="82ba8-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="82ba8-149">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="82ba8-150">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="82ba8-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


