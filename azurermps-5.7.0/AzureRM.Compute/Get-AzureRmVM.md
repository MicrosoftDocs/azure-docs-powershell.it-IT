---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516884"
---
# <span data-ttu-id="b1452-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="b1452-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1452-102">SYNOPSIS</span></span>
<span data-ttu-id="b1452-103">Ottiene le proprietà di una macchina virtuale di Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="b1452-103">Gets the properties of an Azure Resource Manager (ARM) virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1452-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1452-104">SYNTAX</span></span>

### <span data-ttu-id="b1452-105">ListAllVirtualMachinesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1452-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1452-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b1452-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1452-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b1452-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1452-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="b1452-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1452-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1452-109">DESCRIPTION</span></span>
<span data-ttu-id="b1452-110">Il cmdlet **Get-AzureRmVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1452-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="b1452-111">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1452-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="b1452-112">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1452-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="b1452-113">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1452-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="b1452-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1452-114">EXAMPLES</span></span>

### <span data-ttu-id="b1452-115">Esempio 1: ottenere le proprietà di visualizzazione modello e istanza</span><span class="sxs-lookup"><span data-stu-id="b1452-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b1452-116">Questo comando consente di ottenere le proprietà visualizzazione modello e visualizzazione istanza della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="b1452-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b1452-117">Esempio 2: ottenere le proprietà della visualizzazione istanza</span><span class="sxs-lookup"><span data-stu-id="b1452-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="b1452-118">Questo comando consente di ottenere le proprietà della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="b1452-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="b1452-119">Questo comando specifica il parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="b1452-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="b1452-120">Il comando ottiene pertanto solo le proprietà della visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="b1452-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="b1452-121">Esempio 3: ottenere le proprietà per tutte le macchine virtuali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b1452-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b1452-122">Questo comando consente di ottenere le proprietà per tutte le macchine virtuali nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b1452-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b1452-123">Esempio 4: ottenere tutte le macchine virtuali nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="b1452-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="b1452-124">Questo comando consente di ottenere tutte le macchine virtuali nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b1452-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="b1452-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1452-125">PARAMETERS</span></span>

### <span data-ttu-id="b1452-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1452-126">-DefaultProfile</span></span>
<span data-ttu-id="b1452-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1452-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1452-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="b1452-128">-DisplayHint</span></span>
<span data-ttu-id="b1452-129">Determina il modo in cui viene visualizzato l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1452-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="b1452-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b1452-130">Valid values are:</span></span>

<span data-ttu-id="b1452-131">--Compatta: Visualizza solo le proprietà di primo livello</span><span class="sxs-lookup"><span data-stu-id="b1452-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="b1452-132">--Expand: Visualizza tutte le proprietà in tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="b1452-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1452-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1452-133">-Name</span></span>
<span data-ttu-id="b1452-134">Specifica il nome della macchina virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b1452-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1452-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="b1452-135">-NextLink</span></span>
<span data-ttu-id="b1452-136">Specifica il collegamento successivo.</span><span class="sxs-lookup"><span data-stu-id="b1452-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1452-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1452-137">-ResourceGroupName</span></span>
<span data-ttu-id="b1452-138">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1452-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1452-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="b1452-139">-Status</span></span>
<span data-ttu-id="b1452-140">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1452-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1452-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1452-141">CommonParameters</span></span>
<span data-ttu-id="b1452-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1452-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1452-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1452-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1452-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1452-144">INPUTS</span></span>

### <span data-ttu-id="b1452-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1452-145">None</span></span>
<span data-ttu-id="b1452-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b1452-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1452-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1452-147">OUTPUTS</span></span>

### <span data-ttu-id="b1452-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1452-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b1452-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="b1452-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="b1452-150">Note</span><span class="sxs-lookup"><span data-stu-id="b1452-150">NOTES</span></span>

## <span data-ttu-id="b1452-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1452-151">RELATED LINKS</span></span>

[<span data-ttu-id="b1452-152">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b1452-153">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b1452-154">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b1452-155">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b1452-156">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b1452-157">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1452-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


