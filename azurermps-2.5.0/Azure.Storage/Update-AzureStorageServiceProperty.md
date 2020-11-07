---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: 2f0c59acba56fb80a12df0c5df6c8168ebc91000
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866917"
---
# <span data-ttu-id="438e1-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="438e1-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="438e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="438e1-102">SYNOPSIS</span></span>
<span data-ttu-id="438e1-103">Modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="438e1-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="438e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="438e1-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="438e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="438e1-105">DESCRIPTION</span></span>
<span data-ttu-id="438e1-106">Il cmdlet **Update-AzureStorageServiceProperty** modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="438e1-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="438e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="438e1-107">EXAMPLES</span></span>

### <span data-ttu-id="438e1-108">Esempio 1: impostare il servizio BLOB DefaultServiceVersion su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="438e1-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="438e1-109">Questo comando imposta il servizio DefaultServiceVersion di BLOB su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="438e1-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="438e1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="438e1-110">PARAMETERS</span></span>

### <span data-ttu-id="438e1-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="438e1-111">-Context</span></span>
<span data-ttu-id="438e1-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="438e1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="438e1-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="438e1-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="438e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438e1-114">-DefaultProfile</span></span>
<span data-ttu-id="438e1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="438e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="438e1-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="438e1-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="438e1-117">DefaultServiceVersion indica la versione predefinita da usare per le richieste al servizio BLOB se non è specificata la versione della richiesta in arrivo.</span><span class="sxs-lookup"><span data-stu-id="438e1-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="438e1-118">I valori possibili includono la versione 2008-10-27 e tutte le versioni più recenti.</span><span class="sxs-lookup"><span data-stu-id="438e1-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="438e1-119">Vedere altri dettagli in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="438e1-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438e1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="438e1-120">-PassThru</span></span>
<span data-ttu-id="438e1-121">Visualizza ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="438e1-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="438e1-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="438e1-122">-ServiceType</span></span>
<span data-ttu-id="438e1-123">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="438e1-123">Specifies the storage service type.</span></span>
<span data-ttu-id="438e1-124">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="438e1-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="438e1-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="438e1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="438e1-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="438e1-126">Blob</span></span> 
- <span data-ttu-id="438e1-127">tavolo</span><span class="sxs-lookup"><span data-stu-id="438e1-127">Table</span></span>
- <span data-ttu-id="438e1-128">Coda</span><span class="sxs-lookup"><span data-stu-id="438e1-128">Queue</span></span>
- <span data-ttu-id="438e1-129">File</span><span class="sxs-lookup"><span data-stu-id="438e1-129">File</span></span>

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

### <span data-ttu-id="438e1-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="438e1-130">-Confirm</span></span>
<span data-ttu-id="438e1-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="438e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="438e1-132">-WhatIf</span></span>
<span data-ttu-id="438e1-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="438e1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="438e1-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="438e1-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="438e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438e1-135">CommonParameters</span></span>
<span data-ttu-id="438e1-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438e1-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438e1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438e1-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="438e1-138">INPUTS</span></span>

### <span data-ttu-id="438e1-139">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="438e1-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="438e1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="438e1-140">OUTPUTS</span></span>

### <span data-ttu-id="438e1-141">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="438e1-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="438e1-142">Note</span><span class="sxs-lookup"><span data-stu-id="438e1-142">NOTES</span></span>

## <span data-ttu-id="438e1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="438e1-143">RELATED LINKS</span></span>
