---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033635"
---
# <span data-ttu-id="bdaff-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bdaff-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="bdaff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdaff-102">SYNOPSIS</span></span>
<span data-ttu-id="bdaff-103">Ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bdaff-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="bdaff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdaff-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdaff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdaff-105">DESCRIPTION</span></span>
<span data-ttu-id="bdaff-106">Il cmdlet **Get-AzStorageServiceProperty** ottiene le proprietà per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bdaff-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="bdaff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdaff-107">EXAMPLES</span></span>

### <span data-ttu-id="bdaff-108">Esempio 1: ottenere la proprietà servizi di archiviazione di Azure del servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="bdaff-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="bdaff-109">Questo comando ottiene la proprietà DefaultServiceVersion del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="bdaff-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="bdaff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdaff-110">PARAMETERS</span></span>

### <span data-ttu-id="bdaff-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bdaff-111">-Context</span></span>
<span data-ttu-id="bdaff-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bdaff-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bdaff-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bdaff-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bdaff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdaff-114">-DefaultProfile</span></span>
<span data-ttu-id="bdaff-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdaff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdaff-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bdaff-116">-ServiceType</span></span>
<span data-ttu-id="bdaff-117">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bdaff-117">Specifies the storage service type.</span></span>
<span data-ttu-id="bdaff-118">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bdaff-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bdaff-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdaff-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bdaff-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="bdaff-120">Blob</span></span> 
- <span data-ttu-id="bdaff-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="bdaff-121">Table</span></span>
- <span data-ttu-id="bdaff-122">Coda</span><span class="sxs-lookup"><span data-stu-id="bdaff-122">Queue</span></span>
- <span data-ttu-id="bdaff-123">File</span><span class="sxs-lookup"><span data-stu-id="bdaff-123">File</span></span>

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

### <span data-ttu-id="bdaff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdaff-124">CommonParameters</span></span>
<span data-ttu-id="bdaff-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdaff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdaff-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdaff-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdaff-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdaff-127">INPUTS</span></span>

### <span data-ttu-id="bdaff-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdaff-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bdaff-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdaff-129">OUTPUTS</span></span>

### <span data-ttu-id="bdaff-130">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="bdaff-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="bdaff-131">Note</span><span class="sxs-lookup"><span data-stu-id="bdaff-131">NOTES</span></span>

## <span data-ttu-id="bdaff-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdaff-132">RELATED LINKS</span></span>
