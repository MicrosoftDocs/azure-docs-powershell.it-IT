---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863789"
---
# <span data-ttu-id="ad52e-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-101">Get-AzVM</span></span>

## <span data-ttu-id="ad52e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad52e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad52e-103">Ottiene le proprietà di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="ad52e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad52e-104">SYNTAX</span></span>

### <span data-ttu-id="ad52e-105">ListAllVirtualMachinesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad52e-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad52e-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ad52e-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad52e-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ad52e-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad52e-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="ad52e-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad52e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad52e-109">DESCRIPTION</span></span>
<span data-ttu-id="ad52e-110">Il cmdlet **Get-AzVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad52e-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="ad52e-111">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="ad52e-112">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="ad52e-113">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="ad52e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad52e-114">EXAMPLES</span></span>

### <span data-ttu-id="ad52e-115">Esempio 1: ottenere le proprietà di visualizzazione modello e istanza</span><span class="sxs-lookup"><span data-stu-id="ad52e-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ad52e-116">Questo comando consente di ottenere le proprietà visualizzazione modello e visualizzazione istanza della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ad52e-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="ad52e-117">Esempio 2: ottenere le proprietà della visualizzazione istanza</span><span class="sxs-lookup"><span data-stu-id="ad52e-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="ad52e-118">Questo comando consente di ottenere le proprietà della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ad52e-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ad52e-119">Questo comando specifica il parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="ad52e-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="ad52e-120">Il comando ottiene pertanto solo le proprietà della visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="ad52e-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="ad52e-121">Esempio 3: ottenere le proprietà per tutte le macchine virtuali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ad52e-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ad52e-122">Questo comando consente di ottenere le proprietà per tutte le macchine virtuali nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad52e-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ad52e-123">Esempio 4: ottenere tutte le macchine virtuali nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="ad52e-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="ad52e-124">Questo comando consente di ottenere tutte le macchine virtuali nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ad52e-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="ad52e-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad52e-125">PARAMETERS</span></span>

### <span data-ttu-id="ad52e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad52e-126">-DefaultProfile</span></span>
<span data-ttu-id="ad52e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad52e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad52e-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="ad52e-128">-DisplayHint</span></span>
<span data-ttu-id="ad52e-129">Determina il modo in cui viene visualizzato l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="ad52e-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ad52e-130">Valid values are:</span></span>

<span data-ttu-id="ad52e-131">--Compatta: Visualizza solo le proprietà di primo livello</span><span class="sxs-lookup"><span data-stu-id="ad52e-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="ad52e-132">--Expand: Visualizza tutte le proprietà in tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="ad52e-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="ad52e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad52e-133">-Name</span></span>
<span data-ttu-id="ad52e-134">Specifica il nome della macchina virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ad52e-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="ad52e-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ad52e-135">-NextLink</span></span>
<span data-ttu-id="ad52e-136">Specifica il collegamento successivo.</span><span class="sxs-lookup"><span data-stu-id="ad52e-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="ad52e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad52e-137">-ResourceGroupName</span></span>
<span data-ttu-id="ad52e-138">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad52e-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad52e-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="ad52e-139">-Status</span></span>
<span data-ttu-id="ad52e-140">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad52e-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="ad52e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad52e-141">CommonParameters</span></span>
<span data-ttu-id="ad52e-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad52e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad52e-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad52e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad52e-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad52e-144">INPUTS</span></span>

### <span data-ttu-id="ad52e-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad52e-145">None</span></span>
<span data-ttu-id="ad52e-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ad52e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad52e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad52e-147">OUTPUTS</span></span>

### <span data-ttu-id="ad52e-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ad52e-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ad52e-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="ad52e-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="ad52e-150">Note</span><span class="sxs-lookup"><span data-stu-id="ad52e-150">NOTES</span></span>

## <span data-ttu-id="ad52e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad52e-151">RELATED LINKS</span></span>

[<span data-ttu-id="ad52e-152">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ad52e-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="ad52e-154">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="ad52e-155">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ad52e-156">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ad52e-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad52e-157">Update-AzVM</span></span>](./Update-AzVM.md)


