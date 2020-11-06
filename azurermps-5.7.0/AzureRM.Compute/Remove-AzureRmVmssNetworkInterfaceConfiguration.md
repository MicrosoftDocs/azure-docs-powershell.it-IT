---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514447"
---
# <span data-ttu-id="09091-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09091-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="09091-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09091-102">SYNOPSIS</span></span>
<span data-ttu-id="09091-103">Rimuove una configurazione di interfaccia di rete da un VMSS.</span><span class="sxs-lookup"><span data-stu-id="09091-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09091-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09091-104">SYNTAX</span></span>

### <span data-ttu-id="09091-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09091-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09091-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09091-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09091-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09091-107">DESCRIPTION</span></span>
<span data-ttu-id="09091-108">Il cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** rimuove una configurazione di interfaccia di rete da un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="09091-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="09091-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09091-109">EXAMPLES</span></span>

### <span data-ttu-id="09091-110">Esempio 1: rimuovere una configurazione di interfaccia</span><span class="sxs-lookup"><span data-stu-id="09091-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="09091-111">Il primo comando ottiene un VMSS usando il cmdlet Get-AzureRmVmss e lo archivia nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09091-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="09091-112">Il secondo comando rimuove la configurazione dell'interfaccia di rete denominata ContosoVmssInterface02 dall'insieme in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09091-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="09091-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09091-113">PARAMETERS</span></span>

### <span data-ttu-id="09091-114">-ID</span><span class="sxs-lookup"><span data-stu-id="09091-114">-Id</span></span>
<span data-ttu-id="09091-115">Specifica l'ID della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09091-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09091-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="09091-116">-Name</span></span>
<span data-ttu-id="09091-117">Specifica il nome della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09091-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09091-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09091-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09091-119">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="09091-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09091-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09091-120">-Confirm</span></span>
<span data-ttu-id="09091-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09091-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09091-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09091-122">-WhatIf</span></span>
<span data-ttu-id="09091-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09091-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09091-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09091-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09091-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09091-125">CommonParameters</span></span>
<span data-ttu-id="09091-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09091-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09091-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09091-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09091-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09091-128">INPUTS</span></span>

### <span data-ttu-id="09091-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09091-129">None</span></span>
<span data-ttu-id="09091-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="09091-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09091-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09091-131">OUTPUTS</span></span>

## <span data-ttu-id="09091-132">Note</span><span class="sxs-lookup"><span data-stu-id="09091-132">NOTES</span></span>

## <span data-ttu-id="09091-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09091-133">RELATED LINKS</span></span>

[<span data-ttu-id="09091-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09091-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="09091-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="09091-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


