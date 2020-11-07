---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: adb671b81dd26c1fa66ea98f98dddf8fffbb5356
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865968"
---
# <span data-ttu-id="6f597-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6f597-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="6f597-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f597-102">SYNOPSIS</span></span>
<span data-ttu-id="6f597-103">Ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f597-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f597-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f597-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f597-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f597-105">DESCRIPTION</span></span>
<span data-ttu-id="6f597-106">Il cmdlet **Get-AzureStorageServiceProperty** ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f597-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="6f597-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f597-107">EXAMPLES</span></span>

### <span data-ttu-id="6f597-108">Esempio 1: ottenere la proprietà servizi di archiviazione di Azure del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="6f597-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="6f597-109">Questo comando ottiene la proprietà DefaultServiceVersion del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="6f597-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="6f597-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f597-110">PARAMETERS</span></span>

### <span data-ttu-id="6f597-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6f597-111">-Context</span></span>
<span data-ttu-id="6f597-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f597-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6f597-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6f597-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6f597-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f597-114">-DefaultProfile</span></span>
<span data-ttu-id="6f597-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f597-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f597-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6f597-116">-ServiceType</span></span>
<span data-ttu-id="6f597-117">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6f597-117">Specifies the storage service type.</span></span>
<span data-ttu-id="6f597-118">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6f597-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6f597-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f597-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f597-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="6f597-120">Blob</span></span> 
- <span data-ttu-id="6f597-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="6f597-121">Table</span></span>
- <span data-ttu-id="6f597-122">Coda</span><span class="sxs-lookup"><span data-stu-id="6f597-122">Queue</span></span>
- <span data-ttu-id="6f597-123">File</span><span class="sxs-lookup"><span data-stu-id="6f597-123">File</span></span>

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

### <span data-ttu-id="6f597-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f597-124">CommonParameters</span></span>
<span data-ttu-id="6f597-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f597-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f597-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f597-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f597-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f597-127">INPUTS</span></span>

### <span data-ttu-id="6f597-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f597-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6f597-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f597-129">OUTPUTS</span></span>

### <span data-ttu-id="6f597-130">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="6f597-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="6f597-131">Note</span><span class="sxs-lookup"><span data-stu-id="6f597-131">NOTES</span></span>

## <span data-ttu-id="6f597-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f597-132">RELATED LINKS</span></span>
