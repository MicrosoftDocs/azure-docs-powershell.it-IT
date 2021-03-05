---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 84eae2221564d1c1a569ea5469c44cb1cd628b04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974141"
---
# <span data-ttu-id="8877b-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8877b-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="8877b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8877b-102">SYNOPSIS</span></span>
<span data-ttu-id="8877b-103">Modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="8877b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8877b-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8877b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8877b-105">DESCRIPTION</span></span>
<span data-ttu-id="8877b-106">Il cmdlet **Set-AzStorageServiceLoggingProperty** modifica la registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="8877b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8877b-107">EXAMPLES</span></span>

### <span data-ttu-id="8877b-108">Esempio 1: Modificare le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="8877b-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="8877b-109">Questo comando modifica la registrazione della versione 1.0 per l'archiviazione BLOB in modo da includere operazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="8877b-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="8877b-110">La registrazione del servizio di archiviazione di Azure conserva le voci per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="8877b-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="8877b-111">Poiché questo comando specifica il *parametro PassThru,* il comando visualizza le proprietà di registrazione modificate.</span><span class="sxs-lookup"><span data-stu-id="8877b-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="8877b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8877b-112">PARAMETERS</span></span>

### <span data-ttu-id="8877b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8877b-113">-Context</span></span>
<span data-ttu-id="8877b-114">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8877b-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8877b-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8877b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8877b-116">-DefaultProfile</span></span>
<span data-ttu-id="8877b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8877b-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="8877b-118">-LoggingOperations</span></span>
<span data-ttu-id="8877b-119">Specifica una matrice di operazioni del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="8877b-120">I servizi di archiviazione di Azure registrano le operazioni specificate da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8877b-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="8877b-121">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="8877b-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8877b-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8877b-122">None</span></span>
- <span data-ttu-id="8877b-123">Lettura</span><span class="sxs-lookup"><span data-stu-id="8877b-123">Read</span></span>
- <span data-ttu-id="8877b-124">Scrivere</span><span class="sxs-lookup"><span data-stu-id="8877b-124">Write</span></span>
- <span data-ttu-id="8877b-125">Elimina</span><span class="sxs-lookup"><span data-stu-id="8877b-125">Delete</span></span>
- <span data-ttu-id="8877b-126">Tutti</span><span class="sxs-lookup"><span data-stu-id="8877b-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8877b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8877b-127">-PassThru</span></span>
<span data-ttu-id="8877b-128">Indica che questo cmdlet restituisce le proprietà di registrazione aggiornate.</span><span class="sxs-lookup"><span data-stu-id="8877b-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="8877b-129">Se non si specifica questo parametro, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8877b-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8877b-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8877b-130">-RetentionDays</span></span>
<span data-ttu-id="8877b-131">Specifica il numero di giorni per cui il servizio di archiviazione di Azure conserva le informazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="8877b-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="8877b-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8877b-132">-ServiceType</span></span>
<span data-ttu-id="8877b-133">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8877b-133">Specifies the storage service type.</span></span>
<span data-ttu-id="8877b-134">Questo cmdlet modifica le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8877b-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="8877b-135">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="8877b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8877b-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="8877b-136">Blob</span></span> 
- <span data-ttu-id="8877b-137">tavolo</span><span class="sxs-lookup"><span data-stu-id="8877b-137">Table</span></span>
- <span data-ttu-id="8877b-138">Coda</span><span class="sxs-lookup"><span data-stu-id="8877b-138">Queue</span></span>
- <span data-ttu-id="8877b-139">File Il valore di File non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="8877b-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="8877b-140">-Version</span><span class="sxs-lookup"><span data-stu-id="8877b-140">-Version</span></span>
<span data-ttu-id="8877b-141">Specifica la versione della registrazione del servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8877b-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="8877b-142">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="8877b-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="8877b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8877b-143">CommonParameters</span></span>
<span data-ttu-id="8877b-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8877b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8877b-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8877b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8877b-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="8877b-146">INPUTS</span></span>

### <span data-ttu-id="8877b-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8877b-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8877b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8877b-148">OUTPUTS</span></span>

### <span data-ttu-id="8877b-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="8877b-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="8877b-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="8877b-150">NOTES</span></span>

## <span data-ttu-id="8877b-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8877b-151">RELATED LINKS</span></span>

[<span data-ttu-id="8877b-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8877b-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="8877b-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8877b-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


