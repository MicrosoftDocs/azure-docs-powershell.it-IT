---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197479"
---
# <span data-ttu-id="0c154-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0c154-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="0c154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c154-102">SYNOPSIS</span></span>
<span data-ttu-id="0c154-103">Modifica le proprietà del servizio per il servizio BLOB archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c154-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0c154-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c154-104">SYNTAX</span></span>

### <span data-ttu-id="0c154-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c154-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c154-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0c154-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c154-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="0c154-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c154-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c154-108">DESCRIPTION</span></span>
<span data-ttu-id="0c154-109">Il cmdlet **Update-AzStorageBlobServiceProperty** modifica le proprietà del servizio per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c154-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0c154-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c154-110">EXAMPLES</span></span>

### <span data-ttu-id="0c154-111">Esempio 1: Impostare DefaultServiceVersion del servizio BLOB su 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="0c154-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="0c154-112">Questo comando imposta DefaultServiceVersion di Servizio BLOB su 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="0c154-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="0c154-113">Esempio 2: Abilitare il changefeed nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0c154-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="0c154-114">Questo comando abilita Changefeed nel servizio BLOB di un feed Di modifica dell'account di archiviazione in Archiviazione BLOB di Azure e funziona ascoltando un account GPv2 o Di archiviazione BLOB per qualsiasi evento di creazione, modifica o eliminazione a livello di BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c154-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="0c154-115">Restituisce quindi un log ordinato degli eventi per i BLOB archiviati nel contenitore $blobchangefeed all'interno dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c154-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="0c154-116">Le modifiche serializzate vengono mantenute come file Apache Avro e possono essere elaborate in modo asincrono e incrementale.</span><span class="sxs-lookup"><span data-stu-id="0c154-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="0c154-117">Esempio 3: Abilitare il controllo delle versioni nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0c154-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="0c154-118">Questo comando abilita il controllo delle versioni nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0c154-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="0c154-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c154-119">PARAMETERS</span></span>

### <span data-ttu-id="0c154-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c154-120">-DefaultProfile</span></span>
<span data-ttu-id="0c154-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c154-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="0c154-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="0c154-123">Versione del servizio predefinita da impostare</span><span class="sxs-lookup"><span data-stu-id="0c154-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="0c154-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="0c154-124">-EnableChangeFeed</span></span>
<span data-ttu-id="0c154-125">Abilitare la registrazione dei feed di modifica per l'account di archiviazione impostandola su $true, disabilitare la registrazione dei feed di modifica impostandola su $false.</span><span class="sxs-lookup"><span data-stu-id="0c154-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="0c154-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="0c154-127">Ottiene o imposta il controllo delle versioni abilitato se impostato su true.</span><span class="sxs-lookup"><span data-stu-id="0c154-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c154-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c154-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c154-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c154-130">-ResourceId</span></span>
<span data-ttu-id="0c154-131">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c154-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0c154-132">-StorageAccount</span></span>
<span data-ttu-id="0c154-133">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0c154-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0c154-134">-StorageAccountName</span></span>
<span data-ttu-id="0c154-135">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c154-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c154-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c154-136">-Confirm</span></span>
<span data-ttu-id="0c154-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c154-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c154-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c154-138">-WhatIf</span></span>
<span data-ttu-id="0c154-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c154-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c154-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c154-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c154-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c154-141">CommonParameters</span></span>
<span data-ttu-id="0c154-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c154-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c154-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c154-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c154-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c154-144">INPUTS</span></span>

### <span data-ttu-id="0c154-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0c154-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0c154-146">System.String</span><span class="sxs-lookup"><span data-stu-id="0c154-146">System.String</span></span>

## <span data-ttu-id="0c154-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c154-147">OUTPUTS</span></span>

### <span data-ttu-id="0c154-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="0c154-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="0c154-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c154-149">NOTES</span></span>

## <span data-ttu-id="0c154-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c154-150">RELATED LINKS</span></span>
