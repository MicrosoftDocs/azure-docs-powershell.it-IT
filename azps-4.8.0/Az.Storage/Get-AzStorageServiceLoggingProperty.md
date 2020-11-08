---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188739"
---
# <span data-ttu-id="571b3-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="571b3-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="571b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="571b3-102">SYNOPSIS</span></span>
<span data-ttu-id="571b3-103">Ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="571b3-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="571b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="571b3-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="571b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571b3-105">DESCRIPTION</span></span>
<span data-ttu-id="571b3-106">Il cmdlet **Get-AzStorageServiceLoggingProperty** ottiene le proprietà di registrazione per i servizi di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="571b3-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="571b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="571b3-107">EXAMPLES</span></span>

### <span data-ttu-id="571b3-108">Esempio 1: ottenere le proprietà di registrazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="571b3-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="571b3-109">Questo comando ottiene le proprietà di registrazione per l'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="571b3-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="571b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="571b3-110">PARAMETERS</span></span>

### <span data-ttu-id="571b3-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="571b3-111">-Context</span></span>
<span data-ttu-id="571b3-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="571b3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="571b3-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="571b3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="571b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571b3-114">-DefaultProfile</span></span>
<span data-ttu-id="571b3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="571b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="571b3-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="571b3-116">-ServiceType</span></span>
<span data-ttu-id="571b3-117">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="571b3-117">Specifies the storage service type.</span></span>
<span data-ttu-id="571b3-118">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="571b3-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="571b3-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="571b3-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="571b3-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="571b3-120">Blob</span></span> 
- <span data-ttu-id="571b3-121">tavolo</span><span class="sxs-lookup"><span data-stu-id="571b3-121">Table</span></span>
- <span data-ttu-id="571b3-122">Coda</span><span class="sxs-lookup"><span data-stu-id="571b3-122">Queue</span></span>
- <span data-ttu-id="571b3-123">File il valore di file non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="571b3-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="571b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571b3-124">CommonParameters</span></span>
<span data-ttu-id="571b3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571b3-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571b3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571b3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="571b3-127">INPUTS</span></span>

### <span data-ttu-id="571b3-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="571b3-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="571b3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="571b3-129">OUTPUTS</span></span>

### <span data-ttu-id="571b3-130">Microsoft. Azure. storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="571b3-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="571b3-131">Note</span><span class="sxs-lookup"><span data-stu-id="571b3-131">NOTES</span></span>

## <span data-ttu-id="571b3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="571b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="571b3-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="571b3-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="571b3-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="571b3-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


