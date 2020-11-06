---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521735"
---
# <span data-ttu-id="62c22-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="62c22-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="62c22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62c22-102">SYNOPSIS</span></span>
<span data-ttu-id="62c22-103">Salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="62c22-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62c22-104">SYNTAX</span></span>

### <span data-ttu-id="62c22-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62c22-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62c22-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="62c22-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c22-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62c22-107">DESCRIPTION</span></span>
<span data-ttu-id="62c22-108">Il cmdlet **Save-AzureRmVMImage** salva una macchina virtuale come VMImage.</span><span class="sxs-lookup"><span data-stu-id="62c22-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="62c22-109">Prima di creare un'immagine della macchina virtuale, Sysprep la macchina virtuale e quindi contrassegnarla come generalizzata usando il cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="62c22-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="62c22-110">L'output di questo cmdlet è un modello JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="62c22-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="62c22-111">È possibile distribuire macchine virtuali dall'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="62c22-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="62c22-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62c22-112">EXAMPLES</span></span>

### <span data-ttu-id="62c22-113">Esempio 1: acquisire una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="62c22-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="62c22-114">Il primo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="62c22-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="62c22-115">Il secondo comando acquisisce una macchina virtuale denominata VirtualMachine07 come VMImage.</span><span class="sxs-lookup"><span data-stu-id="62c22-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="62c22-116">La proprietà **output** restituisce un modello JSON.</span><span class="sxs-lookup"><span data-stu-id="62c22-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="62c22-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62c22-117">PARAMETERS</span></span>

### <span data-ttu-id="62c22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c22-118">-DefaultProfile</span></span>
<span data-ttu-id="62c22-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62c22-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c22-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="62c22-120">-DestinationContainerName</span></span>
<span data-ttu-id="62c22-121">Specifica il nome di un contenitore all'interno del contenitore "System" in cui si vogliono contenere le immagini.</span><span class="sxs-lookup"><span data-stu-id="62c22-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="62c22-122">Se il contenitore non esiste, viene creato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="62c22-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="62c22-123">I dischi rigidi virtuali che costituiscono il VMImage si trovano nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="62c22-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="62c22-124">Se i VHD sono distribuiti in più account di archiviazione, questo cmdlet crea un contenitore con questo nome in ogni account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="62c22-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="62c22-125">L'URL dell'immagine salvata è simile a:</span><span class="sxs-lookup"><span data-stu-id="62c22-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="62c22-126"> https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="62c22-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="62c22-127">-ID</span><span class="sxs-lookup"><span data-stu-id="62c22-127">-Id</span></span>
<span data-ttu-id="62c22-128">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62c22-128">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="62c22-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="62c22-129">-Name</span></span>
<span data-ttu-id="62c22-130">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="62c22-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c22-131">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="62c22-131">-Overwrite</span></span>
<span data-ttu-id="62c22-132">Indica che questo cmdlet sovrascrive tutti i VHD con lo stesso prefisso nel contenitore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62c22-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="62c22-133">-Path</span><span class="sxs-lookup"><span data-stu-id="62c22-133">-Path</span></span>
<span data-ttu-id="62c22-134">Specifica il percorso del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="62c22-134">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="62c22-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c22-135">-ResourceGroupName</span></span>
<span data-ttu-id="62c22-136">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62c22-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62c22-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="62c22-137">-VHDNamePrefix</span></span>
<span data-ttu-id="62c22-138">Specifica il prefisso nel nome dei BLOB che costituiscono il profilo di archiviazione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="62c22-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="62c22-139">Ad esempio, un prefisso vhdPrefix per un disco del sistema operativo restituisce il nome vhdPrefix-OSDISK. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="62c22-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="62c22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c22-140">CommonParameters</span></span>
<span data-ttu-id="62c22-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c22-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c22-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c22-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62c22-143">INPUTS</span></span>

## <span data-ttu-id="62c22-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62c22-144">OUTPUTS</span></span>

## <span data-ttu-id="62c22-145">Note</span><span class="sxs-lookup"><span data-stu-id="62c22-145">NOTES</span></span>

## <span data-ttu-id="62c22-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62c22-146">RELATED LINKS</span></span>

[<span data-ttu-id="62c22-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="62c22-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="62c22-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="62c22-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="62c22-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="62c22-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="62c22-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="62c22-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="62c22-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="62c22-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


