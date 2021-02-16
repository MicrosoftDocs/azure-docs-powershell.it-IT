---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197455"
---
# <span data-ttu-id="bb857-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bb857-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="bb857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb857-102">SYNOPSIS</span></span>
<span data-ttu-id="bb857-103">Modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb857-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bb857-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb857-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb857-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb857-105">DESCRIPTION</span></span>
<span data-ttu-id="bb857-106">Il cmdlet **Update-AzStorageServiceProperty** modifica le proprietà per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb857-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bb857-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb857-107">EXAMPLES</span></span>

### <span data-ttu-id="bb857-108">Esempio 1: Impostare DefaultServiceVersion del servizio BLOB su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="bb857-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="bb857-109">Questo comando imposta DefaultServiceVersion del servizio BLOB su 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="bb857-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="bb857-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb857-110">PARAMETERS</span></span>

### <span data-ttu-id="bb857-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bb857-111">-Context</span></span>
<span data-ttu-id="bb857-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb857-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bb857-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb857-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb857-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb857-114">-DefaultProfile</span></span>
<span data-ttu-id="bb857-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb857-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb857-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="bb857-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="bb857-117">DefaultServiceVersion indica la versione predefinita da usare per le richieste al servizio BLOB se non è specificata la versione di una richiesta in arrivo.</span><span class="sxs-lookup"><span data-stu-id="bb857-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="bb857-118">I valori possibili includono la versione 2008-10-27 e tutte le versioni più recenti.</span><span class="sxs-lookup"><span data-stu-id="bb857-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="bb857-119">Vedi altri dettagli in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="bb857-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="bb857-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb857-120">-PassThru</span></span>
<span data-ttu-id="bb857-121">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bb857-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="bb857-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bb857-122">-ServiceType</span></span>
<span data-ttu-id="bb857-123">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb857-123">Specifies the storage service type.</span></span>
<span data-ttu-id="bb857-124">Questo cmdlet ottiene le proprietà di registrazione per il tipo di servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bb857-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bb857-125">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="bb857-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb857-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="bb857-126">Blob</span></span> 
- <span data-ttu-id="bb857-127">tavolo</span><span class="sxs-lookup"><span data-stu-id="bb857-127">Table</span></span>
- <span data-ttu-id="bb857-128">Coda</span><span class="sxs-lookup"><span data-stu-id="bb857-128">Queue</span></span>
- <span data-ttu-id="bb857-129">File</span><span class="sxs-lookup"><span data-stu-id="bb857-129">File</span></span>

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

### <span data-ttu-id="bb857-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb857-130">-Confirm</span></span>
<span data-ttu-id="bb857-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb857-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb857-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb857-132">-WhatIf</span></span>
<span data-ttu-id="bb857-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb857-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb857-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb857-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb857-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb857-135">CommonParameters</span></span>
<span data-ttu-id="bb857-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb857-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb857-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb857-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb857-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb857-138">INPUTS</span></span>

### <span data-ttu-id="bb857-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bb857-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bb857-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb857-140">OUTPUTS</span></span>

### <span data-ttu-id="bb857-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="bb857-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="bb857-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb857-142">NOTES</span></span>

## <span data-ttu-id="bb857-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb857-143">RELATED LINKS</span></span>
