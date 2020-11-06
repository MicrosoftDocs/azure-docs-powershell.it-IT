---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 8d24aadd185a58472268fc4edf9ca504e7592bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512708"
---
# <span data-ttu-id="fc69d-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="fc69d-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="fc69d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc69d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc69d-103">Ottiene le proprietà di una macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="fc69d-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc69d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc69d-104">SYNTAX</span></span>

### <span data-ttu-id="fc69d-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc69d-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc69d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fc69d-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

## <span data-ttu-id="fc69d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc69d-107">DESCRIPTION</span></span>
<span data-ttu-id="fc69d-108">Il cmdlet **Get-AzureRmVmssVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="fc69d-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="fc69d-109">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="fc69d-110">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="fc69d-111">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="fc69d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc69d-112">EXAMPLES</span></span>

### <span data-ttu-id="fc69d-113">Esempio 1: ottenere le proprietà di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="fc69d-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fc69d-114">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="fc69d-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="fc69d-115">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="fc69d-116">Esempio 2: ottenere le proprietà della visualizzazione modello di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="fc69d-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="fc69d-117">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="fc69d-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="fc69d-118">Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione modello.</span><span class="sxs-lookup"><span data-stu-id="fc69d-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="fc69d-119">Esempio 3: ottenere le proprietà della visualizzazione istanza di una macchina virtuale VMSS</span><span class="sxs-lookup"><span data-stu-id="fc69d-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="fc69d-120">Questo comando consente di ottenere le proprietà della macchina virtuale VMSS denominata VMSS004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="fc69d-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="fc69d-121">Poiché il comando specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione dell'istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="fc69d-122">Il comando ottiene l'ID istanza archiviato nella variabile $ID per cui ottenere la visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="fc69d-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="fc69d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc69d-123">PARAMETERS</span></span>

### <span data-ttu-id="fc69d-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fc69d-124">-InstanceId</span></span>
<span data-ttu-id="fc69d-125">Specifica l'ID istanza per cui ottenere la visualizzazione modello.</span><span class="sxs-lookup"><span data-stu-id="fc69d-125">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc69d-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="fc69d-126">-InstanceView</span></span>
<span data-ttu-id="fc69d-127">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc69d-127">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc69d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc69d-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc69d-129">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="fc69d-129">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc69d-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fc69d-130">-VMScaleSetName</span></span>
<span data-ttu-id="fc69d-131">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="fc69d-131">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc69d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc69d-132">CommonParameters</span></span>
<span data-ttu-id="fc69d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc69d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc69d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc69d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc69d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc69d-135">INPUTS</span></span>

### <span data-ttu-id="fc69d-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fc69d-136">None</span></span>
<span data-ttu-id="fc69d-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fc69d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc69d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc69d-138">OUTPUTS</span></span>

### <span data-ttu-id="fc69d-139">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fc69d-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fc69d-140">Note</span><span class="sxs-lookup"><span data-stu-id="fc69d-140">NOTES</span></span>

## <span data-ttu-id="fc69d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc69d-141">RELATED LINKS</span></span>

[<span data-ttu-id="fc69d-142">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="fc69d-142">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="fc69d-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc69d-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


