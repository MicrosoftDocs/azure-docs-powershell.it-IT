---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023394"
---
# <span data-ttu-id="6863d-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6863d-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="6863d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6863d-102">SYNOPSIS</span></span>
<span data-ttu-id="6863d-103">Imposta le proprietà del disco dati nell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6863d-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="6863d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6863d-104">SYNTAX</span></span>

### <span data-ttu-id="6863d-105">UpdateAzureVMImageParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6863d-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6863d-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="6863d-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6863d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6863d-107">DESCRIPTION</span></span>
<span data-ttu-id="6863d-108">Il cmdlet **set-AzureVMImageDataDiskConfig** imposta le proprietà del disco di dati nell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6863d-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="6863d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6863d-109">EXAMPLES</span></span>

### <span data-ttu-id="6863d-110">Esempio 1: impostare le proprietà del disco dati in un'immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6863d-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="6863d-111">Questo comando imposta le proprietà del disco dati in una macchina virtuale e quindi aggiorna l'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6863d-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="6863d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6863d-112">PARAMETERS</span></span>

### <span data-ttu-id="6863d-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="6863d-113">-DataDiskName</span></span>
<span data-ttu-id="6863d-114">Specifica il nome del disco di dati configurato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6863d-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6863d-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="6863d-115">-DiskConfig</span></span>
<span data-ttu-id="6863d-116">Specifica l'oggetto di configurazione del disco che incapsula il disco del sistema operativo e gli oggetti del disco di dati.</span><span class="sxs-lookup"><span data-stu-id="6863d-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="6863d-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="6863d-117">-HostCaching</span></span>
<span data-ttu-id="6863d-118">Specifica l'attributo della cache host per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6863d-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="6863d-119">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6863d-119">Valid values are:</span></span>

<span data-ttu-id="6863d-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6863d-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6863d-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6863d-121">-InformationAction</span></span>
<span data-ttu-id="6863d-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6863d-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6863d-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6863d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6863d-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="6863d-124">Continue</span></span>
- <span data-ttu-id="6863d-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="6863d-125">Ignore</span></span>
- <span data-ttu-id="6863d-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6863d-126">Inquire</span></span>
- <span data-ttu-id="6863d-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6863d-127">SilentlyContinue</span></span>
- <span data-ttu-id="6863d-128">Stop</span><span class="sxs-lookup"><span data-stu-id="6863d-128">Stop</span></span>
- <span data-ttu-id="6863d-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6863d-129">Suspend</span></span>

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

### <span data-ttu-id="6863d-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6863d-130">-InformationVariable</span></span>
<span data-ttu-id="6863d-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6863d-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6863d-132">-Lun</span><span class="sxs-lookup"><span data-stu-id="6863d-132">-Lun</span></span>
<span data-ttu-id="6863d-133">Specifica lo slot in cui è installata l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6863d-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6863d-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="6863d-134">-MediaLink</span></span>
<span data-ttu-id="6863d-135">Specifica l'URI della posizione in cui viene creata la nuova unità disco rigido virtuale quando viene aggiunto il nuovo disco dati.</span><span class="sxs-lookup"><span data-stu-id="6863d-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6863d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6863d-136">CommonParameters</span></span>
<span data-ttu-id="6863d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6863d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6863d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6863d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6863d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6863d-139">INPUTS</span></span>

## <span data-ttu-id="6863d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6863d-140">OUTPUTS</span></span>

### <span data-ttu-id="6863d-141">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="6863d-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="6863d-142">Note</span><span class="sxs-lookup"><span data-stu-id="6863d-142">NOTES</span></span>

## <span data-ttu-id="6863d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6863d-143">RELATED LINKS</span></span>

[<span data-ttu-id="6863d-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6863d-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


