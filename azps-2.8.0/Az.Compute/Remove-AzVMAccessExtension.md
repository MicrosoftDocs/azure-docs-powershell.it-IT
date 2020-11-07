---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 1fececa1c7d40e8ea2667ecd6461740a6714d744
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675263"
---
# <span data-ttu-id="b417d-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b417d-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="b417d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b417d-102">SYNOPSIS</span></span>
<span data-ttu-id="b417d-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b417d-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="b417d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b417d-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b417d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b417d-105">DESCRIPTION</span></span>
<span data-ttu-id="b417d-106">Il cmdlet **Remove-AzVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b417d-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b417d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b417d-107">EXAMPLES</span></span>

## <span data-ttu-id="b417d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b417d-108">PARAMETERS</span></span>

### <span data-ttu-id="b417d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b417d-109">-DefaultProfile</span></span>
<span data-ttu-id="b417d-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b417d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b417d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b417d-111">-Force</span></span>
<span data-ttu-id="b417d-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b417d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b417d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b417d-113">-Name</span></span>
<span data-ttu-id="b417d-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b417d-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b417d-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b417d-115">-NoWait</span></span>
<span data-ttu-id="b417d-116">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b417d-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b417d-117">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="b417d-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b417d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b417d-118">-ResourceGroupName</span></span>
<span data-ttu-id="b417d-119">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b417d-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b417d-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="b417d-120">-VMName</span></span>
<span data-ttu-id="b417d-121">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b417d-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b417d-122">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b417d-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b417d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b417d-123">-Confirm</span></span>
<span data-ttu-id="b417d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b417d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b417d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b417d-125">-WhatIf</span></span>
<span data-ttu-id="b417d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b417d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b417d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b417d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b417d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b417d-128">CommonParameters</span></span>
<span data-ttu-id="b417d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b417d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b417d-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b417d-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b417d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b417d-131">INPUTS</span></span>

### <span data-ttu-id="b417d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b417d-132">System.String</span></span>

## <span data-ttu-id="b417d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b417d-133">OUTPUTS</span></span>

### <span data-ttu-id="b417d-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b417d-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b417d-135">Note</span><span class="sxs-lookup"><span data-stu-id="b417d-135">NOTES</span></span>

## <span data-ttu-id="b417d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b417d-136">RELATED LINKS</span></span>

[<span data-ttu-id="b417d-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b417d-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="b417d-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b417d-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="b417d-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b417d-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
