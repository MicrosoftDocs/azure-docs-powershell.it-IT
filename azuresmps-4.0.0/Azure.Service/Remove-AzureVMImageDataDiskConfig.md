---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023455"
---
# <span data-ttu-id="7eb92-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7eb92-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="7eb92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eb92-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb92-103">Rimuove la configurazione del disco dati dall'oggetto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="7eb92-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="7eb92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eb92-104">SYNTAX</span></span>

### <span data-ttu-id="7eb92-105">RemoveByDiskName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7eb92-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7eb92-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="7eb92-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7eb92-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eb92-107">DESCRIPTION</span></span>
<span data-ttu-id="7eb92-108">Il cmdlet **Remove-AzureVMImageDataDiskConfig** rimuove la configurazione del disco dati dall'oggetto **DiskConfigSet** .</span><span class="sxs-lookup"><span data-stu-id="7eb92-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="7eb92-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eb92-109">EXAMPLES</span></span>

### <span data-ttu-id="7eb92-110">Esempio 1: rimuovere la configurazione del disco dati dall'oggetto DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="7eb92-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="7eb92-111">Questo esempio crea un **DiskConfigSet** , lo configura e quindi rimuove il disco di dati.</span><span class="sxs-lookup"><span data-stu-id="7eb92-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="7eb92-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eb92-112">PARAMETERS</span></span>

### <span data-ttu-id="7eb92-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="7eb92-113">-DataDiskName</span></span>
<span data-ttu-id="7eb92-114">Specifica il nome del disco di dati rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb92-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb92-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="7eb92-115">-DiskConfig</span></span>
<span data-ttu-id="7eb92-116">Specifica l'oggetto di configurazione del disco che incapsula il disco del sistema operativo e gli oggetti del disco di dati.</span><span class="sxs-lookup"><span data-stu-id="7eb92-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="7eb92-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7eb92-117">-InformationAction</span></span>
<span data-ttu-id="7eb92-118">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7eb92-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7eb92-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7eb92-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7eb92-120">Continuare</span><span class="sxs-lookup"><span data-stu-id="7eb92-120">Continue</span></span>
- <span data-ttu-id="7eb92-121">Ignora</span><span class="sxs-lookup"><span data-stu-id="7eb92-121">Ignore</span></span>
- <span data-ttu-id="7eb92-122">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7eb92-122">Inquire</span></span>
- <span data-ttu-id="7eb92-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7eb92-123">SilentlyContinue</span></span>
- <span data-ttu-id="7eb92-124">Stop</span><span class="sxs-lookup"><span data-stu-id="7eb92-124">Stop</span></span>
- <span data-ttu-id="7eb92-125">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7eb92-125">Suspend</span></span>

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

### <span data-ttu-id="7eb92-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7eb92-126">-InformationVariable</span></span>
<span data-ttu-id="7eb92-127">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7eb92-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7eb92-128">-Lun</span><span class="sxs-lookup"><span data-stu-id="7eb92-128">-Lun</span></span>
<span data-ttu-id="7eb92-129">Specifica lo slot in cui è installata l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7eb92-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb92-130">CommonParameters</span></span>
<span data-ttu-id="7eb92-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb92-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb92-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb92-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eb92-133">INPUTS</span></span>

## <span data-ttu-id="7eb92-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eb92-134">OUTPUTS</span></span>

### <span data-ttu-id="7eb92-135">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="7eb92-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="7eb92-136">Note</span><span class="sxs-lookup"><span data-stu-id="7eb92-136">NOTES</span></span>

## <span data-ttu-id="7eb92-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eb92-137">RELATED LINKS</span></span>

[<span data-ttu-id="7eb92-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7eb92-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


