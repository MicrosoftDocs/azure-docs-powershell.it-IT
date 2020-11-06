---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510748"
---
# <span data-ttu-id="0aa27-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="0aa27-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="0aa27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0aa27-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa27-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="0aa27-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aa27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0aa27-104">SYNTAX</span></span>

### <span data-ttu-id="0aa27-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0aa27-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa27-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0aa27-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aa27-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa27-108">Il cmdlet **set-AzureRmVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="0aa27-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0aa27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0aa27-109">EXAMPLES</span></span>

## <span data-ttu-id="0aa27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0aa27-110">PARAMETERS</span></span>

### <span data-ttu-id="0aa27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa27-111">-DefaultProfile</span></span>
<span data-ttu-id="0aa27-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa27-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0aa27-113">-InstanceId</span></span>
<span data-ttu-id="0aa27-114">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="0aa27-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa27-115">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="0aa27-115">-Reimage</span></span>
<span data-ttu-id="0aa27-116">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="0aa27-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="0aa27-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="0aa27-117">-ReimageAll</span></span>
<span data-ttu-id="0aa27-118">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="0aa27-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="0aa27-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa27-119">-ResourceGroupName</span></span>
<span data-ttu-id="0aa27-120">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="0aa27-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="0aa27-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0aa27-121">-VMScaleSetName</span></span>
<span data-ttu-id="0aa27-122">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aa27-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0aa27-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0aa27-123">-Confirm</span></span>
<span data-ttu-id="0aa27-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aa27-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aa27-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa27-125">-WhatIf</span></span>
<span data-ttu-id="0aa27-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0aa27-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0aa27-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0aa27-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aa27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa27-128">CommonParameters</span></span>
<span data-ttu-id="0aa27-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa27-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa27-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa27-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0aa27-131">INPUTS</span></span>

## <span data-ttu-id="0aa27-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0aa27-132">OUTPUTS</span></span>

## <span data-ttu-id="0aa27-133">Note</span><span class="sxs-lookup"><span data-stu-id="0aa27-133">NOTES</span></span>

## <span data-ttu-id="0aa27-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0aa27-134">RELATED LINKS</span></span>

[<span data-ttu-id="0aa27-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="0aa27-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
