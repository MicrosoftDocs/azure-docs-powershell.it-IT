---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863706"
---
# <span data-ttu-id="19e0d-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-101">Get-AzVmss</span></span>

## <span data-ttu-id="19e0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="19e0d-103">Ottiene le proprietà di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="19e0d-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="19e0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19e0d-104">SYNTAX</span></span>

### <span data-ttu-id="19e0d-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19e0d-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19e0d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="19e0d-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19e0d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="19e0d-108">Il cmdlet **Get-AzVmss** ottiene il modello e la visualizzazione dell'istanza di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="19e0d-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="19e0d-109">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e0d-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="19e0d-110">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e0d-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="19e0d-111">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e0d-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="19e0d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19e0d-112">EXAMPLES</span></span>

### <span data-ttu-id="19e0d-113">Esempio 1: ottenere le proprietà di un VMSS</span><span class="sxs-lookup"><span data-stu-id="19e0d-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="19e0d-114">Questo comando consente di ottenere le proprietà del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="19e0d-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="19e0d-115">Poiché il comando non specifica il parametro *InstanceView* switch, il cmdlet ottiene la visualizzazione modello della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e0d-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="19e0d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19e0d-116">PARAMETERS</span></span>

### <span data-ttu-id="19e0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e0d-117">-DefaultProfile</span></span>
<span data-ttu-id="19e0d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19e0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19e0d-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="19e0d-119">-InstanceView</span></span>
<span data-ttu-id="19e0d-120">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e0d-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="19e0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="19e0d-122">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="19e0d-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="19e0d-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="19e0d-123">-VMScaleSetName</span></span>
<span data-ttu-id="19e0d-124">Specie il nome del VMSS.</span><span class="sxs-lookup"><span data-stu-id="19e0d-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="19e0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e0d-125">CommonParameters</span></span>
<span data-ttu-id="19e0d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e0d-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e0d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e0d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19e0d-128">INPUTS</span></span>

### <span data-ttu-id="19e0d-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19e0d-129">None</span></span>
<span data-ttu-id="19e0d-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="19e0d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19e0d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19e0d-131">OUTPUTS</span></span>

### <span data-ttu-id="19e0d-132">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="19e0d-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="19e0d-133">Note</span><span class="sxs-lookup"><span data-stu-id="19e0d-133">NOTES</span></span>

## <span data-ttu-id="19e0d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19e0d-134">RELATED LINKS</span></span>

[<span data-ttu-id="19e0d-135">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="19e0d-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="19e0d-137">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="19e0d-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="19e0d-139">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="19e0d-140">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="19e0d-141">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="19e0d-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


