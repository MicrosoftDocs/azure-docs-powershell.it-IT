---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866554"
---
# <span data-ttu-id="a1056-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a1056-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="a1056-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1056-102">SYNOPSIS</span></span>
<span data-ttu-id="a1056-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1056-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1056-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1056-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1056-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1056-105">DESCRIPTION</span></span>
<span data-ttu-id="a1056-106">Il cmdlet **Remove-AzureRmVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1056-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="a1056-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1056-107">EXAMPLES</span></span>

### <span data-ttu-id="a1056-108">1:</span><span class="sxs-lookup"><span data-stu-id="a1056-108">1:</span></span>
```

```

## <span data-ttu-id="a1056-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1056-109">PARAMETERS</span></span>

### <span data-ttu-id="a1056-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1056-110">-DefaultProfile</span></span>
<span data-ttu-id="a1056-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1056-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1056-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="a1056-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="a1056-113">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1056-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1056-114">-VM</span><span class="sxs-lookup"><span data-stu-id="a1056-114">-VM</span></span>
<span data-ttu-id="a1056-115">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a1056-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="a1056-116">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a1056-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="a1056-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1056-117">-Confirm</span></span>
<span data-ttu-id="a1056-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1056-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="a1056-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1056-119">-WhatIf</span></span>
<span data-ttu-id="a1056-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1056-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1056-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1056-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="a1056-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1056-122">CommonParameters</span></span>
<span data-ttu-id="a1056-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1056-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1056-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1056-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1056-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1056-125">INPUTS</span></span>

### <span data-ttu-id="a1056-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a1056-126">PSVirtualMachine</span></span>
<span data-ttu-id="a1056-127">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a1056-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="a1056-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1056-128">OUTPUTS</span></span>

### <span data-ttu-id="a1056-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a1056-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a1056-130">Note</span><span class="sxs-lookup"><span data-stu-id="a1056-130">NOTES</span></span>

## <span data-ttu-id="a1056-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1056-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1056-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a1056-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


