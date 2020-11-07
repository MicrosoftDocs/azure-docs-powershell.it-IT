---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 00325dc33daa6ec58693dbe6cd6d526ac41b8fd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520266"
---
# <span data-ttu-id="67e1c-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="67e1c-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="67e1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="67e1c-103">Ottiene le proprietà di una macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="67e1c-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67e1c-104">SYNTAX</span></span>

### <span data-ttu-id="67e1c-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67e1c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67e1c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="67e1c-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67e1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="67e1c-108">Il cmdlet **Get-AzureRmVmssVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="67e1c-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="67e1c-109">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="67e1c-110">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="67e1c-111">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="67e1c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67e1c-112">EXAMPLES</span></span>

### <span data-ttu-id="67e1c-113">Esempio 1: ottenere le proprietà di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="67e1c-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="67e1c-114">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="67e1c-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="67e1c-115">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="67e1c-116">Esempio 2: ottenere le proprietà della visualizzazione modello di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="67e1c-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="67e1c-117">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="67e1c-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="67e1c-118">Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione modello.</span><span class="sxs-lookup"><span data-stu-id="67e1c-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="67e1c-119">Esempio 3: ottenere le proprietà della visualizzazione istanza di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="67e1c-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="67e1c-120">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="67e1c-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="67e1c-121">Poiché il comando specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione dell'istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="67e1c-122">Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="67e1c-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="67e1c-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67e1c-123">PARAMETERS</span></span>

### <span data-ttu-id="67e1c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e1c-124">-DefaultProfile</span></span>
<span data-ttu-id="67e1c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67e1c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e1c-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="67e1c-126">-InstanceId</span></span>
<span data-ttu-id="67e1c-127">Specifica l'ID istanza per cui ottenere la visualizzazione modello.</span><span class="sxs-lookup"><span data-stu-id="67e1c-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e1c-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="67e1c-128">-InstanceView</span></span>
<span data-ttu-id="67e1c-129">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67e1c-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="67e1c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e1c-130">-ResourceGroupName</span></span>
<span data-ttu-id="67e1c-131">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="67e1c-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="67e1c-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="67e1c-132">-VMScaleSetName</span></span>
<span data-ttu-id="67e1c-133">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="67e1c-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="67e1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e1c-134">CommonParameters</span></span>
<span data-ttu-id="67e1c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e1c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e1c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67e1c-137">INPUTS</span></span>

### <span data-ttu-id="67e1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="67e1c-138">System.String</span></span>

## <span data-ttu-id="67e1c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67e1c-139">OUTPUTS</span></span>

### <span data-ttu-id="67e1c-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="67e1c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="67e1c-141">Note</span><span class="sxs-lookup"><span data-stu-id="67e1c-141">NOTES</span></span>

## <span data-ttu-id="67e1c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67e1c-142">RELATED LINKS</span></span>

[<span data-ttu-id="67e1c-143">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="67e1c-143">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="67e1c-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="67e1c-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

