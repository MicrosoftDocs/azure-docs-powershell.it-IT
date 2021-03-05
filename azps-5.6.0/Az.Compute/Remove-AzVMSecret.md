---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985247"
---
# <span data-ttu-id="18754-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="18754-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="18754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18754-102">SYNOPSIS</span></span>
<span data-ttu-id="18754-103">Rimuove (a) uno o più segreti da un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="18754-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="18754-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18754-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18754-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18754-105">DESCRIPTION</span></span>
<span data-ttu-id="18754-106">Il cmdlet Remove-AzVMSecret rimuove (a) segreto/i da un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18754-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="18754-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18754-107">EXAMPLES</span></span>

### <span data-ttu-id="18754-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18754-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="18754-109">Rimuove tutti i segreti da una macchina virtuale "vm1" nel gruppo di risorse "rg1" e aggiorna la macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="18754-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="18754-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18754-110">PARAMETERS</span></span>

### <span data-ttu-id="18754-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18754-111">-DefaultProfile</span></span>
<span data-ttu-id="18754-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18754-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18754-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="18754-113">-SourceVaultId</span></span>
<span data-ttu-id="18754-114">Specifica una matrice di ID vault di origine rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18754-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18754-115">-VM</span><span class="sxs-lookup"><span data-stu-id="18754-115">-VM</span></span>
<span data-ttu-id="18754-116">Specifica la macchina virtuale da cui questo cmdlet rimuove (a) i segreti.</span><span class="sxs-lookup"><span data-stu-id="18754-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="18754-117">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="18754-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18754-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18754-118">-Confirm</span></span>
<span data-ttu-id="18754-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18754-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18754-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18754-120">-WhatIf</span></span>
<span data-ttu-id="18754-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18754-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18754-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18754-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18754-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18754-123">CommonParameters</span></span>
<span data-ttu-id="18754-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18754-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18754-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18754-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18754-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="18754-126">INPUTS</span></span>

### <span data-ttu-id="18754-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18754-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="18754-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18754-128">OUTPUTS</span></span>

### <span data-ttu-id="18754-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18754-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="18754-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="18754-130">NOTES</span></span>

## <span data-ttu-id="18754-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18754-131">RELATED LINKS</span></span>
