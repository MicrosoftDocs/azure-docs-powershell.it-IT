---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511864"
---
# <span data-ttu-id="c5034-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="c5034-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5034-102">SYNOPSIS</span></span>
<span data-ttu-id="c5034-103">Ottiene le proprietà di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5034-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5034-104">SYNTAX</span></span>

### <span data-ttu-id="c5034-105">ListAllVirtualMachinesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5034-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5034-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="c5034-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5034-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="c5034-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5034-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="c5034-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5034-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="c5034-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5034-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5034-110">DESCRIPTION</span></span>
<span data-ttu-id="c5034-111">Il cmdlet **Get-AzureRmVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5034-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="c5034-112">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="c5034-113">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="c5034-114">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="c5034-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5034-115">EXAMPLES</span></span>

### <span data-ttu-id="c5034-116">Esempio 1: ottenere le proprietà di visualizzazione modello e istanza</span><span class="sxs-lookup"><span data-stu-id="c5034-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="c5034-117">Questo comando consente di ottenere le proprietà visualizzazione modello e visualizzazione istanza della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="c5034-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="c5034-118">Esempio 2: ottenere le proprietà della visualizzazione istanza</span><span class="sxs-lookup"><span data-stu-id="c5034-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="c5034-119">Questo comando consente di ottenere le proprietà della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="c5034-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="c5034-120">Questo comando specifica il parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="c5034-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="c5034-121">Il comando ottiene pertanto solo le proprietà della visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="c5034-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="c5034-122">Esempio 3: ottenere le proprietà per tutte le macchine virtuali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c5034-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c5034-123">Questo comando consente di ottenere le proprietà per tutte le macchine virtuali nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c5034-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c5034-124">Esempio 4: ottenere tutte le macchine virtuali nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="c5034-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="c5034-125">Questo comando consente di ottenere tutte le macchine virtuali nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c5034-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="c5034-126">Esempio 5: ottenere tutte le macchine virtuali nella posizione.</span><span class="sxs-lookup"><span data-stu-id="c5034-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="c5034-127">Questo comando consente di ottenere tutte le macchine virtuali nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="c5034-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="c5034-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5034-128">PARAMETERS</span></span>

### <span data-ttu-id="c5034-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5034-129">-DefaultProfile</span></span>
<span data-ttu-id="c5034-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5034-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5034-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="c5034-131">-DisplayHint</span></span>
<span data-ttu-id="c5034-132">Determina il modo in cui viene visualizzato l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="c5034-133">I valori validi sono:--Compact: Visualizza solo le proprietà di primo livello--Expand: Visualizza tutte le proprietà in tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="c5034-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c5034-134">-Location</span></span>
<span data-ttu-id="c5034-135">Specifica un percorso per l'elenco delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c5034-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5034-136">-Name</span></span>
<span data-ttu-id="c5034-137">Specifica il nome della macchina virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c5034-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="c5034-138">-NextLink</span></span>
<span data-ttu-id="c5034-139">Specifica il collegamento successivo.</span><span class="sxs-lookup"><span data-stu-id="c5034-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5034-140">-ResourceGroupName</span></span>
<span data-ttu-id="c5034-141">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5034-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="c5034-142">-Status</span></span>
<span data-ttu-id="c5034-143">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5034-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5034-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5034-144">CommonParameters</span></span>
<span data-ttu-id="c5034-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5034-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5034-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5034-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5034-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5034-147">INPUTS</span></span>

### <span data-ttu-id="c5034-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c5034-148">System.String</span></span>

### <span data-ttu-id="c5034-149">System. Uri</span><span class="sxs-lookup"><span data-stu-id="c5034-149">System.Uri</span></span>

### <span data-ttu-id="c5034-150">Microsoft. Azure. Commands. Compute. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="c5034-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="c5034-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5034-151">OUTPUTS</span></span>

### <span data-ttu-id="c5034-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c5034-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c5034-153">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="c5034-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="c5034-154">Note</span><span class="sxs-lookup"><span data-stu-id="c5034-154">NOTES</span></span>

## <span data-ttu-id="c5034-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5034-155">RELATED LINKS</span></span>

[<span data-ttu-id="c5034-156">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="c5034-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="c5034-158">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="c5034-159">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="c5034-160">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="c5034-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5034-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


