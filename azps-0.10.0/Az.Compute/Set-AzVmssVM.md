---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861641"
---
# <span data-ttu-id="db5a2-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="db5a2-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="db5a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db5a2-102">SYNOPSIS</span></span>
<span data-ttu-id="db5a2-103">Modifica lo stato di un'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="db5a2-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="db5a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db5a2-104">SYNTAX</span></span>

### <span data-ttu-id="db5a2-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db5a2-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5a2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="db5a2-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db5a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db5a2-107">DESCRIPTION</span></span>
<span data-ttu-id="db5a2-108">Il cmdlet **set-AzVmssVM** modifica lo stato di un'istanza di vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="db5a2-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="db5a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db5a2-109">EXAMPLES</span></span>

## <span data-ttu-id="db5a2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db5a2-110">PARAMETERS</span></span>

### <span data-ttu-id="db5a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db5a2-111">-AsJob</span></span>
<span data-ttu-id="db5a2-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db5a2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db5a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5a2-113">-DefaultProfile</span></span>
<span data-ttu-id="db5a2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db5a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db5a2-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="db5a2-115">-InstanceId</span></span>
<span data-ttu-id="db5a2-116">Specifica l'ID dell'istanza di VMSS per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="db5a2-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db5a2-117">-Riimmagine</span><span class="sxs-lookup"><span data-stu-id="db5a2-117">-Reimage</span></span>
<span data-ttu-id="db5a2-118">Indica che questo cmdlet riimmaginerà l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="db5a2-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5a2-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="db5a2-119">-ReimageAll</span></span>
<span data-ttu-id="db5a2-120">Indica che il cmdlet riimmaginerà tutti i dischi nell'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="db5a2-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="db5a2-122">Specifica il nome del gruppo di risorse che contiene l'istanza di VMSS.</span><span class="sxs-lookup"><span data-stu-id="db5a2-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="db5a2-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="db5a2-123">-VMScaleSetName</span></span>
<span data-ttu-id="db5a2-124">Specifica il nome dell'istanza di VMSS modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5a2-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="db5a2-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db5a2-125">-Confirm</span></span>
<span data-ttu-id="db5a2-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5a2-127">-WhatIf</span></span>
<span data-ttu-id="db5a2-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db5a2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db5a2-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db5a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5a2-130">CommonParameters</span></span>
<span data-ttu-id="db5a2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5a2-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5a2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5a2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db5a2-133">INPUTS</span></span>

### <span data-ttu-id="db5a2-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="db5a2-134">None</span></span>
<span data-ttu-id="db5a2-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="db5a2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db5a2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db5a2-136">OUTPUTS</span></span>

### <span data-ttu-id="db5a2-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="db5a2-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="db5a2-138">Note</span><span class="sxs-lookup"><span data-stu-id="db5a2-138">NOTES</span></span>

## <span data-ttu-id="db5a2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db5a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="db5a2-140">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="db5a2-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
