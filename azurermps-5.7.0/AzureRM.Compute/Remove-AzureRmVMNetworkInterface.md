---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508340"
---
# <span data-ttu-id="38186-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="38186-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="38186-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38186-102">SYNOPSIS</span></span>
<span data-ttu-id="38186-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="38186-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38186-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38186-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38186-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38186-105">DESCRIPTION</span></span>
<span data-ttu-id="38186-106">Il cmdlet **Remove-AzureRmVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="38186-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="38186-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38186-107">EXAMPLES</span></span>

## <span data-ttu-id="38186-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38186-108">PARAMETERS</span></span>

### <span data-ttu-id="38186-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="38186-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="38186-110">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38186-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38186-111">-VM</span><span class="sxs-lookup"><span data-stu-id="38186-111">-VM</span></span>
<span data-ttu-id="38186-112">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="38186-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="38186-113">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="38186-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="38186-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38186-114">-Confirm</span></span>
<span data-ttu-id="38186-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38186-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="38186-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38186-116">-WhatIf</span></span>
<span data-ttu-id="38186-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38186-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38186-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38186-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="38186-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38186-119">CommonParameters</span></span>
<span data-ttu-id="38186-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38186-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38186-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38186-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38186-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38186-122">INPUTS</span></span>

### <span data-ttu-id="38186-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="38186-123">None</span></span>
<span data-ttu-id="38186-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="38186-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38186-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38186-125">OUTPUTS</span></span>

## <span data-ttu-id="38186-126">Note</span><span class="sxs-lookup"><span data-stu-id="38186-126">NOTES</span></span>

## <span data-ttu-id="38186-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38186-127">RELATED LINKS</span></span>

[<span data-ttu-id="38186-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38186-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


