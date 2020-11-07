---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b663087437097b3e059f9d88c7720696222134e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836691"
---
# <span data-ttu-id="a86a1-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a86a1-101">Save-AzVMImage</span></span>

## <span data-ttu-id="a86a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a86a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a86a1-103">Salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="a86a1-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="a86a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a86a1-104">SYNTAX</span></span>

### <span data-ttu-id="a86a1-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a86a1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a86a1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a86a1-106">IdParameterSetName</span></span>
```
Save-AzVMImage [[-Name] <String>] [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a86a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a86a1-107">DESCRIPTION</span></span>
<span data-ttu-id="a86a1-108">Il cmdlet **Save-AzVMImage** salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="a86a1-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="a86a1-109">Prima di creare un'immagine della macchina virtuale, Sysprep la macchina virtuale e quindi contrassegnarla come generalizzata usando il cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a86a1-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="a86a1-110">L'output di questo cmdlet è un modello JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a86a1-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="a86a1-111">È possibile distribuire macchine virtuali dall'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="a86a1-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="a86a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a86a1-112">EXAMPLES</span></span>

### <span data-ttu-id="a86a1-113">Esempio 1: acquisire una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a86a1-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="a86a1-114">Il primo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="a86a1-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="a86a1-115">Il secondo comando acquisisce una macchina virtuale denominata VirtualMachine07 come VMImage.</span><span class="sxs-lookup"><span data-stu-id="a86a1-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="a86a1-116">La proprietà **output** restituisce un modello JSON.</span><span class="sxs-lookup"><span data-stu-id="a86a1-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="a86a1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a86a1-117">PARAMETERS</span></span>

### <span data-ttu-id="a86a1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a86a1-118">-AsJob</span></span>
<span data-ttu-id="a86a1-119">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a86a1-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a86a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86a1-120">-DefaultProfile</span></span>
<span data-ttu-id="a86a1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a86a1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a86a1-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="a86a1-122">-DestinationContainerName</span></span>
<span data-ttu-id="a86a1-123">Specifica il nome di un contenitore all'interno del contenitore "System" in cui si vogliono contenere le immagini.</span><span class="sxs-lookup"><span data-stu-id="a86a1-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="a86a1-124">Se il contenitore non esiste, viene creato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="a86a1-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="a86a1-125">I dischi rigidi virtuali che costituiscono il VMImage si trovano nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a86a1-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="a86a1-126">Se i VHD sono distribuiti in più account di archiviazione, questo cmdlet crea un contenitore con questo nome in ogni account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a86a1-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="a86a1-127">L'URL dell'immagine salvata è simile a: https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="a86a1-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="a86a1-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a86a1-128">-Id</span></span>
<span data-ttu-id="a86a1-129">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a86a1-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a86a1-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a86a1-130">-Name</span></span>
<span data-ttu-id="a86a1-131">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="a86a1-131">Specifies a name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86a1-132">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="a86a1-132">-Overwrite</span></span>
<span data-ttu-id="a86a1-133">Indica che questo cmdlet sovrascrive tutti i VHD con lo stesso prefisso nel contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a86a1-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="a86a1-134">-Path</span><span class="sxs-lookup"><span data-stu-id="a86a1-134">-Path</span></span>
<span data-ttu-id="a86a1-135">Percorso del file in cui è archiviato il modello dell'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="a86a1-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="a86a1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86a1-136">-ResourceGroupName</span></span>
<span data-ttu-id="a86a1-137">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a86a1-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a86a1-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a86a1-138">-VHDNamePrefix</span></span>
<span data-ttu-id="a86a1-139">Specifica il prefisso nel nome dei BLOB che costituiscono il profilo di archiviazione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="a86a1-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="a86a1-140">Ad esempio, un prefisso vhdPrefix per un disco del sistema operativo restituisce il nome vhdPrefix-OSDISK. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="a86a1-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="a86a1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86a1-141">CommonParameters</span></span>
<span data-ttu-id="a86a1-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86a1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86a1-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86a1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86a1-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a86a1-144">INPUTS</span></span>

### <span data-ttu-id="a86a1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a86a1-145">System.String</span></span>

### <span data-ttu-id="a86a1-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a86a1-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a86a1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a86a1-147">OUTPUTS</span></span>

### <span data-ttu-id="a86a1-148">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a86a1-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a86a1-149">Note</span><span class="sxs-lookup"><span data-stu-id="a86a1-149">NOTES</span></span>

## <span data-ttu-id="a86a1-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a86a1-150">RELATED LINKS</span></span>

[<span data-ttu-id="a86a1-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a86a1-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a86a1-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a86a1-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a86a1-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a86a1-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a86a1-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a86a1-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a86a1-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a86a1-155">Set-AzVM</span></span>](./Set-AzVM.md)


