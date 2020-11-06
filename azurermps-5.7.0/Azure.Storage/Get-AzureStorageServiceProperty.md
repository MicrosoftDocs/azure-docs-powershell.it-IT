---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515907"
---
# <span data-ttu-id="fc420-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fc420-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="fc420-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc420-102">SYNOPSIS</span></span>
<span data-ttu-id="fc420-103">Ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc420-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc420-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc420-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc420-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc420-105">DESCRIPTION</span></span>
<span data-ttu-id="fc420-106">Il cmdlet **Get-AzureStorageServiceProperty** ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc420-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="fc420-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc420-107">EXAMPLES</span></span>

### <span data-ttu-id="fc420-108">Esempio 1: ottenere la proprietà servizi di archiviazione di Azure del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="fc420-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="fc420-109">Questo comando ottiene la proprietà DefaultServiceVersion del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="fc420-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="fc420-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc420-110">PARAMETERS</span></span>

### <span data-ttu-id="fc420-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fc420-111">-Context</span></span>
<span data-ttu-id="fc420-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc420-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fc420-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fc420-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fc420-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fc420-114">-ServiceType</span></span>
<span data-ttu-id="fc420-115">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fc420-115">Specifies the storage service type.</span></span>
<span data-ttu-id="fc420-116">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fc420-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="fc420-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc420-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc420-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="fc420-118">Blob</span></span> 
- <span data-ttu-id="fc420-119">tavolo</span><span class="sxs-lookup"><span data-stu-id="fc420-119">Table</span></span>
- <span data-ttu-id="fc420-120">Coda</span><span class="sxs-lookup"><span data-stu-id="fc420-120">Queue</span></span>
- <span data-ttu-id="fc420-121">File</span><span class="sxs-lookup"><span data-stu-id="fc420-121">File</span></span>

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

### <span data-ttu-id="fc420-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc420-122">CommonParameters</span></span>
<span data-ttu-id="fc420-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc420-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc420-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc420-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc420-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc420-125">INPUTS</span></span>

### <span data-ttu-id="fc420-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc420-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fc420-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc420-127">OUTPUTS</span></span>

### <span data-ttu-id="fc420-128">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="fc420-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="fc420-129">Note</span><span class="sxs-lookup"><span data-stu-id="fc420-129">NOTES</span></span>

## <span data-ttu-id="fc420-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc420-130">RELATED LINKS</span></span>

