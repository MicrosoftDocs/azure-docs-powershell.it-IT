---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: f99f5742e9719ca9761313cd40d2c996d4e23be9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863485"
---
# <span data-ttu-id="09990-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09990-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="09990-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09990-102">SYNOPSIS</span></span>
<span data-ttu-id="09990-103">Rimuove una configurazione di interfaccia di rete da un VMSS.</span><span class="sxs-lookup"><span data-stu-id="09990-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="09990-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09990-104">SYNTAX</span></span>

### <span data-ttu-id="09990-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09990-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09990-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09990-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09990-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09990-107">DESCRIPTION</span></span>
<span data-ttu-id="09990-108">Il cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** rimuove una configurazione di interfaccia di rete da un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="09990-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="09990-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09990-109">EXAMPLES</span></span>

### <span data-ttu-id="09990-110">Esempio 1: rimuovere una configurazione di interfaccia</span><span class="sxs-lookup"><span data-stu-id="09990-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="09990-111">Il primo comando ottiene un VMSS usando il cmdlet Get-AzVmss e lo archivia nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09990-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="09990-112">Il secondo comando rimuove la configurazione dell'interfaccia di rete denominata ContosoVmssInterface02 dall'insieme in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="09990-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="09990-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09990-113">PARAMETERS</span></span>

### <span data-ttu-id="09990-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09990-114">-DefaultProfile</span></span>
<span data-ttu-id="09990-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09990-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09990-116">-ID</span><span class="sxs-lookup"><span data-stu-id="09990-116">-Id</span></span>
<span data-ttu-id="09990-117">Specifica l'ID della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09990-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09990-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="09990-118">-Name</span></span>
<span data-ttu-id="09990-119">Specifica il nome della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09990-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09990-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09990-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="09990-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="09990-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="09990-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09990-122">-Confirm</span></span>
<span data-ttu-id="09990-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09990-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09990-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09990-124">-WhatIf</span></span>
<span data-ttu-id="09990-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09990-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09990-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09990-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09990-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09990-127">CommonParameters</span></span>
<span data-ttu-id="09990-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09990-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09990-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09990-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09990-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09990-130">INPUTS</span></span>

### <span data-ttu-id="09990-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09990-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="09990-132">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="09990-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="09990-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09990-133">OUTPUTS</span></span>

### <span data-ttu-id="09990-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="09990-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="09990-135">Note</span><span class="sxs-lookup"><span data-stu-id="09990-135">NOTES</span></span>

## <span data-ttu-id="09990-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09990-136">RELATED LINKS</span></span>

[<span data-ttu-id="09990-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09990-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="09990-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="09990-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


