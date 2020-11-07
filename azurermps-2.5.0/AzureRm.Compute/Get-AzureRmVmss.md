---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866573"
---
# <span data-ttu-id="16ea0-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="16ea0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="16ea0-103">Ottiene le proprietà di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ea0-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ea0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16ea0-104">SYNTAX</span></span>

### <span data-ttu-id="16ea0-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16ea0-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16ea0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="16ea0-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ea0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ea0-107">DESCRIPTION</span></span>
<span data-ttu-id="16ea0-108">Il cmdlet **Get-AzureRmVmss** ottiene il modello e la visualizzazione dell'istanza di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="16ea0-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="16ea0-109">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="16ea0-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="16ea0-110">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="16ea0-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="16ea0-111">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="16ea0-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="16ea0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16ea0-112">EXAMPLES</span></span>

### <span data-ttu-id="16ea0-113">Esempio 1: ottenere le proprietà di un VMSS</span><span class="sxs-lookup"><span data-stu-id="16ea0-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="16ea0-114">Questo comando consente di ottenere le proprietà del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="16ea0-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="16ea0-115">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="16ea0-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="16ea0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16ea0-116">PARAMETERS</span></span>

### <span data-ttu-id="16ea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ea0-117">-DefaultProfile</span></span>
<span data-ttu-id="16ea0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16ea0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ea0-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="16ea0-119">-InstanceView</span></span>
<span data-ttu-id="16ea0-120">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="16ea0-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ea0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ea0-121">-ResourceGroupName</span></span>
<span data-ttu-id="16ea0-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ea0-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="16ea0-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="16ea0-123">-VMScaleSetName</span></span>
<span data-ttu-id="16ea0-124">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="16ea0-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="16ea0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ea0-125">CommonParameters</span></span>
<span data-ttu-id="16ea0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ea0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ea0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ea0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ea0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16ea0-128">INPUTS</span></span>

### <span data-ttu-id="16ea0-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16ea0-129">None</span></span>
<span data-ttu-id="16ea0-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="16ea0-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16ea0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16ea0-131">OUTPUTS</span></span>

### <span data-ttu-id="16ea0-132">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="16ea0-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="16ea0-133">Note</span><span class="sxs-lookup"><span data-stu-id="16ea0-133">NOTES</span></span>

## <span data-ttu-id="16ea0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16ea0-134">RELATED LINKS</span></span>

[<span data-ttu-id="16ea0-135">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="16ea0-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="16ea0-137">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="16ea0-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="16ea0-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="16ea0-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="16ea0-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="16ea0-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


