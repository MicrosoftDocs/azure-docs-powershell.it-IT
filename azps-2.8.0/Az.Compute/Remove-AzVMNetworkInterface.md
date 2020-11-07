---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 391f0e6c2c44c409d4d2c02f0be4e243f0929457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675247"
---
# <span data-ttu-id="2b507-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2b507-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="2b507-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b507-102">SYNOPSIS</span></span>
<span data-ttu-id="2b507-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2b507-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="2b507-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b507-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b507-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b507-105">DESCRIPTION</span></span>
<span data-ttu-id="2b507-106">Il cmdlet **Remove-AzVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2b507-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="2b507-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b507-107">EXAMPLES</span></span>

## <span data-ttu-id="2b507-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b507-108">PARAMETERS</span></span>

### <span data-ttu-id="2b507-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b507-109">-DefaultProfile</span></span>
<span data-ttu-id="2b507-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b507-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b507-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="2b507-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="2b507-112">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b507-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b507-113">-VM</span><span class="sxs-lookup"><span data-stu-id="2b507-113">-VM</span></span>
<span data-ttu-id="2b507-114">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2b507-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="2b507-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2b507-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="2b507-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b507-116">-Confirm</span></span>
<span data-ttu-id="2b507-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b507-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b507-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b507-118">-WhatIf</span></span>
<span data-ttu-id="2b507-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b507-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b507-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b507-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b507-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b507-121">CommonParameters</span></span>
<span data-ttu-id="2b507-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b507-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b507-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b507-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b507-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b507-124">INPUTS</span></span>

### <span data-ttu-id="2b507-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2b507-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2b507-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b507-126">OUTPUTS</span></span>

### <span data-ttu-id="2b507-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2b507-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2b507-128">Note</span><span class="sxs-lookup"><span data-stu-id="2b507-128">NOTES</span></span>

## <span data-ttu-id="2b507-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b507-129">RELATED LINKS</span></span>

[<span data-ttu-id="2b507-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b507-130">Get-AzVM</span></span>](./Get-AzVM.md)


