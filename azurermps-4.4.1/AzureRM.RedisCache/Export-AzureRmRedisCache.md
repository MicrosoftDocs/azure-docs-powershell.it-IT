---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519988"
---
# <span data-ttu-id="4279e-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="4279e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4279e-102">SYNOPSIS</span></span>
<span data-ttu-id="4279e-103">Esporta i dati dalla cache di Azure Redis in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="4279e-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4279e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4279e-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4279e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4279e-105">DESCRIPTION</span></span>
<span data-ttu-id="4279e-106">Il cmdlet **Export-AzureRmRedisCache** Esporta i dati dalla cache di Azure Redis in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="4279e-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="4279e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4279e-107">EXAMPLES</span></span>

### <span data-ttu-id="4279e-108">Esempio 1: esportare i dati</span><span class="sxs-lookup"><span data-stu-id="4279e-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="4279e-109">Questo comando Esporta i dati da un'istanza della cache di Azure Redis nel contenitore specificato dall'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="4279e-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="4279e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4279e-110">PARAMETERS</span></span>

### <span data-ttu-id="4279e-111">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="4279e-111">-Container</span></span>
<span data-ttu-id="4279e-112">Specifica l'URL SAS del servizio container in cui questo cmdlet Esporta i dati.</span><span class="sxs-lookup"><span data-stu-id="4279e-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="4279e-113">Puoi generare un URL di Service SAS usando i comandi di PowerShell seguenti:</span><span class="sxs-lookup"><span data-stu-id="4279e-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="4279e-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="4279e-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="4279e-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-nome "ContainerName"-autorizzazione "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-contesto $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="4279e-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="4279e-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-nome "CacheName"-prefisso "blobprefix"-contenitore ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="4279e-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="4279e-117">-Format</span><span class="sxs-lookup"><span data-stu-id="4279e-117">-Format</span></span>
<span data-ttu-id="4279e-118">Specifica un formato per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="4279e-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="4279e-119">Attualmente RDB è l'unico formato supportato.</span><span class="sxs-lookup"><span data-stu-id="4279e-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="4279e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4279e-120">-Name</span></span>
<span data-ttu-id="4279e-121">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="4279e-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="4279e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4279e-122">-PassThru</span></span>
<span data-ttu-id="4279e-123">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4279e-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="4279e-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4279e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4279e-125">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="4279e-125">-Prefix</span></span>
<span data-ttu-id="4279e-126">Specifica un prefisso da usare per i nomi BLOB.</span><span class="sxs-lookup"><span data-stu-id="4279e-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="4279e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4279e-127">-ResourceGroupName</span></span>
<span data-ttu-id="4279e-128">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="4279e-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="4279e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4279e-129">-DefaultProfile</span></span>
<span data-ttu-id="4279e-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4279e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4279e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4279e-131">CommonParameters</span></span>
<span data-ttu-id="4279e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4279e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4279e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4279e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4279e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4279e-134">INPUTS</span></span>

### <span data-ttu-id="4279e-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4279e-135">None</span></span>
<span data-ttu-id="4279e-136">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="4279e-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4279e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4279e-137">OUTPUTS</span></span>

### <span data-ttu-id="4279e-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4279e-138">None</span></span>

## <span data-ttu-id="4279e-139">Note</span><span class="sxs-lookup"><span data-stu-id="4279e-139">NOTES</span></span>
* <span data-ttu-id="4279e-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="4279e-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="4279e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4279e-141">RELATED LINKS</span></span>

[<span data-ttu-id="4279e-142">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="4279e-143">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4279e-144">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="4279e-145">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="4279e-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4279e-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


