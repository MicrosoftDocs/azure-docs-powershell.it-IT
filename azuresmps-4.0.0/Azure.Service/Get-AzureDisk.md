---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029816"
---
# <span data-ttu-id="2bfab-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2bfab-101">Get-AzureDisk</span></span>

## <span data-ttu-id="2bfab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bfab-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfab-103">Ottiene informazioni sui dischi nel repository di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="2bfab-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="2bfab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bfab-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2bfab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bfab-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfab-106">Il cmdlet **Get-AzureDisk** ottiene le informazioni sui dischi archiviati nel repository di Azure disk per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="2bfab-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="2bfab-107">Questo cmdlet restituisce un elenco di informazioni per tutti i dischi nel repository.</span><span class="sxs-lookup"><span data-stu-id="2bfab-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="2bfab-108">Per visualizzare le informazioni relative a un disco specifico, specificare il nome del disco.</span><span class="sxs-lookup"><span data-stu-id="2bfab-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="2bfab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bfab-109">EXAMPLES</span></span>

### <span data-ttu-id="2bfab-110">Esempio 1: ottenere informazioni su un disco</span><span class="sxs-lookup"><span data-stu-id="2bfab-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="2bfab-111">Questo comando recupera i dati sulle informazioni sul disco denominato ContosoDataDisk dall'archivio disco.</span><span class="sxs-lookup"><span data-stu-id="2bfab-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="2bfab-112">Esempio 2: ottenere informazioni su tutti i dischi</span><span class="sxs-lookup"><span data-stu-id="2bfab-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="2bfab-113">Questo comando consente di ottenere informazioni su tutti i dischi nel repository del disco.</span><span class="sxs-lookup"><span data-stu-id="2bfab-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="2bfab-114">Esempio 3: ottenere informazioni su un disco</span><span class="sxs-lookup"><span data-stu-id="2bfab-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="2bfab-115">Questo comando consente di ottenere dati per tutti i dischi nel repository del disco che non sono attualmente collegati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2bfab-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="2bfab-116">Il comando ottiene le informazioni su tutti i dischi e passa ogni oggetto al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="2bfab-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="2bfab-117">Questo cmdlet elimina qualsiasi disco che non ha un valore di $Null per la proprietà **legatiai** .</span><span class="sxs-lookup"><span data-stu-id="2bfab-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="2bfab-118">Il comando Formatta l'elenco come tabella usando il cmdlet **Format-Table** .</span><span class="sxs-lookup"><span data-stu-id="2bfab-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="2bfab-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bfab-119">PARAMETERS</span></span>

### <span data-ttu-id="2bfab-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="2bfab-120">-DiskName</span></span>
<span data-ttu-id="2bfab-121">Specifica il nome del disco nel repository del disco sul quale questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="2bfab-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bfab-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2bfab-122">-InformationAction</span></span>
<span data-ttu-id="2bfab-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2bfab-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2bfab-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2bfab-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bfab-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="2bfab-125">Continue</span></span>
- <span data-ttu-id="2bfab-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="2bfab-126">Ignore</span></span>
- <span data-ttu-id="2bfab-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2bfab-127">Inquire</span></span>
- <span data-ttu-id="2bfab-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2bfab-128">SilentlyContinue</span></span>
- <span data-ttu-id="2bfab-129">Stop</span><span class="sxs-lookup"><span data-stu-id="2bfab-129">Stop</span></span>
- <span data-ttu-id="2bfab-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2bfab-130">Suspend</span></span>

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

### <span data-ttu-id="2bfab-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2bfab-131">-InformationVariable</span></span>
<span data-ttu-id="2bfab-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2bfab-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2bfab-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="2bfab-133">-Profile</span></span>
<span data-ttu-id="2bfab-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bfab-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bfab-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2bfab-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2bfab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfab-136">CommonParameters</span></span>
<span data-ttu-id="2bfab-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfab-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfab-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bfab-139">INPUTS</span></span>

## <span data-ttu-id="2bfab-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bfab-140">OUTPUTS</span></span>

## <span data-ttu-id="2bfab-141">Note</span><span class="sxs-lookup"><span data-stu-id="2bfab-141">NOTES</span></span>

## <span data-ttu-id="2bfab-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bfab-142">RELATED LINKS</span></span>

[<span data-ttu-id="2bfab-143">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2bfab-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="2bfab-144">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2bfab-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="2bfab-145">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="2bfab-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


