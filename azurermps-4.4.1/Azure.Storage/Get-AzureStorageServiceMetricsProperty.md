---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508903"
---
# <span data-ttu-id="53df5-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="53df5-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="53df5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53df5-102">SYNOPSIS</span></span>
<span data-ttu-id="53df5-103">Ottiene le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53df5-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53df5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53df5-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="53df5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53df5-105">DESCRIPTION</span></span>
<span data-ttu-id="53df5-106">Il cmdlet **Get-AzureStorageServiceMetricsProperty** ottiene le proprietà metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53df5-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="53df5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53df5-107">EXAMPLES</span></span>

### <span data-ttu-id="53df5-108">Esempio 1: ottenere le proprietà metriche per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="53df5-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="53df5-109">Questo comando ottiene le proprietà metriche per l'archiviazione BLOB per il tipo di metriche per le ore.</span><span class="sxs-lookup"><span data-stu-id="53df5-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="53df5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53df5-110">PARAMETERS</span></span>

### <span data-ttu-id="53df5-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="53df5-111">-Context</span></span>
<span data-ttu-id="53df5-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53df5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53df5-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="53df5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="53df5-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="53df5-114">-MetricsType</span></span>
<span data-ttu-id="53df5-115">Specifica un tipo di metriche.</span><span class="sxs-lookup"><span data-stu-id="53df5-115">Specifies a metrics type.</span></span>
<span data-ttu-id="53df5-116">Questo cmdlet ottiene le proprietà metriche del servizio di archiviazione di Azure per il tipo di metriche specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="53df5-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="53df5-117">I valori accettabili per questo parametro sono: hour e minute.</span><span class="sxs-lookup"><span data-stu-id="53df5-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53df5-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="53df5-118">-ServiceType</span></span>
<span data-ttu-id="53df5-119">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="53df5-119">Specifies the storage service type.</span></span>
<span data-ttu-id="53df5-120">Questo cmdlet ottiene le proprietà metriche per il tipo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="53df5-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="53df5-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="53df5-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53df5-122">BLOB</span><span class="sxs-lookup"><span data-stu-id="53df5-122">Blob</span></span> 
- <span data-ttu-id="53df5-123">tavolo</span><span class="sxs-lookup"><span data-stu-id="53df5-123">Table</span></span>
- <span data-ttu-id="53df5-124">Coda</span><span class="sxs-lookup"><span data-stu-id="53df5-124">Queue</span></span>
- <span data-ttu-id="53df5-125">File</span><span class="sxs-lookup"><span data-stu-id="53df5-125">File</span></span> 

<span data-ttu-id="53df5-126">Il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="53df5-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="53df5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53df5-127">CommonParameters</span></span>
<span data-ttu-id="53df5-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53df5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53df5-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53df5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53df5-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53df5-130">INPUTS</span></span>

### <span data-ttu-id="53df5-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53df5-131">IStorageContext</span></span>

<span data-ttu-id="53df5-132">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="53df5-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="53df5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53df5-133">OUTPUTS</span></span>

### <span data-ttu-id="53df5-134">Microsoft. WindowsAzure. storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="53df5-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="53df5-135">Note</span><span class="sxs-lookup"><span data-stu-id="53df5-135">NOTES</span></span>

## <span data-ttu-id="53df5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53df5-136">RELATED LINKS</span></span>

[<span data-ttu-id="53df5-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="53df5-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="53df5-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="53df5-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


