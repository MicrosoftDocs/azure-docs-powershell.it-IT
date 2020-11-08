---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029619"
---
# <span data-ttu-id="8a480-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8a480-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="8a480-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a480-102">SYNOPSIS</span></span>
<span data-ttu-id="8a480-103">Rimuove un disco dall'archivio di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="8a480-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="8a480-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a480-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a480-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a480-105">DESCRIPTION</span></span>
<span data-ttu-id="8a480-106">Il cmdlet **Remove-AzureDisk** rimuove un disco dall'archivio di Azure disk nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8a480-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="8a480-107">Per impostazione predefinita, questo cmdlet non elimina il file del disco rigido virtuale (VHD) dallo spazio di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a480-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="8a480-108">Per eliminare il VHD, specifica il parametro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="8a480-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="8a480-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a480-109">EXAMPLES</span></span>

### <span data-ttu-id="8a480-110">Esempio 1: rimuovere un disco</span><span class="sxs-lookup"><span data-stu-id="8a480-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="8a480-111">Questo comando rimuove il disco denominato ContosoDataDisk Disk dall'archivio disco.</span><span class="sxs-lookup"><span data-stu-id="8a480-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8a480-112">Il comando non consente di eliminare il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a480-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="8a480-113">Esempio 2: rimuovere ed eliminare un disco</span><span class="sxs-lookup"><span data-stu-id="8a480-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="8a480-114">Questo comando rimuove il disco denominato ContosoDataDisk Disk dall'archivio disco.</span><span class="sxs-lookup"><span data-stu-id="8a480-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8a480-115">Questo comando specifica il parametro DeleteVHD.</span><span class="sxs-lookup"><span data-stu-id="8a480-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="8a480-116">Di conseguenza, il comando Elimina il VHD da spazio di archiviazione Azure.</span><span class="sxs-lookup"><span data-stu-id="8a480-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="8a480-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a480-117">PARAMETERS</span></span>

### <span data-ttu-id="8a480-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="8a480-118">-DeleteVHD</span></span>
<span data-ttu-id="8a480-119">Indica che questo cmdlet rimuove il disco rigido virtuale dall'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a480-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="8a480-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="8a480-120">-DiskName</span></span>
<span data-ttu-id="8a480-121">Specifica il nome del disco di dati nel repository del disco rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a480-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a480-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a480-122">-InformationAction</span></span>
<span data-ttu-id="8a480-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8a480-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a480-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a480-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a480-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="8a480-125">Continue</span></span>
- <span data-ttu-id="8a480-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="8a480-126">Ignore</span></span>
- <span data-ttu-id="8a480-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8a480-127">Inquire</span></span>
- <span data-ttu-id="8a480-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a480-128">SilentlyContinue</span></span>
- <span data-ttu-id="8a480-129">Stop</span><span class="sxs-lookup"><span data-stu-id="8a480-129">Stop</span></span>
- <span data-ttu-id="8a480-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8a480-130">Suspend</span></span>

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

### <span data-ttu-id="8a480-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a480-131">-InformationVariable</span></span>
<span data-ttu-id="8a480-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8a480-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a480-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8a480-133">-Profile</span></span>
<span data-ttu-id="8a480-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a480-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a480-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8a480-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a480-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a480-136">CommonParameters</span></span>
<span data-ttu-id="8a480-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a480-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a480-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a480-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a480-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a480-139">INPUTS</span></span>

## <span data-ttu-id="8a480-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a480-140">OUTPUTS</span></span>

## <span data-ttu-id="8a480-141">Note</span><span class="sxs-lookup"><span data-stu-id="8a480-141">NOTES</span></span>

## <span data-ttu-id="8a480-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a480-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a480-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8a480-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="8a480-144">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8a480-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="8a480-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8a480-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


