---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029665"
---
# <span data-ttu-id="d9751-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d9751-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="d9751-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9751-102">SYNOPSIS</span></span>
<span data-ttu-id="d9751-103">Rigenera le chiavi di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9751-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="d9751-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9751-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d9751-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9751-105">DESCRIPTION</span></span>
<span data-ttu-id="d9751-106">Il cmdlet **New-AzureStorageKey** rigenera la chiave primaria o secondaria per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9751-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="d9751-107">Restituisce un oggetto che contiene il nome dell'account di archiviazione, la chiave primaria e la chiave secondaria come proprietà.</span><span class="sxs-lookup"><span data-stu-id="d9751-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="d9751-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9751-108">EXAMPLES</span></span>

### <span data-ttu-id="d9751-109">Esempio 1: rigenerare una chiave di archiviazione primaria</span><span class="sxs-lookup"><span data-stu-id="d9751-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="d9751-110">Questo comando rigenera la chiave di archiviazione primaria per l'account di archiviazione di ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="d9751-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="d9751-111">Esempio 2: rigenerare un tasto di archiviazione secondario e salvarlo in una variabile</span><span class="sxs-lookup"><span data-stu-id="d9751-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="d9751-112">Questo comando rigenera la chiave di archiviazione secondaria per l'account di archiviazione di ContosoStore01 e archivia le informazioni chiave dell'account di archiviazione aggiornate nella $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="d9751-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="d9751-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9751-113">PARAMETERS</span></span>

### <span data-ttu-id="d9751-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d9751-114">-InformationAction</span></span>
<span data-ttu-id="d9751-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d9751-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d9751-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9751-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9751-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="d9751-117">Continue</span></span>
- <span data-ttu-id="d9751-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="d9751-118">Ignore</span></span>
- <span data-ttu-id="d9751-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d9751-119">Inquire</span></span>
- <span data-ttu-id="d9751-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d9751-120">SilentlyContinue</span></span>
- <span data-ttu-id="d9751-121">Stop</span><span class="sxs-lookup"><span data-stu-id="d9751-121">Stop</span></span>
- <span data-ttu-id="d9751-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d9751-122">Suspend</span></span>

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

### <span data-ttu-id="d9751-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d9751-123">-InformationVariable</span></span>
<span data-ttu-id="d9751-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d9751-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d9751-125">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="d9751-125">-KeyType</span></span>
<span data-ttu-id="d9751-126">Specifica il tasto da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="d9751-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d9751-127">I valori validi sono: primario e secondario.</span><span class="sxs-lookup"><span data-stu-id="d9751-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9751-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="d9751-128">-Profile</span></span>
<span data-ttu-id="d9751-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9751-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9751-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d9751-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9751-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9751-131">-StorageAccountName</span></span>
<span data-ttu-id="d9751-132">Specifica il nome dell'account di archiviazione di Azure per cui rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="d9751-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9751-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9751-133">CommonParameters</span></span>
<span data-ttu-id="d9751-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9751-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9751-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9751-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9751-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9751-136">INPUTS</span></span>

## <span data-ttu-id="d9751-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9751-137">OUTPUTS</span></span>

### <span data-ttu-id="d9751-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d9751-138">StorageServiceKeys</span></span>

## <span data-ttu-id="d9751-139">Note</span><span class="sxs-lookup"><span data-stu-id="d9751-139">NOTES</span></span>

## <span data-ttu-id="d9751-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9751-140">RELATED LINKS</span></span>

[<span data-ttu-id="d9751-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d9751-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


