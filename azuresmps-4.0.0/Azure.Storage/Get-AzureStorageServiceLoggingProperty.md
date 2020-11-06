---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507052"
---
# <span data-ttu-id="12a6f-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="12a6f-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="12a6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="12a6f-103">Ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="12a6f-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="12a6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12a6f-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="12a6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="12a6f-106">Il cmdlet **Get-AzureStorageServiceLoggingProperty** ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="12a6f-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="12a6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12a6f-107">EXAMPLES</span></span>

### <span data-ttu-id="12a6f-108">Esempio 1: ottenere le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="12a6f-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="12a6f-109">Questo comando ottiene le proprietà di registrazione per l'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="12a6f-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="12a6f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12a6f-110">PARAMETERS</span></span>

### <span data-ttu-id="12a6f-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="12a6f-111">-Context</span></span>
<span data-ttu-id="12a6f-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="12a6f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="12a6f-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="12a6f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a6f-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="12a6f-114">-ServiceType</span></span>
<span data-ttu-id="12a6f-115">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="12a6f-115">Specifies the storage service type.</span></span>
<span data-ttu-id="12a6f-116">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="12a6f-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="12a6f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="12a6f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12a6f-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="12a6f-118">Blob</span></span> 
- <span data-ttu-id="12a6f-119">tavolo</span><span class="sxs-lookup"><span data-stu-id="12a6f-119">Table</span></span>
- <span data-ttu-id="12a6f-120">Coda</span><span class="sxs-lookup"><span data-stu-id="12a6f-120">Queue</span></span>
- <span data-ttu-id="12a6f-121">File</span><span class="sxs-lookup"><span data-stu-id="12a6f-121">File</span></span>

<span data-ttu-id="12a6f-122">Il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="12a6f-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a6f-123">CommonParameters</span></span>
<span data-ttu-id="12a6f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a6f-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a6f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a6f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12a6f-126">INPUTS</span></span>

## <span data-ttu-id="12a6f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12a6f-127">OUTPUTS</span></span>

## <span data-ttu-id="12a6f-128">Note</span><span class="sxs-lookup"><span data-stu-id="12a6f-128">NOTES</span></span>

## <span data-ttu-id="12a6f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12a6f-129">RELATED LINKS</span></span>

[<span data-ttu-id="12a6f-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="12a6f-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="12a6f-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="12a6f-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


