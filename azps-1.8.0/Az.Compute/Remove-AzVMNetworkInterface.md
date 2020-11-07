---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: d5aba3e8810ef06e81b62803cb6b71dd8de619ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684739"
---
# <span data-ttu-id="e6320-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6320-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="e6320-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6320-102">SYNOPSIS</span></span>
<span data-ttu-id="e6320-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6320-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="e6320-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6320-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6320-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6320-105">DESCRIPTION</span></span>
<span data-ttu-id="e6320-106">Il cmdlet **Remove-AzVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6320-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="e6320-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6320-107">EXAMPLES</span></span>

## <span data-ttu-id="e6320-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6320-108">PARAMETERS</span></span>

### <span data-ttu-id="e6320-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6320-109">-DefaultProfile</span></span>
<span data-ttu-id="e6320-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6320-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6320-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="e6320-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="e6320-112">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6320-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6320-113">-VM</span><span class="sxs-lookup"><span data-stu-id="e6320-113">-VM</span></span>
<span data-ttu-id="e6320-114">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="e6320-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="e6320-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e6320-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="e6320-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6320-116">-Confirm</span></span>
<span data-ttu-id="e6320-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6320-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6320-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6320-118">-WhatIf</span></span>
<span data-ttu-id="e6320-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6320-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6320-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6320-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6320-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6320-121">CommonParameters</span></span>
<span data-ttu-id="e6320-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6320-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6320-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6320-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6320-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6320-124">INPUTS</span></span>

### <span data-ttu-id="e6320-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6320-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e6320-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6320-126">OUTPUTS</span></span>

### <span data-ttu-id="e6320-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6320-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e6320-128">Note</span><span class="sxs-lookup"><span data-stu-id="e6320-128">NOTES</span></span>

## <span data-ttu-id="e6320-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6320-129">RELATED LINKS</span></span>

[<span data-ttu-id="e6320-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e6320-130">Get-AzVM</span></span>](./Get-AzVM.md)


