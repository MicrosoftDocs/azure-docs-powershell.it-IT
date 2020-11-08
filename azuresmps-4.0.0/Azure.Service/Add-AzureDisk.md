---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029855"
---
# <span data-ttu-id="05ab8-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="05ab8-101">Add-AzureDisk</span></span>

## <span data-ttu-id="05ab8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="05ab8-103">Aggiunge un disco all'archivio di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="05ab8-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="05ab8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05ab8-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="05ab8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="05ab8-106">Il cmdlet **Add-AzureDisk** aggiunge un disco all'archivio di Azure disk nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="05ab8-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="05ab8-107">Questo cmdlet può aggiungere un disco di sistema o un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="05ab8-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="05ab8-108">Per aggiungere un disco di sistema, specificare un tipo di sistema operativo usando il parametro *OS* .</span><span class="sxs-lookup"><span data-stu-id="05ab8-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="05ab8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05ab8-109">EXAMPLES</span></span>

### <span data-ttu-id="05ab8-110">Esempio 1: aggiungere un disco di avvio che usa il sistema operativo Windows</span><span class="sxs-lookup"><span data-stu-id="05ab8-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="05ab8-111">Questo comando aggiunge un disco di sistema al repository del disco.</span><span class="sxs-lookup"><span data-stu-id="05ab8-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="05ab8-112">Il disco di sistema usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="05ab8-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="05ab8-113">Esempio 2: aggiungere un disco dati</span><span class="sxs-lookup"><span data-stu-id="05ab8-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="05ab8-114">Questo comando aggiunge un disco dati.</span><span class="sxs-lookup"><span data-stu-id="05ab8-114">This command adds a data disk.</span></span>

### <span data-ttu-id="05ab8-115">Esempio 3: aggiungere un disco di sistema Linux</span><span class="sxs-lookup"><span data-stu-id="05ab8-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="05ab8-116">Questo comando aggiunge un disco di sistema Linux.</span><span class="sxs-lookup"><span data-stu-id="05ab8-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="05ab8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05ab8-117">PARAMETERS</span></span>

### <span data-ttu-id="05ab8-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="05ab8-118">-DiskName</span></span>
<span data-ttu-id="05ab8-119">Specifica il nome del disco aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ab8-119">Specifies the name of the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ab8-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="05ab8-120">-InformationAction</span></span>
<span data-ttu-id="05ab8-121">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="05ab8-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="05ab8-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="05ab8-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05ab8-123">Continuare</span><span class="sxs-lookup"><span data-stu-id="05ab8-123">Continue</span></span>
- <span data-ttu-id="05ab8-124">Ignora</span><span class="sxs-lookup"><span data-stu-id="05ab8-124">Ignore</span></span>
- <span data-ttu-id="05ab8-125">Informarsi</span><span class="sxs-lookup"><span data-stu-id="05ab8-125">Inquire</span></span>
- <span data-ttu-id="05ab8-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="05ab8-126">SilentlyContinue</span></span>
- <span data-ttu-id="05ab8-127">Stop</span><span class="sxs-lookup"><span data-stu-id="05ab8-127">Stop</span></span>
- <span data-ttu-id="05ab8-128">Sospensione</span><span class="sxs-lookup"><span data-stu-id="05ab8-128">Suspend</span></span>

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

### <span data-ttu-id="05ab8-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="05ab8-129">-InformationVariable</span></span>
<span data-ttu-id="05ab8-130">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="05ab8-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="05ab8-131">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="05ab8-131">-Label</span></span>
<span data-ttu-id="05ab8-132">Specifica un'etichetta disco per il disco aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ab8-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ab8-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="05ab8-133">-MediaLocation</span></span>
<span data-ttu-id="05ab8-134">Specifica la posizione fisica del disco in Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="05ab8-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="05ab8-135">Questo valore fa riferimento a una pagina BLOB nell'account corrente dell'abbonamento e dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="05ab8-135">This value refers to a blob page in the current subscription and storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ab8-136">-OS</span><span class="sxs-lookup"><span data-stu-id="05ab8-136">-OS</span></span>
<span data-ttu-id="05ab8-137">Specifica il tipo di sistema operativo per un disco di sistema.</span><span class="sxs-lookup"><span data-stu-id="05ab8-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="05ab8-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="05ab8-138">Valid values are:</span></span> 

- <span data-ttu-id="05ab8-139">Windows</span><span class="sxs-lookup"><span data-stu-id="05ab8-139">Windows</span></span> 
- <span data-ttu-id="05ab8-140">Linux</span><span class="sxs-lookup"><span data-stu-id="05ab8-140">Linux</span></span> 

<span data-ttu-id="05ab8-141">Se non specifichi questo parametro, il cmdlet aggiunge il disco come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="05ab8-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ab8-142">-Profile</span><span class="sxs-lookup"><span data-stu-id="05ab8-142">-Profile</span></span>
<span data-ttu-id="05ab8-143">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ab8-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05ab8-144">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="05ab8-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ab8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ab8-145">CommonParameters</span></span>
<span data-ttu-id="05ab8-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ab8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ab8-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ab8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ab8-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05ab8-148">INPUTS</span></span>

## <span data-ttu-id="05ab8-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05ab8-149">OUTPUTS</span></span>

### <span data-ttu-id="05ab8-150">DiskContext</span><span class="sxs-lookup"><span data-stu-id="05ab8-150">DiskContext</span></span>

## <span data-ttu-id="05ab8-151">Note</span><span class="sxs-lookup"><span data-stu-id="05ab8-151">NOTES</span></span>

## <span data-ttu-id="05ab8-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05ab8-152">RELATED LINKS</span></span>

[<span data-ttu-id="05ab8-153">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="05ab8-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="05ab8-154">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="05ab8-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="05ab8-155">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="05ab8-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


