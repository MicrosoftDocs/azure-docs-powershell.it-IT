---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519951"
---
# <span data-ttu-id="97a8c-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="97a8c-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="97a8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="97a8c-103">Modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97a8c-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97a8c-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a8c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="97a8c-106">Il cmdlet **Update-AzureStorageServiceProperty** modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97a8c-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="97a8c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97a8c-107">EXAMPLES</span></span>

### <span data-ttu-id="97a8c-108">Esempio 1: impostare il servizio BLOB DefaultServiceVersion su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="97a8c-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="97a8c-109">Questo comando imposta il servizio DefaultServiceVersion di BLOB su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="97a8c-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="97a8c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97a8c-110">PARAMETERS</span></span>

### <span data-ttu-id="97a8c-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="97a8c-111">-Context</span></span>
<span data-ttu-id="97a8c-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97a8c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="97a8c-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="97a8c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="97a8c-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="97a8c-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="97a8c-115">DefaultServiceVersion indica la versione predefinita da usare per le richieste al servizio BLOB se non è specificata la versione della richiesta in arrivo.</span><span class="sxs-lookup"><span data-stu-id="97a8c-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="97a8c-116">I valori possibili includono la versione 2008-10-27 e tutte le versioni più recenti.</span><span class="sxs-lookup"><span data-stu-id="97a8c-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="97a8c-117">Vedere altri dettagli in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="97a8c-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a8c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97a8c-118">-PassThru</span></span>
<span data-ttu-id="97a8c-119">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="97a8c-119">Display ServiceProperties</span></span>

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

### <span data-ttu-id="97a8c-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="97a8c-120">-ServiceType</span></span>
<span data-ttu-id="97a8c-121">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="97a8c-121">Specifies the storage service type.</span></span>
<span data-ttu-id="97a8c-122">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="97a8c-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="97a8c-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="97a8c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97a8c-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="97a8c-124">Blob</span></span> 
- <span data-ttu-id="97a8c-125">tavolo</span><span class="sxs-lookup"><span data-stu-id="97a8c-125">Table</span></span>
- <span data-ttu-id="97a8c-126">Coda</span><span class="sxs-lookup"><span data-stu-id="97a8c-126">Queue</span></span>
- <span data-ttu-id="97a8c-127">File</span><span class="sxs-lookup"><span data-stu-id="97a8c-127">File</span></span>

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

### <span data-ttu-id="97a8c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97a8c-128">-Confirm</span></span>
<span data-ttu-id="97a8c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a8c-130">-WhatIf</span></span>
<span data-ttu-id="97a8c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97a8c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97a8c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97a8c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a8c-133">CommonParameters</span></span>
<span data-ttu-id="97a8c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a8c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a8c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97a8c-136">INPUTS</span></span>

### <span data-ttu-id="97a8c-137">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="97a8c-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="97a8c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97a8c-138">OUTPUTS</span></span>

### <span data-ttu-id="97a8c-139">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="97a8c-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="97a8c-140">Note</span><span class="sxs-lookup"><span data-stu-id="97a8c-140">NOTES</span></span>

## <span data-ttu-id="97a8c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97a8c-141">RELATED LINKS</span></span>

