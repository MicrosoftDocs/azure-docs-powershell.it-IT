---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: d0edbcc3b519f9600a2ad36832dee0305ce49be7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512771"
---
# <span data-ttu-id="96867-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="96867-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="96867-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96867-102">SYNOPSIS</span></span>
<span data-ttu-id="96867-103">Ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96867-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96867-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96867-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="96867-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96867-105">DESCRIPTION</span></span>
<span data-ttu-id="96867-106">Il cmdlet **Get-AzureStorageServiceLoggingProperty** ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96867-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="96867-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96867-107">EXAMPLES</span></span>

### <span data-ttu-id="96867-108">Esempio 1: ottenere le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="96867-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="96867-109">Questo comando ottiene le proprietà di registrazione per l'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="96867-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="96867-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96867-110">PARAMETERS</span></span>

### <span data-ttu-id="96867-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="96867-111">-Context</span></span>
<span data-ttu-id="96867-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="96867-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96867-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="96867-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="96867-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="96867-114">-ServiceType</span></span>
<span data-ttu-id="96867-115">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96867-115">Specifies the storage service type.</span></span>
<span data-ttu-id="96867-116">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="96867-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="96867-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="96867-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96867-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="96867-118">Blob</span></span> 
- <span data-ttu-id="96867-119">tavolo</span><span class="sxs-lookup"><span data-stu-id="96867-119">Table</span></span>
- <span data-ttu-id="96867-120">Coda</span><span class="sxs-lookup"><span data-stu-id="96867-120">Queue</span></span>
- <span data-ttu-id="96867-121">File</span><span class="sxs-lookup"><span data-stu-id="96867-121">File</span></span>

<span data-ttu-id="96867-122">Il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="96867-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="96867-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96867-123">CommonParameters</span></span>
<span data-ttu-id="96867-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96867-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96867-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96867-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96867-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96867-126">INPUTS</span></span>

### <span data-ttu-id="96867-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96867-127">IStorageContext</span></span>

<span data-ttu-id="96867-128">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="96867-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="96867-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96867-129">OUTPUTS</span></span>

### <span data-ttu-id="96867-130">Microsoft. WindowsAzure. storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="96867-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="96867-131">Note</span><span class="sxs-lookup"><span data-stu-id="96867-131">NOTES</span></span>

## <span data-ttu-id="96867-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96867-132">RELATED LINKS</span></span>

[<span data-ttu-id="96867-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="96867-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="96867-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="96867-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


