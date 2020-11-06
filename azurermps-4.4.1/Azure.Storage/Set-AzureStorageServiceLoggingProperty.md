---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520831"
---
# <span data-ttu-id="99d79-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="99d79-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="99d79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99d79-102">SYNOPSIS</span></span>
<span data-ttu-id="99d79-103">Modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="99d79-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99d79-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="99d79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99d79-105">DESCRIPTION</span></span>
<span data-ttu-id="99d79-106">Il cmdlet **set-AzureStorageServiceLoggingProperty** modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="99d79-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="99d79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99d79-107">EXAMPLES</span></span>

### <span data-ttu-id="99d79-108">Esempio 1: modificare le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="99d79-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="99d79-109">Questo comando modifica la registrazione della versione 1,0 per l'archiviazione BLOB per includere le operazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="99d79-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="99d79-110">La registrazione del servizio di archiviazione di Azure mantiene le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="99d79-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="99d79-111">Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà di registrazione modificate.</span><span class="sxs-lookup"><span data-stu-id="99d79-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="99d79-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99d79-112">PARAMETERS</span></span>

### <span data-ttu-id="99d79-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="99d79-113">-Context</span></span>
<span data-ttu-id="99d79-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="99d79-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="99d79-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="99d79-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="99d79-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="99d79-116">-LoggingOperations</span></span>
<span data-ttu-id="99d79-117">Specifica una matrice di operazioni del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="99d79-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="99d79-118">Azure Storage Services registra le operazioni specificate da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="99d79-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="99d79-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="99d79-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99d79-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99d79-120">None</span></span>
- <span data-ttu-id="99d79-121">Leggere</span><span class="sxs-lookup"><span data-stu-id="99d79-121">Read</span></span>
- <span data-ttu-id="99d79-122">Scrivere</span><span class="sxs-lookup"><span data-stu-id="99d79-122">Write</span></span>
- <span data-ttu-id="99d79-123">Eliminare</span><span class="sxs-lookup"><span data-stu-id="99d79-123">Delete</span></span>
- <span data-ttu-id="99d79-124">Tutti</span><span class="sxs-lookup"><span data-stu-id="99d79-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d79-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99d79-125">-PassThru</span></span>
<span data-ttu-id="99d79-126">Indica che questo cmdlet restituisce le proprietà di registrazione aggiornate.</span><span class="sxs-lookup"><span data-stu-id="99d79-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="99d79-127">Se non specifichi questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="99d79-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="99d79-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="99d79-128">-RetentionDays</span></span>
<span data-ttu-id="99d79-129">Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="99d79-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d79-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="99d79-130">-ServiceType</span></span>
<span data-ttu-id="99d79-131">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99d79-131">Specifies the storage service type.</span></span>
<span data-ttu-id="99d79-132">Questo cmdlet modifica le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="99d79-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="99d79-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="99d79-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99d79-134">BLOB</span><span class="sxs-lookup"><span data-stu-id="99d79-134">Blob</span></span> 
- <span data-ttu-id="99d79-135">tavolo</span><span class="sxs-lookup"><span data-stu-id="99d79-135">Table</span></span>
- <span data-ttu-id="99d79-136">Coda</span><span class="sxs-lookup"><span data-stu-id="99d79-136">Queue</span></span>
- <span data-ttu-id="99d79-137">File</span><span class="sxs-lookup"><span data-stu-id="99d79-137">File</span></span>

<span data-ttu-id="99d79-138">Il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="99d79-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="99d79-139">-Versione</span><span class="sxs-lookup"><span data-stu-id="99d79-139">-Version</span></span>
<span data-ttu-id="99d79-140">Specifica la versione della registrazione del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="99d79-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="99d79-141">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="99d79-141">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d79-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d79-142">CommonParameters</span></span>
<span data-ttu-id="99d79-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d79-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d79-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d79-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d79-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99d79-145">INPUTS</span></span>

### <span data-ttu-id="99d79-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="99d79-146">IStorageContext</span></span>

<span data-ttu-id="99d79-147">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="99d79-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="99d79-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99d79-148">OUTPUTS</span></span>

### <span data-ttu-id="99d79-149">Microsoft. WindowsAzure. storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="99d79-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="99d79-150">Note</span><span class="sxs-lookup"><span data-stu-id="99d79-150">NOTES</span></span>

## <span data-ttu-id="99d79-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99d79-151">RELATED LINKS</span></span>

[<span data-ttu-id="99d79-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="99d79-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="99d79-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="99d79-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


