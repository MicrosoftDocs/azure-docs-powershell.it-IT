---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998211"
---
# <span data-ttu-id="f1c96-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f1c96-101">Save-AzVMImage</span></span>

## <span data-ttu-id="f1c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c96-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c96-103">Salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="f1c96-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="f1c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1c96-104">SYNTAX</span></span>

### <span data-ttu-id="f1c96-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1c96-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1c96-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f1c96-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c96-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f1c96-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c96-108">Il cmdlet **Save-AzVMImage** salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="f1c96-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="f1c96-109">Prima di creare un'immagine della macchina virtuale, preparare la macchina virtuale e quindi contrassegnarla come generalizzata con il cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f1c96-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="f1c96-110">L'output di questo cmdlet è un modello JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="f1c96-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="f1c96-111">È possibile distribuire le macchine virtuali dall'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="f1c96-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="f1c96-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1c96-112">EXAMPLES</span></span>

### <span data-ttu-id="f1c96-113">Esempio 1: Acquisire una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f1c96-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="f1c96-114">Il primo comando contrassegna come generalizzata la macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f1c96-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="f1c96-115">Il secondo comando acquisisce una macchina virtuale denominata VirtualMachine07 come VMImage.</span><span class="sxs-lookup"><span data-stu-id="f1c96-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="f1c96-116">La **proprietà Output** restituisce un modello JSON.</span><span class="sxs-lookup"><span data-stu-id="f1c96-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="f1c96-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c96-117">PARAMETERS</span></span>

### <span data-ttu-id="f1c96-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1c96-118">-AsJob</span></span>
<span data-ttu-id="f1c96-119">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f1c96-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c96-120">-DefaultProfile</span></span>
<span data-ttu-id="f1c96-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c96-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="f1c96-122">-DestinationContainerName</span></span>
<span data-ttu-id="f1c96-123">Specifica il nome di un contenitore all'interno del contenitore "sistema" in cui si vogliono contenere le immagini.</span><span class="sxs-lookup"><span data-stu-id="f1c96-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="f1c96-124">Se il contenitore non esiste, viene creato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f1c96-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="f1c96-125">I dischi rigidi virtuali (VHD) che costituiscono vmImage risiedono nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f1c96-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="f1c96-126">Se i dischi rigidi virtuali sono distribuiti tra più account di archiviazione, questo cmdlet crea un contenitore con questo nome in ogni account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f1c96-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="f1c96-127">L'URL dell'immagine salvata è simile al seguente: https:// \<storageAccountName\> .blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="f1c96-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-128">-Id</span><span class="sxs-lookup"><span data-stu-id="f1c96-128">-Id</span></span>
<span data-ttu-id="f1c96-129">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1c96-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f1c96-130">-Name</span></span>
<span data-ttu-id="f1c96-131">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="f1c96-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f1c96-132">-Overwrite</span></span>
<span data-ttu-id="f1c96-133">Indica che questo cmdlet sovrascrive gli eventuali dischi rigidi virtuali che hanno lo stesso prefisso nel contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1c96-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f1c96-134">-Path</span></span>
<span data-ttu-id="f1c96-135">Percorso del file in cui è archiviato il modello dell'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="f1c96-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c96-136">-ResourceGroupName</span></span>
<span data-ttu-id="f1c96-137">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1c96-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f1c96-138">-VHDNamePrefix</span></span>
<span data-ttu-id="f1c96-139">Specifica il prefisso nel nome dei BLOB che costituiscono il profilo di archiviazione dell'immagine VMImage.</span><span class="sxs-lookup"><span data-stu-id="f1c96-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="f1c96-140">Ad esempio, un prefisso vhdPrefix per un disco del sistema operativo è il nome vhdPrefix-osdisk. \<guid\> vhd.</span><span class="sxs-lookup"><span data-stu-id="f1c96-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c96-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c96-141">CommonParameters</span></span>
<span data-ttu-id="f1c96-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c96-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c96-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1c96-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c96-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="f1c96-144">INPUTS</span></span>

### <span data-ttu-id="f1c96-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f1c96-145">System.String</span></span>

### <span data-ttu-id="f1c96-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1c96-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1c96-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1c96-147">OUTPUTS</span></span>

### <span data-ttu-id="f1c96-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f1c96-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f1c96-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="f1c96-149">NOTES</span></span>

## <span data-ttu-id="f1c96-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1c96-150">RELATED LINKS</span></span>

[<span data-ttu-id="f1c96-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f1c96-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f1c96-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f1c96-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f1c96-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f1c96-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f1c96-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f1c96-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f1c96-155">Set-AZVM</span><span class="sxs-lookup"><span data-stu-id="f1c96-155">Set-AzVM</span></span>](./Set-AzVM.md)


