---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029660"
---
# <span data-ttu-id="4aba1-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="4aba1-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="4aba1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4aba1-102">SYNOPSIS</span></span>
<span data-ttu-id="4aba1-103">Crea un oggetto set di configurazione disco.</span><span class="sxs-lookup"><span data-stu-id="4aba1-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="4aba1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4aba1-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4aba1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aba1-105">DESCRIPTION</span></span>
<span data-ttu-id="4aba1-106">Il cmdlet **New-AzureVMImageDiskConfigSet** crea un oggetto set di configurazione del disco passato al cmdlet di aggiornamento delle immagini.</span><span class="sxs-lookup"><span data-stu-id="4aba1-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="4aba1-107">Incapsula il OSDiskConfig e l'oggetto DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="4aba1-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="4aba1-108">Usare i cmdlet **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** per impostare le proprietà del disco del sistema operativo e dei dischi dati per l'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4aba1-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="4aba1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4aba1-109">EXAMPLES</span></span>

### <span data-ttu-id="4aba1-110">Esempio 1: creare un oggetto set di configurazione del disco</span><span class="sxs-lookup"><span data-stu-id="4aba1-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="4aba1-111">Questo comando crea un oggetto set di configurazione disco e archivia i risultati nella variabile denominata $Disk.</span><span class="sxs-lookup"><span data-stu-id="4aba1-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="4aba1-112">Dopo aver creato la configurazione del disco, viene usata per impostare OSDiskConfig e DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="4aba1-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="4aba1-113">La macchina virtuale viene quindi aggiornata con la configurazione.</span><span class="sxs-lookup"><span data-stu-id="4aba1-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="4aba1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4aba1-114">PARAMETERS</span></span>

### <span data-ttu-id="4aba1-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4aba1-115">-InformationAction</span></span>
<span data-ttu-id="4aba1-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="4aba1-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4aba1-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4aba1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aba1-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="4aba1-118">Continue</span></span>
- <span data-ttu-id="4aba1-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="4aba1-119">Ignore</span></span>
- <span data-ttu-id="4aba1-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="4aba1-120">Inquire</span></span>
- <span data-ttu-id="4aba1-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4aba1-121">SilentlyContinue</span></span>
- <span data-ttu-id="4aba1-122">Stop</span><span class="sxs-lookup"><span data-stu-id="4aba1-122">Stop</span></span>
- <span data-ttu-id="4aba1-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="4aba1-123">Suspend</span></span>

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

### <span data-ttu-id="4aba1-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4aba1-124">-InformationVariable</span></span>
<span data-ttu-id="4aba1-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="4aba1-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4aba1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aba1-126">CommonParameters</span></span>
<span data-ttu-id="4aba1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aba1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aba1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aba1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aba1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4aba1-129">INPUTS</span></span>

## <span data-ttu-id="4aba1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4aba1-130">OUTPUTS</span></span>

### <span data-ttu-id="4aba1-131">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="4aba1-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="4aba1-132">Note</span><span class="sxs-lookup"><span data-stu-id="4aba1-132">NOTES</span></span>

## <span data-ttu-id="4aba1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4aba1-133">RELATED LINKS</span></span>

[<span data-ttu-id="4aba1-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="4aba1-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="4aba1-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4aba1-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="4aba1-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4aba1-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


