---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023506"
---
# <span data-ttu-id="d4d24-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d4d24-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="d4d24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4d24-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d24-103">Restituisce i tasti dell'account di archiviazione primari e secondari per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d24-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="d4d24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4d24-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4d24-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4d24-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d24-106">Il cmdlet **Get-AzureStorageKey** restituisce un oggetto con il nome dell'account di archiviazione di Azure, la chiave dell'account principale e la chiave dell'account secondario dell'account di archiviazione di Azure specificato come proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4d24-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="d4d24-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4d24-107">EXAMPLES</span></span>

### <span data-ttu-id="d4d24-108">Esempio 1: ottenere un oggetto che contiene chiavi di archiviazione primarie e secondarie</span><span class="sxs-lookup"><span data-stu-id="d4d24-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="d4d24-109">Questo comando ottiene un oggetto con le chiavi di archiviazione primarie e secondarie per l'account di archiviazione ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="d4d24-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="d4d24-110">Esempio 2: ottenere la chiave dell'account di archiviazione principale e archiviarla in una variabile</span><span class="sxs-lookup"><span data-stu-id="d4d24-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="d4d24-111">Questo comando inserisce la chiave dell'account di archiviazione principale per l'account di archiviazione di ContosoStore01 nella variabile $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="d4d24-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="d4d24-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4d24-112">PARAMETERS</span></span>

### <span data-ttu-id="d4d24-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d4d24-113">-InformationAction</span></span>
<span data-ttu-id="d4d24-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d4d24-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d4d24-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4d24-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4d24-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="d4d24-116">Continue</span></span>
- <span data-ttu-id="d4d24-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="d4d24-117">Ignore</span></span>
- <span data-ttu-id="d4d24-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d4d24-118">Inquire</span></span>
- <span data-ttu-id="d4d24-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4d24-119">SilentlyContinue</span></span>
- <span data-ttu-id="d4d24-120">Stop</span><span class="sxs-lookup"><span data-stu-id="d4d24-120">Stop</span></span>
- <span data-ttu-id="d4d24-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d4d24-121">Suspend</span></span>

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

### <span data-ttu-id="d4d24-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4d24-122">-InformationVariable</span></span>
<span data-ttu-id="d4d24-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d4d24-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d4d24-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="d4d24-124">-Profile</span></span>
<span data-ttu-id="d4d24-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d24-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4d24-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d4d24-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4d24-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d4d24-127">-StorageAccountName</span></span>
<span data-ttu-id="d4d24-128">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4d24-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d24-129">CommonParameters</span></span>
<span data-ttu-id="d4d24-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d24-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d24-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d24-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4d24-132">INPUTS</span></span>

## <span data-ttu-id="d4d24-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4d24-133">OUTPUTS</span></span>

## <span data-ttu-id="d4d24-134">Note</span><span class="sxs-lookup"><span data-stu-id="d4d24-134">NOTES</span></span>
* <span data-ttu-id="d4d24-135">Per ottenere assistenza per Node.js, usare il `help node-dev` comando.</span><span class="sxs-lookup"><span data-stu-id="d4d24-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="d4d24-136">Per informazioni sulle estensioni PHP, usa il `help php-dev` comando.</span><span class="sxs-lookup"><span data-stu-id="d4d24-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="d4d24-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4d24-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4d24-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4d24-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="d4d24-139">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4d24-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="d4d24-140">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="d4d24-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="d4d24-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4d24-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="d4d24-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4d24-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


