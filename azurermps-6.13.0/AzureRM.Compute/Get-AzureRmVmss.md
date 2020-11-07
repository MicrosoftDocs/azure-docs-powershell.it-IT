---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687369"
---
# <span data-ttu-id="ccf78-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="ccf78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccf78-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf78-103">Ottiene le proprietà di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="ccf78-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccf78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccf78-104">SYNTAX</span></span>

### <span data-ttu-id="ccf78-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccf78-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccf78-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ccf78-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccf78-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="ccf78-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf78-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf78-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf78-109">Il cmdlet **Get-AzureRmVmss** ottiene il modello e la visualizzazione dell'istanza di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ccf78-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ccf78-110">La visualizzazione modello rappresenta le proprietà specificate dall'utente del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="ccf78-111">La visualizzazione istanza è lo stato del livello di istanza del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="ccf78-112">Specifica il parametro *InstanceView* per ottenere solo la visualizzazione istanza di un set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="ccf78-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccf78-113">EXAMPLES</span></span>

### <span data-ttu-id="ccf78-114">Esempio 1: ottenere le proprietà di un VMSS</span><span class="sxs-lookup"><span data-stu-id="ccf78-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ccf78-115">Questo comando consente di ottenere le proprietà del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="ccf78-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="ccf78-116">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="ccf78-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccf78-117">PARAMETERS</span></span>

### <span data-ttu-id="ccf78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf78-118">-DefaultProfile</span></span>
<span data-ttu-id="ccf78-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf78-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf78-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="ccf78-120">-InstanceView</span></span>
<span data-ttu-id="ccf78-121">Indica che questo cmdlet ottiene solo la visualizzazione istanza del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf78-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="ccf78-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="ccf78-123">Indica che questo cmdlet elenca la cronologia di aggiornamento del sistema operativo del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccf78-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf78-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccf78-125">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="ccf78-125">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf78-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ccf78-126">-VMScaleSetName</span></span>
<span data-ttu-id="ccf78-127">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="ccf78-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf78-128">CommonParameters</span></span>
<span data-ttu-id="ccf78-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf78-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf78-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf78-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccf78-131">INPUTS</span></span>

### <span data-ttu-id="ccf78-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ccf78-132">System.String</span></span>

## <span data-ttu-id="ccf78-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccf78-133">OUTPUTS</span></span>

### <span data-ttu-id="ccf78-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ccf78-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ccf78-135">Note</span><span class="sxs-lookup"><span data-stu-id="ccf78-135">NOTES</span></span>

## <span data-ttu-id="ccf78-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccf78-136">RELATED LINKS</span></span>

[<span data-ttu-id="ccf78-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ccf78-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ccf78-139">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ccf78-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ccf78-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ccf78-142">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ccf78-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccf78-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


