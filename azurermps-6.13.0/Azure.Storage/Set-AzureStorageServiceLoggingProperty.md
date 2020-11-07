---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fb526bbd33e30e4ea125e9662926c7ea4c7bbb00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517747"
---
# <span data-ttu-id="e578d-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e578d-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e578d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e578d-102">SYNOPSIS</span></span>
<span data-ttu-id="e578d-103">Modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e578d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e578d-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e578d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e578d-105">DESCRIPTION</span></span>
<span data-ttu-id="e578d-106">Il cmdlet **set-AzureStorageServiceLoggingProperty** modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="e578d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e578d-107">EXAMPLES</span></span>

### <span data-ttu-id="e578d-108">Esempio 1: modificare le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="e578d-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="e578d-109">Questo comando modifica la registrazione della versione 1,0 per l'archiviazione BLOB per includere le operazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="e578d-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="e578d-110">La registrazione del servizio di archiviazione di Azure mantiene le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="e578d-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="e578d-111">Poiché questo comando specifica il parametro *PassThru* , il comando Visualizza le proprietà di registrazione modificate.</span><span class="sxs-lookup"><span data-stu-id="e578d-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="e578d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e578d-112">PARAMETERS</span></span>

### <span data-ttu-id="e578d-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e578d-113">-Context</span></span>
<span data-ttu-id="e578d-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e578d-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e578d-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e578d-116">-DefaultProfile</span></span>
<span data-ttu-id="e578d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="e578d-118">-LoggingOperations</span></span>
<span data-ttu-id="e578d-119">Specifica una matrice di operazioni del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="e578d-120">Azure Storage Services registra le operazioni specificate da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e578d-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="e578d-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e578d-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e578d-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e578d-122">None</span></span>
- <span data-ttu-id="e578d-123">Leggere</span><span class="sxs-lookup"><span data-stu-id="e578d-123">Read</span></span>
- <span data-ttu-id="e578d-124">Scrivere</span><span class="sxs-lookup"><span data-stu-id="e578d-124">Write</span></span>
- <span data-ttu-id="e578d-125">Eliminare</span><span class="sxs-lookup"><span data-stu-id="e578d-125">Delete</span></span>
- <span data-ttu-id="e578d-126">Tutti</span><span class="sxs-lookup"><span data-stu-id="e578d-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e578d-127">-PassThru</span></span>
<span data-ttu-id="e578d-128">Indica che questo cmdlet restituisce le proprietà di registrazione aggiornate.</span><span class="sxs-lookup"><span data-stu-id="e578d-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="e578d-129">Se non specifichi questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e578d-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="e578d-130">-RetentionDays</span></span>
<span data-ttu-id="e578d-131">Specifica il numero di giorni in cui il servizio di archiviazione di Azure mantiene le informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="e578d-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e578d-132">-ServiceType</span></span>
<span data-ttu-id="e578d-133">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e578d-133">Specifies the storage service type.</span></span>
<span data-ttu-id="e578d-134">Questo cmdlet modifica le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e578d-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e578d-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e578d-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e578d-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="e578d-136">Blob</span></span> 
- <span data-ttu-id="e578d-137">tavolo</span><span class="sxs-lookup"><span data-stu-id="e578d-137">Table</span></span>
- <span data-ttu-id="e578d-138">Coda</span><span class="sxs-lookup"><span data-stu-id="e578d-138">Queue</span></span>
- <span data-ttu-id="e578d-139">File il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="e578d-139">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-140">-Versione</span><span class="sxs-lookup"><span data-stu-id="e578d-140">-Version</span></span>
<span data-ttu-id="e578d-141">Specifica la versione della registrazione del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="e578d-142">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="e578d-142">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e578d-143">CommonParameters</span></span>
<span data-ttu-id="e578d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e578d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e578d-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e578d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e578d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e578d-146">INPUTS</span></span>

### <span data-ttu-id="e578d-147">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e578d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e578d-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e578d-148">OUTPUTS</span></span>

### <span data-ttu-id="e578d-149">Microsoft. WindowsAzure. storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="e578d-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e578d-150">Note</span><span class="sxs-lookup"><span data-stu-id="e578d-150">NOTES</span></span>

## <span data-ttu-id="e578d-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e578d-151">RELATED LINKS</span></span>

[<span data-ttu-id="e578d-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e578d-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="e578d-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e578d-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

