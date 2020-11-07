---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865971"
---
# <span data-ttu-id="3c684-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3c684-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="3c684-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c684-102">SYNOPSIS</span></span>
<span data-ttu-id="3c684-103">Ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c684-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c684-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c684-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c684-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c684-105">DESCRIPTION</span></span>
<span data-ttu-id="3c684-106">Il cmdlet **Get-AzureStorageServiceLoggingProperty** ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c684-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="3c684-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c684-107">EXAMPLES</span></span>

### <span data-ttu-id="3c684-108">Esempio 1: ottenere le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="3c684-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="3c684-109">Questo comando ottiene le proprietà di registrazione per l'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="3c684-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="3c684-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c684-110">PARAMETERS</span></span>

### <span data-ttu-id="3c684-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3c684-111">-Context</span></span>
<span data-ttu-id="3c684-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c684-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3c684-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3c684-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3c684-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c684-114">-DefaultProfile</span></span>
<span data-ttu-id="3c684-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c684-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c684-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3c684-116">-ServiceType</span></span>
<span data-ttu-id="3c684-117">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3c684-117">Specifies the storage service type.</span></span>
<span data-ttu-id="3c684-118">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3c684-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="3c684-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c684-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3c684-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="3c684-120">Blob</span></span> 
- <span data-ttu-id="3c684-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="3c684-121">Table</span></span>
- <span data-ttu-id="3c684-122">Coda</span><span class="sxs-lookup"><span data-stu-id="3c684-122">Queue</span></span>
- <span data-ttu-id="3c684-123">File il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="3c684-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="3c684-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c684-124">CommonParameters</span></span>
<span data-ttu-id="3c684-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c684-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c684-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c684-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c684-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c684-127">INPUTS</span></span>

### <span data-ttu-id="3c684-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c684-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3c684-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c684-129">OUTPUTS</span></span>

### <span data-ttu-id="3c684-130">Microsoft. WindowsAzure. storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="3c684-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="3c684-131">Note</span><span class="sxs-lookup"><span data-stu-id="3c684-131">NOTES</span></span>

## <span data-ttu-id="3c684-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c684-132">RELATED LINKS</span></span>

[<span data-ttu-id="3c684-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c684-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3c684-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3c684-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


