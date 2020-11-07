---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867139"
---
# <span data-ttu-id="eb765-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eb765-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="eb765-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb765-102">SYNOPSIS</span></span>
<span data-ttu-id="eb765-103">Salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="eb765-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb765-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb765-104">SYNTAX</span></span>

### <span data-ttu-id="eb765-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb765-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb765-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eb765-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb765-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb765-107">DESCRIPTION</span></span>
<span data-ttu-id="eb765-108">Il cmdlet **Save-AzureRmVMImage** salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="eb765-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="eb765-109">Prima di creare un'immagine della macchina virtuale, Sysprep la macchina virtuale e quindi contrassegnarla come generalizzata usando il cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="eb765-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="eb765-110">L'output di questo cmdlet è un modello JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="eb765-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="eb765-111">È possibile distribuire macchine virtuali dall'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="eb765-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="eb765-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb765-112">EXAMPLES</span></span>

### <span data-ttu-id="eb765-113">Esempio 1: acquisire una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="eb765-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="eb765-114">Il primo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="eb765-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="eb765-115">Il secondo comando acquisisce una macchina virtuale denominata VirtualMachine07 come VMImage.</span><span class="sxs-lookup"><span data-stu-id="eb765-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="eb765-116">La proprietà **output** restituisce un modello JSON.</span><span class="sxs-lookup"><span data-stu-id="eb765-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="eb765-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb765-117">PARAMETERS</span></span>

### <span data-ttu-id="eb765-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb765-118">-AsJob</span></span>
<span data-ttu-id="eb765-119">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="eb765-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eb765-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb765-120">-DefaultProfile</span></span>
<span data-ttu-id="eb765-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb765-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb765-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="eb765-122">-DestinationContainerName</span></span>
<span data-ttu-id="eb765-123">Specifica il nome di un contenitore all'interno del contenitore "System" in cui si vogliono contenere le immagini.</span><span class="sxs-lookup"><span data-stu-id="eb765-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="eb765-124">Se il contenitore non esiste, viene creato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="eb765-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="eb765-125">I dischi rigidi virtuali che costituiscono il VMImage si trovano nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="eb765-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="eb765-126">Se i VHD sono distribuiti in più account di archiviazione, questo cmdlet crea un contenitore con questo nome in ogni account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eb765-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="eb765-127">L'URL dell'immagine salvata è simile a:</span><span class="sxs-lookup"><span data-stu-id="eb765-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="eb765-128"> https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="eb765-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="eb765-129">-ID</span><span class="sxs-lookup"><span data-stu-id="eb765-129">-Id</span></span>
<span data-ttu-id="eb765-130">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb765-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="eb765-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb765-131">-Name</span></span>
<span data-ttu-id="eb765-132">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="eb765-132">Specifies a name.</span></span>

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

### <span data-ttu-id="eb765-133">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="eb765-133">-Overwrite</span></span>
<span data-ttu-id="eb765-134">Indica che questo cmdlet sovrascrive tutti i VHD con lo stesso prefisso nel contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eb765-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="eb765-135">-Path</span><span class="sxs-lookup"><span data-stu-id="eb765-135">-Path</span></span>
<span data-ttu-id="eb765-136">Specifica il percorso del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb765-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="eb765-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb765-137">-ResourceGroupName</span></span>
<span data-ttu-id="eb765-138">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eb765-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eb765-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="eb765-139">-VHDNamePrefix</span></span>
<span data-ttu-id="eb765-140">Specifica il prefisso nel nome dei BLOB che costituiscono il profilo di archiviazione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="eb765-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="eb765-141">Ad esempio, un prefisso vhdPrefix per un disco del sistema operativo restituisce il nome vhdPrefix-OSDISK. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="eb765-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="eb765-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb765-142">CommonParameters</span></span>
<span data-ttu-id="eb765-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb765-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb765-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb765-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb765-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb765-145">INPUTS</span></span>

### <span data-ttu-id="eb765-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eb765-146">None</span></span>
<span data-ttu-id="eb765-147">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="eb765-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb765-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb765-148">OUTPUTS</span></span>

### <span data-ttu-id="eb765-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="eb765-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="eb765-150">Note</span><span class="sxs-lookup"><span data-stu-id="eb765-150">NOTES</span></span>

## <span data-ttu-id="eb765-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb765-151">RELATED LINKS</span></span>

[<span data-ttu-id="eb765-152">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eb765-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="eb765-153">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="eb765-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="eb765-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="eb765-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="eb765-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="eb765-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="eb765-156">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eb765-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


