---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: ec6abf13cf4f14a8d0cdaab75d5816d87f0540ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677522"
---
# <span data-ttu-id="af398-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="af398-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af398-102">SYNOPSIS</span></span>
<span data-ttu-id="af398-103">Esporta i dati dalla cache di Azure Redis in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="af398-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="af398-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af398-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af398-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af398-105">DESCRIPTION</span></span>
<span data-ttu-id="af398-106">Il cmdlet **Export-AzRedisCache** Esporta i dati dalla cache di Azure Redis in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="af398-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="af398-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af398-107">EXAMPLES</span></span>

### <span data-ttu-id="af398-108">Esempio 1: esportare i dati</span><span class="sxs-lookup"><span data-stu-id="af398-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="af398-109">Questo comando Esporta i dati da un'istanza della cache di Azure Redis nel contenitore specificato dall'URL SAS.</span><span class="sxs-lookup"><span data-stu-id="af398-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="af398-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af398-110">PARAMETERS</span></span>

### <span data-ttu-id="af398-111">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="af398-111">-Container</span></span>
<span data-ttu-id="af398-112">Specifica l'URL SAS del servizio container in cui questo cmdlet Esporta i dati.</span><span class="sxs-lookup"><span data-stu-id="af398-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="af398-113">Puoi generare un URL di Service SAS usando i comandi di PowerShell seguenti: $storageAccountContext = New-AzStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "ContainerName"-permission "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-context $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-nome "CacheName"-prefisso "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="af398-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="af398-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af398-114">-DefaultProfile</span></span>
<span data-ttu-id="af398-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af398-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af398-116">-Format</span><span class="sxs-lookup"><span data-stu-id="af398-116">-Format</span></span>
<span data-ttu-id="af398-117">Specifica un formato per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="af398-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="af398-118">Attualmente RDB è l'unico formato supportato.</span><span class="sxs-lookup"><span data-stu-id="af398-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="af398-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="af398-119">-Name</span></span>
<span data-ttu-id="af398-120">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="af398-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="af398-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af398-121">-PassThru</span></span>
<span data-ttu-id="af398-122">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="af398-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="af398-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="af398-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af398-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="af398-124">-Prefix</span></span>
<span data-ttu-id="af398-125">Specifica un prefisso da usare per i nomi BLOB.</span><span class="sxs-lookup"><span data-stu-id="af398-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="af398-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af398-126">-ResourceGroupName</span></span>
<span data-ttu-id="af398-127">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="af398-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="af398-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af398-128">-Confirm</span></span>
<span data-ttu-id="af398-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af398-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af398-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af398-130">-WhatIf</span></span>
<span data-ttu-id="af398-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af398-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af398-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af398-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af398-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af398-133">CommonParameters</span></span>
<span data-ttu-id="af398-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af398-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af398-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af398-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af398-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af398-136">INPUTS</span></span>

### <span data-ttu-id="af398-137">System. String</span><span class="sxs-lookup"><span data-stu-id="af398-137">System.String</span></span>

## <span data-ttu-id="af398-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af398-138">OUTPUTS</span></span>

### <span data-ttu-id="af398-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af398-139">System.Boolean</span></span>

## <span data-ttu-id="af398-140">Note</span><span class="sxs-lookup"><span data-stu-id="af398-140">NOTES</span></span>
* <span data-ttu-id="af398-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="af398-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="af398-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af398-142">RELATED LINKS</span></span>

[<span data-ttu-id="af398-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="af398-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="af398-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="af398-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="af398-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="af398-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

