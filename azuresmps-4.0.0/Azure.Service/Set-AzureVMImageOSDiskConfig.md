---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023402"
---
# <span data-ttu-id="024a8-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="024a8-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="024a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="024a8-102">SYNOPSIS</span></span>
<span data-ttu-id="024a8-103">Imposta le proprietà del disco del sistema operativo nell'immagine di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="024a8-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="024a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="024a8-104">SYNTAX</span></span>

### <span data-ttu-id="024a8-105">UpdateAzureVMImageParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="024a8-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="024a8-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="024a8-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="024a8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="024a8-107">DESCRIPTION</span></span>
<span data-ttu-id="024a8-108">Il cmdlet **set-AzureVMImageOSDiskConfig** imposta le proprietà del disco del sistema operativo in un'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="024a8-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="024a8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="024a8-109">EXAMPLES</span></span>

### <span data-ttu-id="024a8-110">Esempio 1: impostare le proprietà del disco del sistema operativo in un'immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="024a8-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="024a8-111">Questo esempio imposta le proprietà del disco del sistema operativo in un'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="024a8-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="024a8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="024a8-112">PARAMETERS</span></span>

### <span data-ttu-id="024a8-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="024a8-113">-DiskConfig</span></span>
<span data-ttu-id="024a8-114">Specifica l'oggetto di configurazione del disco che incapsula il disco del sistema operativo e gli oggetti del disco di dati.</span><span class="sxs-lookup"><span data-stu-id="024a8-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="024a8-115">-HostCaching</span></span>
<span data-ttu-id="024a8-116">Specifica l'attributo della cache host per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="024a8-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="024a8-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="024a8-117">Valid values are:</span></span>

<span data-ttu-id="024a8-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="024a8-118">--ReadOnly --ReadWrite</span></span>

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

### <span data-ttu-id="024a8-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="024a8-119">-InformationAction</span></span>
<span data-ttu-id="024a8-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="024a8-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="024a8-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="024a8-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="024a8-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="024a8-122">Continue</span></span>
- <span data-ttu-id="024a8-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="024a8-123">Ignore</span></span>
- <span data-ttu-id="024a8-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="024a8-124">Inquire</span></span>
- <span data-ttu-id="024a8-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="024a8-125">SilentlyContinue</span></span>
- <span data-ttu-id="024a8-126">Stop</span><span class="sxs-lookup"><span data-stu-id="024a8-126">Stop</span></span>
- <span data-ttu-id="024a8-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="024a8-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="024a8-128">-InformationVariable</span></span>
<span data-ttu-id="024a8-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="024a8-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="024a8-130">-MediaLink</span></span>
<span data-ttu-id="024a8-131">Specifica l'URI della posizione in cui viene creata la nuova unità disco rigido virtuale quando viene aggiunto il nuovo disco dati.</span><span class="sxs-lookup"><span data-stu-id="024a8-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-132">-OS</span><span class="sxs-lookup"><span data-stu-id="024a8-132">-OS</span></span>
<span data-ttu-id="024a8-133">Specifica il sistema operativo della configurazione del disco.</span><span class="sxs-lookup"><span data-stu-id="024a8-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="024a8-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="024a8-134">Valid values are:</span></span>

- <span data-ttu-id="024a8-135">Windows</span><span class="sxs-lookup"><span data-stu-id="024a8-135">Windows</span></span>
- <span data-ttu-id="024a8-136">Linux</span><span class="sxs-lookup"><span data-stu-id="024a8-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="024a8-137">-OSState</span></span>
<span data-ttu-id="024a8-138">Specifica lo stato del sistema operativo per l'immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="024a8-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="024a8-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="024a8-139">Valid values are:</span></span>

- <span data-ttu-id="024a8-140">Generalizzata</span><span class="sxs-lookup"><span data-stu-id="024a8-140">Generalized</span></span>
- <span data-ttu-id="024a8-141">Specializzata</span><span class="sxs-lookup"><span data-stu-id="024a8-141">Specialized</span></span>

<span data-ttu-id="024a8-142">L'uso di questo parametro indica la tua intenzione di acquisire l'immagine della macchina virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="024a8-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="024a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024a8-143">CommonParameters</span></span>
<span data-ttu-id="024a8-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="024a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024a8-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="024a8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024a8-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="024a8-146">INPUTS</span></span>

## <span data-ttu-id="024a8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="024a8-147">OUTPUTS</span></span>

### <span data-ttu-id="024a8-148">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="024a8-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="024a8-149">Note</span><span class="sxs-lookup"><span data-stu-id="024a8-149">NOTES</span></span>

## <span data-ttu-id="024a8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="024a8-150">RELATED LINKS</span></span>

[<span data-ttu-id="024a8-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="024a8-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


