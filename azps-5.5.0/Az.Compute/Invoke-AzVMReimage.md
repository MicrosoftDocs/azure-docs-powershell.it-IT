---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177710"
---
# <span data-ttu-id="a48ca-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a48ca-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="a48ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a48ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a48ca-103">Eseguire di nuovo l'immagine di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a48ca-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="a48ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a48ca-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a48ca-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a48ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a48ca-106">Il cmdlet **Invoke-AzVMReimage** ricrea un'immagine di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a48ca-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="a48ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a48ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a48ca-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a48ca-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a48ca-109">Questo comando mostra nuovamente la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a48ca-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="a48ca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a48ca-110">PARAMETERS</span></span>

### <span data-ttu-id="a48ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a48ca-111">-AsJob</span></span>
<span data-ttu-id="a48ca-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a48ca-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a48ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48ca-113">-DefaultProfile</span></span>
<span data-ttu-id="a48ca-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a48ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="a48ca-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a48ca-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48ca-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="a48ca-117">-TempDisk</span></span>
<span data-ttu-id="a48ca-118">Specifica se visualizzare nuovamente il disco temporaneo.</span><span class="sxs-lookup"><span data-stu-id="a48ca-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="a48ca-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a48ca-119">-VMName</span></span>
<span data-ttu-id="a48ca-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a48ca-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48ca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a48ca-121">-Confirm</span></span>
<span data-ttu-id="a48ca-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a48ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a48ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a48ca-123">-WhatIf</span></span>
<span data-ttu-id="a48ca-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a48ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a48ca-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a48ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a48ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48ca-126">CommonParameters</span></span>
<span data-ttu-id="a48ca-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a48ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48ca-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a48ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48ca-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a48ca-129">INPUTS</span></span>

### <span data-ttu-id="a48ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a48ca-130">System.String</span></span>

## <span data-ttu-id="a48ca-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a48ca-131">OUTPUTS</span></span>

### <span data-ttu-id="a48ca-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a48ca-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a48ca-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a48ca-133">NOTES</span></span>

## <span data-ttu-id="a48ca-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a48ca-134">RELATED LINKS</span></span>
