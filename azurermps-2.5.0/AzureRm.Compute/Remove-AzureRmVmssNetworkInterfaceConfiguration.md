---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866910"
---
# <span data-ttu-id="d58d1-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d58d1-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d58d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d58d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d58d1-103">Rimuove una configurazione di interfaccia di rete da un VMSS.</span><span class="sxs-lookup"><span data-stu-id="d58d1-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d58d1-104">SYNTAX</span></span>

### <span data-ttu-id="d58d1-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d58d1-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58d1-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d58d1-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d58d1-107">DESCRIPTION</span></span>
<span data-ttu-id="d58d1-108">Il cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** rimuove una configurazione di interfaccia di rete da un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d58d1-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d58d1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d58d1-109">EXAMPLES</span></span>

### <span data-ttu-id="d58d1-110">Esempio 1: rimuovere una configurazione di interfaccia</span><span class="sxs-lookup"><span data-stu-id="d58d1-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="d58d1-111">Il primo comando ottiene un VMSS usando il cmdlet Get-AzureRmVmss e lo archivia nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="d58d1-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="d58d1-112">Il secondo comando rimuove la configurazione dell'interfaccia di rete denominata ContosoVmssInterface02 dall'insieme in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="d58d1-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="d58d1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d58d1-113">PARAMETERS</span></span>

### <span data-ttu-id="d58d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58d1-114">-DefaultProfile</span></span>
<span data-ttu-id="d58d1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d58d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58d1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d58d1-116">-Id</span></span>
<span data-ttu-id="d58d1-117">Specifica l'ID della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58d1-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d58d1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d58d1-118">-Name</span></span>
<span data-ttu-id="d58d1-119">Specifica il nome della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58d1-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d58d1-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d58d1-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d58d1-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d58d1-121">Specifies the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d58d1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d58d1-122">-Confirm</span></span>
<span data-ttu-id="d58d1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58d1-124">-WhatIf</span></span>
<span data-ttu-id="d58d1-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d58d1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d58d1-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d58d1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58d1-127">CommonParameters</span></span>
<span data-ttu-id="d58d1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58d1-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58d1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d58d1-130">INPUTS</span></span>

### <span data-ttu-id="d58d1-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d58d1-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d58d1-132">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d58d1-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d58d1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d58d1-133">OUTPUTS</span></span>

### <span data-ttu-id="d58d1-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d58d1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d58d1-135">Note</span><span class="sxs-lookup"><span data-stu-id="d58d1-135">NOTES</span></span>

## <span data-ttu-id="d58d1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d58d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="d58d1-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d58d1-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="d58d1-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d58d1-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


