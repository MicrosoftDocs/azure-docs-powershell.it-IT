---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687358"
---
# <span data-ttu-id="47dd7-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="47dd7-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="47dd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="47dd7-103">Rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47dd7-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47dd7-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dd7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="47dd7-106">Il cmdlet **Remove-AzureRmVMNetworkInterface** rimuove un'interfaccia di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47dd7-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="47dd7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47dd7-107">EXAMPLES</span></span>

## <span data-ttu-id="47dd7-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47dd7-108">PARAMETERS</span></span>

### <span data-ttu-id="47dd7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dd7-109">-DefaultProfile</span></span>
<span data-ttu-id="47dd7-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47dd7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dd7-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="47dd7-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="47dd7-112">Specifica una matrice di ID interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47dd7-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="47dd7-113">-VM</span><span class="sxs-lookup"><span data-stu-id="47dd7-113">-VM</span></span>
<span data-ttu-id="47dd7-114">Specifica la macchina virtuale da cui questo cmdlet rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="47dd7-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="47dd7-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="47dd7-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="47dd7-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47dd7-116">-Confirm</span></span>
<span data-ttu-id="47dd7-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47dd7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47dd7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dd7-118">-WhatIf</span></span>
<span data-ttu-id="47dd7-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47dd7-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47dd7-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47dd7-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47dd7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dd7-121">CommonParameters</span></span>
<span data-ttu-id="47dd7-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dd7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dd7-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47dd7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dd7-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47dd7-124">INPUTS</span></span>

### <span data-ttu-id="47dd7-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47dd7-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="47dd7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47dd7-126">OUTPUTS</span></span>

### <span data-ttu-id="47dd7-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47dd7-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="47dd7-128">Note</span><span class="sxs-lookup"><span data-stu-id="47dd7-128">NOTES</span></span>

## <span data-ttu-id="47dd7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47dd7-129">RELATED LINKS</span></span>

[<span data-ttu-id="47dd7-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47dd7-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


