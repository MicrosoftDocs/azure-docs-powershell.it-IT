---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 6c02a8381ca1cda4fec6fb52ea3d798884b45bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020070"
---
# <span data-ttu-id="ccbcd-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ccbcd-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="ccbcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbcd-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="ccbcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccbcd-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbcd-106">Il cmdlet **Remove-AzVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="ccbcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-107">EXAMPLES</span></span>

## <span data-ttu-id="ccbcd-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-108">PARAMETERS</span></span>

### <span data-ttu-id="ccbcd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbcd-109">-DefaultProfile</span></span>
<span data-ttu-id="ccbcd-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccbcd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ccbcd-111">-Force</span></span>
<span data-ttu-id="ccbcd-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccbcd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccbcd-113">-Name</span></span>
<span data-ttu-id="ccbcd-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ccbcd-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ccbcd-115">-NoWait</span></span>
<span data-ttu-id="ccbcd-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ccbcd-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ccbcd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-118">-ResourceGroupName</span></span>
<span data-ttu-id="ccbcd-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ccbcd-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-120">-VMName</span></span>
<span data-ttu-id="ccbcd-121">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ccbcd-122">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ccbcd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccbcd-123">-Confirm</span></span>
<span data-ttu-id="ccbcd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbcd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbcd-125">-WhatIf</span></span>
<span data-ttu-id="ccbcd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbcd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbcd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbcd-128">CommonParameters</span></span>
<span data-ttu-id="ccbcd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbcd-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccbcd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbcd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-131">INPUTS</span></span>

### <span data-ttu-id="ccbcd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ccbcd-132">System.String</span></span>

## <span data-ttu-id="ccbcd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccbcd-133">OUTPUTS</span></span>

### <span data-ttu-id="ccbcd-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ccbcd-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ccbcd-135">Note</span><span class="sxs-lookup"><span data-stu-id="ccbcd-135">NOTES</span></span>

## <span data-ttu-id="ccbcd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-136">RELATED LINKS</span></span>

[<span data-ttu-id="ccbcd-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ccbcd-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="ccbcd-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ccbcd-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="ccbcd-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ccbcd-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
