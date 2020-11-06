---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 792a76d024b34dd90fd8818303c61daafeb4f46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513052"
---
# <span data-ttu-id="bd9fe-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="bd9fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9fe-103">Importa dati da BLOB alla cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd9fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd9fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd9fe-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9fe-106">Il cmdlet **Import-AzureRmRedisCache** importa dati da BLOB nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="bd9fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9fe-108">Esempio 1: importare dati</span><span class="sxs-lookup"><span data-stu-id="bd9fe-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="bd9fe-109">Questo comando importa i dati dal blob specificato dall'URL SAS nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="bd9fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-110">PARAMETERS</span></span>

### <span data-ttu-id="bd9fe-111">-File</span><span class="sxs-lookup"><span data-stu-id="bd9fe-111">-Files</span></span>
<span data-ttu-id="bd9fe-112">Specifica gli URL SAS di BLOB di cui il contenuto questo cmdlet importa nella cache.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-112">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="bd9fe-113">Puoi generare gli URL SAS usando i comandi di PowerShell seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd9fe-113">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="bd9fe-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="bd9fe-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="bd9fe-115">$sasKeyForBlob = New-AzureStorageBlobSASToken-container "ContainerName"-blob "blobname"-autorizzazione "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-contesto $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="bd9fe-115">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="bd9fe-116">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-nome "CacheName"-file ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="bd9fe-116">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bd9fe-117">-Force</span></span>
<span data-ttu-id="bd9fe-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd9fe-119">-Format</span><span class="sxs-lookup"><span data-stu-id="bd9fe-119">-Format</span></span>
<span data-ttu-id="bd9fe-120">Specifica il formato del BLOB.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-120">Specifies the format of the blob.</span></span>
<span data-ttu-id="bd9fe-121">Attualmente RDB è l'unico formato supportato.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd9fe-122">-Name</span></span>
<span data-ttu-id="bd9fe-123">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-123">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd9fe-124">-PassThru</span></span>
<span data-ttu-id="bd9fe-125">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="bd9fe-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bd9fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd9fe-128">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-128">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd9fe-129">-Confirm</span></span>
<span data-ttu-id="bd9fe-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9fe-131">-WhatIf</span></span>
<span data-ttu-id="bd9fe-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9fe-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fe-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9fe-134">-DefaultProfile</span></span>
<span data-ttu-id="bd9fe-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd9fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9fe-136">CommonParameters</span></span>
<span data-ttu-id="bd9fe-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9fe-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd9fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9fe-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-139">INPUTS</span></span>

### <span data-ttu-id="bd9fe-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd9fe-140">None</span></span>
<span data-ttu-id="bd9fe-141">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="bd9fe-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bd9fe-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd9fe-142">OUTPUTS</span></span>

### <span data-ttu-id="bd9fe-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd9fe-143">None</span></span>

## <span data-ttu-id="bd9fe-144">Note</span><span class="sxs-lookup"><span data-stu-id="bd9fe-144">NOTES</span></span>
* <span data-ttu-id="bd9fe-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="bd9fe-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bd9fe-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd9fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="bd9fe-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="bd9fe-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="bd9fe-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="bd9fe-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="bd9fe-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bd9fe-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


