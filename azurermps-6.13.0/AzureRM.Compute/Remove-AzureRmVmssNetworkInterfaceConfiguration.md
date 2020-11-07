---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 526e6a471f7bb1149e27464bc8ca1e9b9e9de0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688141"
---
# <span data-ttu-id="2ba26-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ba26-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="2ba26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ba26-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba26-103">Rimuove una configurazione di interfaccia di rete da un VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ba26-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ba26-104">SYNTAX</span></span>

### <span data-ttu-id="2ba26-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba26-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba26-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba26-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ba26-107">DESCRIPTION</span></span>
<span data-ttu-id="2ba26-108">Il cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** rimuove una configurazione di interfaccia di rete da un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2ba26-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2ba26-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ba26-109">EXAMPLES</span></span>

### <span data-ttu-id="2ba26-110">Esempio 1: rimuovere una configurazione di interfaccia</span><span class="sxs-lookup"><span data-stu-id="2ba26-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="2ba26-111">Il primo comando ottiene un VMSS usando il cmdlet Get-AzureRmVmss e lo archivia nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ba26-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="2ba26-112">Il secondo comando rimuove la configurazione dell'interfaccia di rete denominata ContosoVmssInterface02 dall'insieme in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ba26-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="2ba26-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ba26-113">PARAMETERS</span></span>

### <span data-ttu-id="2ba26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba26-114">-DefaultProfile</span></span>
<span data-ttu-id="2ba26-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ba26-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2ba26-116">-Id</span></span>
<span data-ttu-id="2ba26-117">Specifica l'ID della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba26-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba26-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ba26-118">-Name</span></span>
<span data-ttu-id="2ba26-119">Specifica il nome della configurazione dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba26-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba26-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ba26-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2ba26-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="2ba26-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba26-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ba26-122">-Confirm</span></span>
<span data-ttu-id="2ba26-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba26-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba26-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba26-124">-WhatIf</span></span>
<span data-ttu-id="2ba26-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba26-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ba26-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba26-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba26-127">CommonParameters</span></span>
<span data-ttu-id="2ba26-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba26-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba26-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba26-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ba26-130">INPUTS</span></span>

### <span data-ttu-id="2ba26-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ba26-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2ba26-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ba26-132">System.String</span></span>

## <span data-ttu-id="2ba26-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ba26-133">OUTPUTS</span></span>

### <span data-ttu-id="2ba26-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2ba26-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2ba26-135">Note</span><span class="sxs-lookup"><span data-stu-id="2ba26-135">NOTES</span></span>

## <span data-ttu-id="2ba26-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ba26-136">RELATED LINKS</span></span>

[<span data-ttu-id="2ba26-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ba26-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="2ba26-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2ba26-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


