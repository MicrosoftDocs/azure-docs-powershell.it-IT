---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675256"
---
# <span data-ttu-id="1f427-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1f427-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="1f427-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f427-102">SYNOPSIS</span></span>
<span data-ttu-id="1f427-103">Rimuove un'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f427-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="1f427-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f427-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f427-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f427-105">DESCRIPTION</span></span>
<span data-ttu-id="1f427-106">Il cmdlet **Remove-AzVMCustomScriptExtension** rimuove un'estensione di una macchina virtuale script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f427-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="1f427-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f427-107">EXAMPLES</span></span>

## <span data-ttu-id="1f427-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f427-108">PARAMETERS</span></span>

### <span data-ttu-id="1f427-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f427-109">-DefaultProfile</span></span>
<span data-ttu-id="1f427-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f427-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f427-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f427-111">-Force</span></span>
<span data-ttu-id="1f427-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f427-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f427-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f427-113">-Name</span></span>
<span data-ttu-id="1f427-114">Specifica il nome dell'estensione di script personalizzata rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f427-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f427-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1f427-115">-NoWait</span></span>
<span data-ttu-id="1f427-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1f427-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1f427-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="1f427-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1f427-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f427-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f427-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f427-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1f427-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="1f427-120">-VMName</span></span>
<span data-ttu-id="1f427-121">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="1f427-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="1f427-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f427-122">-Confirm</span></span>
<span data-ttu-id="1f427-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f427-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f427-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f427-124">-WhatIf</span></span>
<span data-ttu-id="1f427-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f427-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f427-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f427-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f427-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f427-127">CommonParameters</span></span>
<span data-ttu-id="1f427-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f427-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f427-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f427-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f427-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f427-130">INPUTS</span></span>

### <span data-ttu-id="1f427-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1f427-131">System.String</span></span>

## <span data-ttu-id="1f427-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f427-132">OUTPUTS</span></span>

### <span data-ttu-id="1f427-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1f427-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1f427-134">Note</span><span class="sxs-lookup"><span data-stu-id="1f427-134">NOTES</span></span>

## <span data-ttu-id="1f427-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f427-135">RELATED LINKS</span></span>

[<span data-ttu-id="1f427-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1f427-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="1f427-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="1f427-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
