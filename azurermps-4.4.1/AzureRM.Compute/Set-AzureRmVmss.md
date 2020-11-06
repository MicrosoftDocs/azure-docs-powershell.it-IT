---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508603"
---
# <span data-ttu-id="81f4c-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="81f4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="81f4c-103">Imposta azioni specifiche in un determinato VMSS.</span><span class="sxs-lookup"><span data-stu-id="81f4c-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81f4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81f4c-104">SYNTAX</span></span>

### <span data-ttu-id="81f4c-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81f4c-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f4c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="81f4c-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f4c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="81f4c-108">Il cmdlet **set-AzureRmVmss** imposta azioni specifiche nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="81f4c-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="81f4c-109">L'unica azione supportata da questo cmdlet è reimage.</span><span class="sxs-lookup"><span data-stu-id="81f4c-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="81f4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81f4c-110">EXAMPLES</span></span>

### <span data-ttu-id="81f4c-111">Esempio 1: riimmagine di un VMSS</span><span class="sxs-lookup"><span data-stu-id="81f4c-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="81f4c-112">Questo comando riimmaginerà la VMSS denominata ContosoVMSS che appartiene al gruppo di risorse denominato ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="81f4c-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="81f4c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81f4c-113">PARAMETERS</span></span>

### <span data-ttu-id="81f4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f4c-114">-DefaultProfile</span></span>
<span data-ttu-id="81f4c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81f4c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81f4c-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="81f4c-116">-InstanceId</span></span>
<span data-ttu-id="81f4c-117">ID istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81f4c-117">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="81f4c-118">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="81f4c-118">-Reimage</span></span>
<span data-ttu-id="81f4c-119">Indica che il cmdlet riimmaginerà il VMSS.</span><span class="sxs-lookup"><span data-stu-id="81f4c-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f4c-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="81f4c-120">-ReimageAll</span></span>
<span data-ttu-id="81f4c-121">Indica che il cmdlet riimmaginerà tutti i dischi in VMSS.</span><span class="sxs-lookup"><span data-stu-id="81f4c-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="81f4c-123">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="81f4c-123">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="81f4c-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="81f4c-124">-VMScaleSetName</span></span>
<span data-ttu-id="81f4c-125">Specie il nome del VMSS per cui questo cmdlet imposta le azioni.</span><span class="sxs-lookup"><span data-stu-id="81f4c-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="81f4c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81f4c-126">-Confirm</span></span>
<span data-ttu-id="81f4c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81f4c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f4c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f4c-128">-WhatIf</span></span>
<span data-ttu-id="81f4c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81f4c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81f4c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81f4c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f4c-131">CommonParameters</span></span>
<span data-ttu-id="81f4c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f4c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f4c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f4c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81f4c-134">INPUTS</span></span>

## <span data-ttu-id="81f4c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81f4c-135">OUTPUTS</span></span>

### <span data-ttu-id="81f4c-136">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="81f4c-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="81f4c-137">Note</span><span class="sxs-lookup"><span data-stu-id="81f4c-137">NOTES</span></span>

## <span data-ttu-id="81f4c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81f4c-138">RELATED LINKS</span></span>

[<span data-ttu-id="81f4c-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="81f4c-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="81f4c-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="81f4c-142">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="81f4c-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="81f4c-144">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="81f4c-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81f4c-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


