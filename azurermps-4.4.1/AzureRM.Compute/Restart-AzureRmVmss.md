---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508655"
---
# <span data-ttu-id="3028e-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="3028e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3028e-102">SYNOPSIS</span></span>
<span data-ttu-id="3028e-103">Riavvia VMSS o una macchina virtuale all'interno di VMSS.</span><span class="sxs-lookup"><span data-stu-id="3028e-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3028e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3028e-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3028e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3028e-105">DESCRIPTION</span></span>
<span data-ttu-id="3028e-106">Il cmdlet **Restart-AzureRmVmss riavvia** il set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3028e-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3028e-107">Questo cmdlet può essere usato anche per riavviare una specifica macchina virtuale all'interno di VMSS usando il parametro *InstanceID* .</span><span class="sxs-lookup"><span data-stu-id="3028e-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="3028e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3028e-108">EXAMPLES</span></span>

### <span data-ttu-id="3028e-109">Esempio 1: riavviare il VMSS</span><span class="sxs-lookup"><span data-stu-id="3028e-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="3028e-110">Questo comando Riavvia il VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="3028e-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="3028e-111">Esempio 2: riavviare una specifica macchina virtuale all'interno di VMSS</span><span class="sxs-lookup"><span data-stu-id="3028e-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="3028e-112">Questo comando Riavvia una macchina virtuale con l'ID istanza di 1 nella VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="3028e-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="3028e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3028e-113">PARAMETERS</span></span>

### <span data-ttu-id="3028e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3028e-114">-DefaultProfile</span></span>
<span data-ttu-id="3028e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3028e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3028e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3028e-116">-InstanceId</span></span>
<span data-ttu-id="3028e-117">Specifica, come matrice di stringhe, l'ID delle istanze che devono essere riavviate.</span><span class="sxs-lookup"><span data-stu-id="3028e-117">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="3028e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3028e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3028e-119">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="3028e-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3028e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3028e-120">-VMScaleSetName</span></span>
<span data-ttu-id="3028e-121">Specie il nome del VMSS riavviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3028e-121">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="3028e-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3028e-122">-Confirm</span></span>
<span data-ttu-id="3028e-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3028e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3028e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3028e-124">-WhatIf</span></span>
<span data-ttu-id="3028e-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3028e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3028e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3028e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3028e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3028e-127">CommonParameters</span></span>
<span data-ttu-id="3028e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3028e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3028e-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3028e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3028e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3028e-130">INPUTS</span></span>

## <span data-ttu-id="3028e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3028e-131">OUTPUTS</span></span>

###  
<span data-ttu-id="3028e-132">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3028e-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3028e-133">Note</span><span class="sxs-lookup"><span data-stu-id="3028e-133">NOTES</span></span>

## <span data-ttu-id="3028e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3028e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3028e-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="3028e-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3028e-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="3028e-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="3028e-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3028e-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3028e-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3028e-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


