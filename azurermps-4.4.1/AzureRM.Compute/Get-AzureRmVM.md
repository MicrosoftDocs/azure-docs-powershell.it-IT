---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685741"
---
# <span data-ttu-id="739fc-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="739fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="739fc-102">SYNOPSIS</span></span>
<span data-ttu-id="739fc-103">Ottiene le proprietà di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="739fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="739fc-104">SYNTAX</span></span>

### <span data-ttu-id="739fc-105">ListAllVirtualMachinesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="739fc-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739fc-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="739fc-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="739fc-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="739fc-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739fc-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="739fc-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="739fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="739fc-109">DESCRIPTION</span></span>
<span data-ttu-id="739fc-110">Il cmdlet **Get-AzureRmVM** ottiene la visualizzazione modello e la visualizzazione istanza di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="739fc-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="739fc-111">La visualizzazione modello rappresenta le proprietà specificate dall'utente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="739fc-112">La visualizzazione istanza è lo stato del livello di istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="739fc-113">Specifica il parametro *status* per ottenere solo la visualizzazione istanza di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="739fc-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="739fc-114">EXAMPLES</span></span>

### <span data-ttu-id="739fc-115">Esempio 1: ottenere le proprietà di visualizzazione modello e istanza</span><span class="sxs-lookup"><span data-stu-id="739fc-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="739fc-116">Questo comando consente di ottenere le proprietà visualizzazione modello e visualizzazione istanza della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="739fc-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="739fc-117">Esempio 2: ottenere le proprietà della visualizzazione istanza</span><span class="sxs-lookup"><span data-stu-id="739fc-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="739fc-118">Questo comando consente di ottenere le proprietà della macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="739fc-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="739fc-119">Questo comando specifica il parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="739fc-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="739fc-120">Il comando ottiene pertanto solo le proprietà della visualizzazione istanza.</span><span class="sxs-lookup"><span data-stu-id="739fc-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="739fc-121">Esempio 3: ottenere le proprietà per tutte le macchine virtuali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="739fc-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="739fc-122">Questo comando consente di ottenere le proprietà per tutte le macchine virtuali nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="739fc-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="739fc-123">Esempio 4: ottenere tutte le macchine virtuali nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="739fc-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="739fc-124">Questo comando consente di ottenere tutte le macchine virtuali nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="739fc-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="739fc-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="739fc-125">PARAMETERS</span></span>

### <span data-ttu-id="739fc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739fc-126">-DefaultProfile</span></span>
<span data-ttu-id="739fc-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="739fc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="739fc-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="739fc-128">-DisplayHint</span></span>
<span data-ttu-id="739fc-129">Determina il modo in cui viene visualizzato l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="739fc-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="739fc-130">Valid values are:</span></span>

<span data-ttu-id="739fc-131">--Compatta: Visualizza solo le proprietà di primo livello</span><span class="sxs-lookup"><span data-stu-id="739fc-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="739fc-132">--Expand: Visualizza tutte le proprietà in tutti i livelli</span><span class="sxs-lookup"><span data-stu-id="739fc-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="739fc-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="739fc-133">-Name</span></span>
<span data-ttu-id="739fc-134">Specifica il nome della macchina virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="739fc-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="739fc-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="739fc-135">-NextLink</span></span>
<span data-ttu-id="739fc-136">Specifica il collegamento successivo.</span><span class="sxs-lookup"><span data-stu-id="739fc-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="739fc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="739fc-137">-ResourceGroupName</span></span>
<span data-ttu-id="739fc-138">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="739fc-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="739fc-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="739fc-139">-Status</span></span>
<span data-ttu-id="739fc-140">Indica che questo cmdlet ottiene solo la visualizzazione istanza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="739fc-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="739fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739fc-141">CommonParameters</span></span>
<span data-ttu-id="739fc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="739fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739fc-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="739fc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739fc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="739fc-144">INPUTS</span></span>

## <span data-ttu-id="739fc-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="739fc-145">OUTPUTS</span></span>

## <span data-ttu-id="739fc-146">Note</span><span class="sxs-lookup"><span data-stu-id="739fc-146">NOTES</span></span>

## <span data-ttu-id="739fc-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="739fc-147">RELATED LINKS</span></span>

[<span data-ttu-id="739fc-148">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="739fc-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="739fc-150">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="739fc-151">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="739fc-152">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="739fc-153">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="739fc-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


