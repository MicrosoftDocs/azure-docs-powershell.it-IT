---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 0006bab846eb70356bdddc2289f87a62a624e806
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675360"
---
# <span data-ttu-id="0fe34-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0fe34-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="0fe34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fe34-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe34-103">Riimmagine di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe34-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="0fe34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fe34-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fe34-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe34-106">Il cmdlet **Invoke-AzVMReimage** riimmagini una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe34-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="0fe34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fe34-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe34-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fe34-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0fe34-109">Questo comando riimmaginerà la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0fe34-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0fe34-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fe34-110">PARAMETERS</span></span>

### <span data-ttu-id="0fe34-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fe34-111">-AsJob</span></span>
<span data-ttu-id="0fe34-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0fe34-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fe34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe34-113">-DefaultProfile</span></span>
<span data-ttu-id="0fe34-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe34-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe34-115">-ResourceGroupName</span></span>
<span data-ttu-id="0fe34-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fe34-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0fe34-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="0fe34-117">-TempDisk</span></span>
<span data-ttu-id="0fe34-118">Specifica se riimmagine del disco Temp.</span><span class="sxs-lookup"><span data-stu-id="0fe34-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="0fe34-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="0fe34-119">-VMName</span></span>
<span data-ttu-id="0fe34-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0fe34-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="0fe34-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fe34-121">-Confirm</span></span>
<span data-ttu-id="0fe34-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe34-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe34-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe34-123">-WhatIf</span></span>
<span data-ttu-id="0fe34-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fe34-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe34-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fe34-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe34-126">CommonParameters</span></span>
<span data-ttu-id="0fe34-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe34-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fe34-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe34-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fe34-129">INPUTS</span></span>

### <span data-ttu-id="0fe34-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe34-130">System.String</span></span>

## <span data-ttu-id="0fe34-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fe34-131">OUTPUTS</span></span>

### <span data-ttu-id="0fe34-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0fe34-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0fe34-133">Note</span><span class="sxs-lookup"><span data-stu-id="0fe34-133">NOTES</span></span>

## <span data-ttu-id="0fe34-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fe34-134">RELATED LINKS</span></span>
