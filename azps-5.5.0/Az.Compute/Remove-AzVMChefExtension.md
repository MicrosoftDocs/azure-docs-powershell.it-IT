---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177566"
---
# <span data-ttu-id="52ee0-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="52ee0-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="52ee0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="52ee0-103">Rimuove l'estensione Die da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52ee0-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="52ee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52ee0-104">SYNTAX</span></span>

### <span data-ttu-id="52ee0-105">Linux</span><span class="sxs-lookup"><span data-stu-id="52ee0-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ee0-106">Windows</span><span class="sxs-lookup"><span data-stu-id="52ee0-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ee0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="52ee0-108">Il cmdlet **Remove-AzVMChefExtension rimuove** l'estensione Disaffezione da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52ee0-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="52ee0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52ee0-109">EXAMPLES</span></span>

### <span data-ttu-id="52ee0-110">Esempio 1: Rimuovere un'estensione di Questo tipo da una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="52ee0-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="52ee0-111">Questo comando rimuove un'estensione da una macchina virtuale basata su Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="52ee0-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="52ee0-112">Esempio 2: Rimuovere un'estensione di Lode da una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="52ee0-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="52ee0-113">Questo comando rimuove un'estensione da una macchina virtuale basata su Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="52ee0-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="52ee0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52ee0-114">PARAMETERS</span></span>

### <span data-ttu-id="52ee0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ee0-115">-DefaultProfile</span></span>
<span data-ttu-id="52ee0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52ee0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ee0-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="52ee0-117">-Linux</span></span>
<span data-ttu-id="52ee0-118">Indica che questo cmdlet è destinato a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="52ee0-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ee0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="52ee0-119">-Name</span></span>
<span data-ttu-id="52ee0-120">Specifica il nome dell'estensione Dif da rimuovere dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ee0-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ee0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="52ee0-121">-NoWait</span></span>
<span data-ttu-id="52ee0-122">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="52ee0-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="52ee0-123">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="52ee0-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="52ee0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ee0-124">-ResourceGroupName</span></span>
<span data-ttu-id="52ee0-125">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52ee0-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="52ee0-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="52ee0-126">-VMName</span></span>
<span data-ttu-id="52ee0-127">Specifica il nome di una macchina virtuale per cui questo cmdlet rimuove l'estensione Estensioni.</span><span class="sxs-lookup"><span data-stu-id="52ee0-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="52ee0-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="52ee0-128">-Windows</span></span>
<span data-ttu-id="52ee0-129">Indica che questo cmdlet è destinato a una macchina virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="52ee0-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ee0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52ee0-130">-Confirm</span></span>
<span data-ttu-id="52ee0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ee0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ee0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ee0-132">-WhatIf</span></span>
<span data-ttu-id="52ee0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52ee0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ee0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52ee0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ee0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ee0-135">CommonParameters</span></span>
<span data-ttu-id="52ee0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ee0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ee0-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52ee0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ee0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="52ee0-138">INPUTS</span></span>

### <span data-ttu-id="52ee0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="52ee0-139">System.String</span></span>

## <span data-ttu-id="52ee0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52ee0-140">OUTPUTS</span></span>

### <span data-ttu-id="52ee0-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="52ee0-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="52ee0-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="52ee0-142">NOTES</span></span>

## <span data-ttu-id="52ee0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52ee0-143">RELATED LINKS</span></span>

[<span data-ttu-id="52ee0-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="52ee0-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="52ee0-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="52ee0-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
