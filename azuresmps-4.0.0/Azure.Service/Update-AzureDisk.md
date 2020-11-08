---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023383"
---
# <span data-ttu-id="a281f-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a281f-101">Update-AzureDisk</span></span>

## <span data-ttu-id="a281f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a281f-102">SYNOPSIS</span></span>
<span data-ttu-id="a281f-103">Modifica l'etichetta di un disco nel repository di Azure disk.</span><span class="sxs-lookup"><span data-stu-id="a281f-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="a281f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a281f-104">SYNTAX</span></span>

### <span data-ttu-id="a281f-105">Ridimensionare</span><span class="sxs-lookup"><span data-stu-id="a281f-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a281f-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="a281f-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a281f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a281f-107">DESCRIPTION</span></span>
<span data-ttu-id="a281f-108">Il cmdlet **Update-AzureDisk** modifica l'etichetta associata a un disco nel repository del disco dell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a281f-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="a281f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a281f-109">EXAMPLES</span></span>

### <span data-ttu-id="a281f-110">Esempio 1: cambiare l'etichetta di un disco</span><span class="sxs-lookup"><span data-stu-id="a281f-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="a281f-111">Questo comando cambia l'etichetta del disco denominato ContosoOSDisk in non utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a281f-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="a281f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a281f-112">PARAMETERS</span></span>

### <span data-ttu-id="a281f-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="a281f-113">-DiskName</span></span>
<span data-ttu-id="a281f-114">Specifica il nome del disco modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a281f-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a281f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a281f-115">-InformationAction</span></span>
<span data-ttu-id="a281f-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a281f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a281f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a281f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a281f-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="a281f-118">Continue</span></span>
- <span data-ttu-id="a281f-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="a281f-119">Ignore</span></span>
- <span data-ttu-id="a281f-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a281f-120">Inquire</span></span>
- <span data-ttu-id="a281f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a281f-121">SilentlyContinue</span></span>
- <span data-ttu-id="a281f-122">Stop</span><span class="sxs-lookup"><span data-stu-id="a281f-122">Stop</span></span>
- <span data-ttu-id="a281f-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a281f-123">Suspend</span></span>

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

### <span data-ttu-id="a281f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a281f-124">-InformationVariable</span></span>
<span data-ttu-id="a281f-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a281f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a281f-126">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="a281f-126">-Label</span></span>
<span data-ttu-id="a281f-127">Specifica la nuova etichetta per il disco.</span><span class="sxs-lookup"><span data-stu-id="a281f-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a281f-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="a281f-128">-Profile</span></span>
<span data-ttu-id="a281f-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a281f-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a281f-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a281f-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a281f-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a281f-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="a281f-132">Specifica le nuove dimensioni, in gigabyte, per il disco.</span><span class="sxs-lookup"><span data-stu-id="a281f-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a281f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a281f-133">CommonParameters</span></span>
<span data-ttu-id="a281f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a281f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a281f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a281f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a281f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a281f-136">INPUTS</span></span>

## <span data-ttu-id="a281f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a281f-137">OUTPUTS</span></span>

### <span data-ttu-id="a281f-138">DiskContext</span><span class="sxs-lookup"><span data-stu-id="a281f-138">DiskContext</span></span>

## <span data-ttu-id="a281f-139">Note</span><span class="sxs-lookup"><span data-stu-id="a281f-139">NOTES</span></span>

## <span data-ttu-id="a281f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a281f-140">RELATED LINKS</span></span>

[<span data-ttu-id="a281f-141">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a281f-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="a281f-142">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a281f-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="a281f-143">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="a281f-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


