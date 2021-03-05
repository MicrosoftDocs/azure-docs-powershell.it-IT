---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 96560f393c361996ad906d1207647ba53f53cbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001742"
---
# <span data-ttu-id="46a87-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="46a87-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="46a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a87-102">SYNOPSIS</span></span>
<span data-ttu-id="46a87-103">Eseguire di nuovo l'immagine di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="46a87-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="46a87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46a87-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a87-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46a87-105">DESCRIPTION</span></span>
<span data-ttu-id="46a87-106">Il cmdlet **Invoke-AzVMReimage** ricrea un'immagine di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="46a87-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="46a87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46a87-107">EXAMPLES</span></span>

### <span data-ttu-id="46a87-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46a87-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="46a87-109">Questo comando mostra nuovamente la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="46a87-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="46a87-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a87-110">PARAMETERS</span></span>

### <span data-ttu-id="46a87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46a87-111">-AsJob</span></span>
<span data-ttu-id="46a87-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="46a87-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46a87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a87-113">-DefaultProfile</span></span>
<span data-ttu-id="46a87-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46a87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a87-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a87-115">-ResourceGroupName</span></span>
<span data-ttu-id="46a87-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="46a87-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="46a87-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="46a87-117">-TempDisk</span></span>
<span data-ttu-id="46a87-118">Specifica se visualizzare nuovamente il disco temporaneo.</span><span class="sxs-lookup"><span data-stu-id="46a87-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="46a87-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="46a87-119">-VMName</span></span>
<span data-ttu-id="46a87-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="46a87-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="46a87-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46a87-121">-Confirm</span></span>
<span data-ttu-id="46a87-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46a87-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a87-123">-WhatIf</span></span>
<span data-ttu-id="46a87-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46a87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a87-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46a87-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a87-126">CommonParameters</span></span>
<span data-ttu-id="46a87-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a87-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46a87-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a87-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="46a87-129">INPUTS</span></span>

### <span data-ttu-id="46a87-130">System.String</span><span class="sxs-lookup"><span data-stu-id="46a87-130">System.String</span></span>

## <span data-ttu-id="46a87-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46a87-131">OUTPUTS</span></span>

### <span data-ttu-id="46a87-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="46a87-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="46a87-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="46a87-133">NOTES</span></span>

## <span data-ttu-id="46a87-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46a87-134">RELATED LINKS</span></span>
