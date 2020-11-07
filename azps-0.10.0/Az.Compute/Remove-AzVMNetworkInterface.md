---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863517"
---
# <span data-ttu-id="85604-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85604-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="85604-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85604-102">SYNOPSIS</span></span>
<span data-ttu-id="85604-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85604-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="85604-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85604-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85604-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85604-105">DESCRIPTION</span></span>
<span data-ttu-id="85604-106">Il cmdlet **Remove-AzVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85604-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="85604-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85604-107">EXAMPLES</span></span>

### <span data-ttu-id="85604-108">1:</span><span class="sxs-lookup"><span data-stu-id="85604-108">1:</span></span>
```

```

## <span data-ttu-id="85604-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85604-109">PARAMETERS</span></span>

### <span data-ttu-id="85604-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85604-110">-DefaultProfile</span></span>
<span data-ttu-id="85604-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85604-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85604-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="85604-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="85604-113">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85604-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85604-114">-VM</span><span class="sxs-lookup"><span data-stu-id="85604-114">-VM</span></span>
<span data-ttu-id="85604-115">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="85604-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="85604-116">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="85604-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85604-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85604-117">-Confirm</span></span>
<span data-ttu-id="85604-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85604-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85604-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85604-119">-WhatIf</span></span>
<span data-ttu-id="85604-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85604-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85604-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85604-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85604-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85604-122">CommonParameters</span></span>
<span data-ttu-id="85604-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85604-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85604-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85604-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85604-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85604-125">INPUTS</span></span>

### <span data-ttu-id="85604-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85604-126">PSVirtualMachine</span></span>
<span data-ttu-id="85604-127">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="85604-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="85604-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85604-128">OUTPUTS</span></span>

### <span data-ttu-id="85604-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="85604-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="85604-130">Note</span><span class="sxs-lookup"><span data-stu-id="85604-130">NOTES</span></span>

## <span data-ttu-id="85604-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85604-131">RELATED LINKS</span></span>

[<span data-ttu-id="85604-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="85604-132">Get-AzVM</span></span>](./Get-AzVM.md)


