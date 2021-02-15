---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177542"
---
# <span data-ttu-id="52f18-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="52f18-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="52f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f18-102">SYNOPSIS</span></span>
<span data-ttu-id="52f18-103">Rimuove un'estensione da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52f18-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="52f18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52f18-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f18-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52f18-105">DESCRIPTION</span></span>
<span data-ttu-id="52f18-106">Il cmdlet **Remove-AzVMExtension** rimuove un'estensione dalle estensioni delle macchine virtuali di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52f18-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="52f18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52f18-107">EXAMPLES</span></span>

### <span data-ttu-id="52f18-108">Esempio 1: Rimuovere un'estensione da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="52f18-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="52f18-109">Questo comando rimuove l'estensione denominata ContosoTest dalla macchina virtuale denominata VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="52f18-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="52f18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52f18-110">PARAMETERS</span></span>

### <span data-ttu-id="52f18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f18-111">-DefaultProfile</span></span>
<span data-ttu-id="52f18-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52f18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f18-113">-Force</span><span class="sxs-lookup"><span data-stu-id="52f18-113">-Force</span></span>
<span data-ttu-id="52f18-114">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="52f18-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52f18-115">-Name</span><span class="sxs-lookup"><span data-stu-id="52f18-115">-Name</span></span>
<span data-ttu-id="52f18-116">Specifica il nome dell'estensione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f18-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f18-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f18-117">-ResourceGroupName</span></span>
<span data-ttu-id="52f18-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52f18-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="52f18-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="52f18-119">-VMName</span></span>
<span data-ttu-id="52f18-120">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione.</span><span class="sxs-lookup"><span data-stu-id="52f18-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f18-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52f18-121">-Confirm</span></span>
<span data-ttu-id="52f18-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f18-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f18-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f18-123">-WhatIf</span></span>
<span data-ttu-id="52f18-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f18-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f18-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f18-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f18-126">CommonParameters</span></span>
<span data-ttu-id="52f18-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f18-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52f18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f18-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="52f18-129">INPUTS</span></span>

### <span data-ttu-id="52f18-130">System.String</span><span class="sxs-lookup"><span data-stu-id="52f18-130">System.String</span></span>

## <span data-ttu-id="52f18-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52f18-131">OUTPUTS</span></span>

### <span data-ttu-id="52f18-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="52f18-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="52f18-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="52f18-133">NOTES</span></span>

## <span data-ttu-id="52f18-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52f18-134">RELATED LINKS</span></span>

[<span data-ttu-id="52f18-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="52f18-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="52f18-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="52f18-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


