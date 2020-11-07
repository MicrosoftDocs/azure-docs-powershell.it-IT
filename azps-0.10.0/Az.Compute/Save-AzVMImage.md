---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863469"
---
# <span data-ttu-id="851bc-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="851bc-101">Save-AzVMImage</span></span>

## <span data-ttu-id="851bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="851bc-102">SYNOPSIS</span></span>
<span data-ttu-id="851bc-103">Salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="851bc-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="851bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="851bc-104">SYNTAX</span></span>

### <span data-ttu-id="851bc-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="851bc-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="851bc-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="851bc-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="851bc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="851bc-107">DESCRIPTION</span></span>
<span data-ttu-id="851bc-108">Il cmdlet **Save-AzVMImage** salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="851bc-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="851bc-109">Prima di creare un'immagine della macchina virtuale, Sysprep la macchina virtuale e quindi contrassegnarla come generalizzata usando il cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="851bc-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>

<span data-ttu-id="851bc-110">L'output di questo cmdlet è un modello JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="851bc-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="851bc-111">È possibile distribuire macchine virtuali dall'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="851bc-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="851bc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="851bc-112">EXAMPLES</span></span>

### <span data-ttu-id="851bc-113">Esempio 1: acquisire una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="851bc-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="851bc-114">Il primo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="851bc-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="851bc-115">Il secondo comando acquisisce una macchina virtuale denominata VirtualMachine07 come VMImage.</span><span class="sxs-lookup"><span data-stu-id="851bc-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="851bc-116">La proprietà **output** restituisce un modello JSON.</span><span class="sxs-lookup"><span data-stu-id="851bc-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="851bc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="851bc-117">PARAMETERS</span></span>

### <span data-ttu-id="851bc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="851bc-118">-AsJob</span></span>
<span data-ttu-id="851bc-119">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="851bc-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851bc-120">-DefaultProfile</span></span>
<span data-ttu-id="851bc-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="851bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="851bc-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="851bc-122">-DestinationContainerName</span></span>
<span data-ttu-id="851bc-123">Specifica il nome di un contenitore all'interno del contenitore "System" in cui si vogliono contenere le immagini.</span><span class="sxs-lookup"><span data-stu-id="851bc-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="851bc-124">Se il contenitore non esiste, viene creato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="851bc-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="851bc-125">I dischi rigidi virtuali che costituiscono il VMImage si trovano nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="851bc-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="851bc-126">Se i VHD sono distribuiti in più account di archiviazione, questo cmdlet crea un contenitore con questo nome in ogni account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="851bc-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="851bc-127">L'URL dell'immagine salvata è simile a:</span><span class="sxs-lookup"><span data-stu-id="851bc-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="851bc-128"> https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \< imagesContainer \> / \< vhdPrefix-osDisk. \> xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="851bc-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-129">-ID</span><span class="sxs-lookup"><span data-stu-id="851bc-129">-Id</span></span>
<span data-ttu-id="851bc-130">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="851bc-130">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="851bc-131">-Name</span></span>
<span data-ttu-id="851bc-132">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="851bc-132">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-133">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="851bc-133">-Overwrite</span></span>
<span data-ttu-id="851bc-134">Indica che questo cmdlet sovrascrive tutti i VHD con lo stesso prefisso nel contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="851bc-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-135">-Path</span><span class="sxs-lookup"><span data-stu-id="851bc-135">-Path</span></span>
<span data-ttu-id="851bc-136">Specifica il percorso del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="851bc-136">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851bc-137">-ResourceGroupName</span></span>
<span data-ttu-id="851bc-138">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="851bc-138">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="851bc-139">-VHDNamePrefix</span></span>
<span data-ttu-id="851bc-140">Specifica il prefisso nel nome dei BLOB che costituiscono il profilo di archiviazione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="851bc-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="851bc-141">Ad esempio, un prefisso vhdPrefix per un disco del sistema operativo restituisce il nome vhdPrefix-OSDISK. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="851bc-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851bc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851bc-142">CommonParameters</span></span>
<span data-ttu-id="851bc-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851bc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851bc-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851bc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851bc-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="851bc-145">INPUTS</span></span>

### <span data-ttu-id="851bc-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="851bc-146">None</span></span>
<span data-ttu-id="851bc-147">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="851bc-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="851bc-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="851bc-148">OUTPUTS</span></span>

### <span data-ttu-id="851bc-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="851bc-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="851bc-150">Note</span><span class="sxs-lookup"><span data-stu-id="851bc-150">NOTES</span></span>

## <span data-ttu-id="851bc-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="851bc-151">RELATED LINKS</span></span>

[<span data-ttu-id="851bc-152">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="851bc-152">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="851bc-153">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="851bc-153">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="851bc-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="851bc-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="851bc-155">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="851bc-155">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="851bc-156">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="851bc-156">Set-AzVM</span></span>](./Set-AzVM.md)


