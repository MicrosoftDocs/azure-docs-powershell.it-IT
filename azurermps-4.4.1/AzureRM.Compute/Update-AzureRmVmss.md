---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518327"
---
# <span data-ttu-id="da70b-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="da70b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da70b-102">SYNOPSIS</span></span>
<span data-ttu-id="da70b-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="da70b-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da70b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da70b-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da70b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da70b-105">DESCRIPTION</span></span>
<span data-ttu-id="da70b-106">Il cmdlet **Update-AzureRmVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="da70b-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="da70b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da70b-107">EXAMPLES</span></span>

### <span data-ttu-id="da70b-108">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="da70b-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="da70b-109">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale denominato LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="da70b-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="da70b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da70b-110">PARAMETERS</span></span>

### <span data-ttu-id="da70b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da70b-111">-DefaultProfile</span></span>
<span data-ttu-id="da70b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da70b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da70b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da70b-113">-ResourceGroupName</span></span>
<span data-ttu-id="da70b-114">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="da70b-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="da70b-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="da70b-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="da70b-116">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="da70b-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="da70b-117">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="da70b-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="da70b-118">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="da70b-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da70b-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="da70b-119">-VMScaleSetName</span></span>
<span data-ttu-id="da70b-120">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da70b-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da70b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da70b-121">-Confirm</span></span>
<span data-ttu-id="da70b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da70b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da70b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da70b-123">-WhatIf</span></span>
<span data-ttu-id="da70b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da70b-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="da70b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da70b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da70b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da70b-126">CommonParameters</span></span>
<span data-ttu-id="da70b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da70b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da70b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da70b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da70b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da70b-129">INPUTS</span></span>

## <span data-ttu-id="da70b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da70b-130">OUTPUTS</span></span>

## <span data-ttu-id="da70b-131">Note</span><span class="sxs-lookup"><span data-stu-id="da70b-131">NOTES</span></span>

## <span data-ttu-id="da70b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da70b-132">RELATED LINKS</span></span>

[<span data-ttu-id="da70b-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="da70b-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="da70b-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="da70b-136">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="da70b-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="da70b-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="da70b-139">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="da70b-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


