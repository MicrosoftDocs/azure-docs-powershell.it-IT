---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188717"
---
# <span data-ttu-id="b6fc8-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b6fc8-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="b6fc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fc8-103">Modifica le proprietà del servizio per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b6fc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6fc8-104">SYNTAX</span></span>

### <span data-ttu-id="b6fc8-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6fc8-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6fc8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b6fc8-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6fc8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b6fc8-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6fc8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6fc8-108">DESCRIPTION</span></span>
<span data-ttu-id="b6fc8-109">Il cmdlet **Update-AzStorageBlobServiceProperty** modifica le proprietà del servizio per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b6fc8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="b6fc8-111">Esempio 1: impostare il servizio BLOB DefaultServiceVersion su 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="b6fc8-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="b6fc8-112">Questo comando imposta il servizio DefaultServiceVersion di BLOB su 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="b6fc8-113">Esempio 2: abilitare changefeed nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b6fc8-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b6fc8-114">Questo comando consente a changefeed su Blob Service di un account di archiviazione il supporto per la modifica del feed in Azure BLOB Storage funziona ascoltando un account di archiviazione di GPv2 o BLOB per eventuali eventi di creazione, modifica o eliminazione a livello di BLOB.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="b6fc8-115">Viene quindi restituito un log ordinato di eventi per i BLOB archiviati nel contenitore $blobchangefeed all'interno dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="b6fc8-116">Le modifiche serializzate vengono rese persistenti come file avro di Apache e possono essere elaborate in modo asincrono e incrementale.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="b6fc8-117">Esempio 3: abilitare il controllo delle versioni nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b6fc8-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b6fc8-118">Questo comando consente di abilitare il controllo delle versioni nel servizio BLOB di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b6fc8-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="b6fc8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6fc8-119">PARAMETERS</span></span>

### <span data-ttu-id="b6fc8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fc8-120">-DefaultProfile</span></span>
<span data-ttu-id="b6fc8-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6fc8-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="b6fc8-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="b6fc8-123">Versione predefinita del servizio da impostare</span><span class="sxs-lookup"><span data-stu-id="b6fc8-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="b6fc8-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="b6fc8-124">-EnableChangeFeed</span></span>
<span data-ttu-id="b6fc8-125">Abilitare la registrazione della modifica del feed per l'account di archiviazione impostando su $true, disabilitare la registrazione del feed di modifica impostando su $false.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="b6fc8-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="b6fc8-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="b6fc8-127">Ottiene o imposta il controllo delle versioni è abilitato se impostato su true.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="b6fc8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6fc8-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6fc8-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6fc8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6fc8-130">-ResourceId</span></span>
<span data-ttu-id="b6fc8-131">Immettere un ID risorsa dell'account di archiviazione o un ID risorsa delle proprietà del servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b6fc8-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6fc8-132">-StorageAccount</span></span>
<span data-ttu-id="b6fc8-133">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b6fc8-133">Storage account object</span></span>

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

### <span data-ttu-id="b6fc8-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6fc8-134">-StorageAccountName</span></span>
<span data-ttu-id="b6fc8-135">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="b6fc8-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6fc8-136">-Confirm</span></span>
<span data-ttu-id="b6fc8-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6fc8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fc8-138">-WhatIf</span></span>
<span data-ttu-id="b6fc8-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fc8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6fc8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fc8-141">CommonParameters</span></span>
<span data-ttu-id="b6fc8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6fc8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fc8-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fc8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fc8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6fc8-144">INPUTS</span></span>

### <span data-ttu-id="b6fc8-145">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6fc8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b6fc8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b6fc8-146">System.String</span></span>

## <span data-ttu-id="b6fc8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6fc8-147">OUTPUTS</span></span>

### <span data-ttu-id="b6fc8-148">Microsoft. Azure. Commands. Management. storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b6fc8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="b6fc8-149">Note</span><span class="sxs-lookup"><span data-stu-id="b6fc8-149">NOTES</span></span>

## <span data-ttu-id="b6fc8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6fc8-150">RELATED LINKS</span></span>
