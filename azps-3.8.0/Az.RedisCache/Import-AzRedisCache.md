---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021529"
---
# <span data-ttu-id="34bac-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="34bac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34bac-102">SYNOPSIS</span></span>
<span data-ttu-id="34bac-103">Importa dati da BLOB alla cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="34bac-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="34bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34bac-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34bac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34bac-105">DESCRIPTION</span></span>
<span data-ttu-id="34bac-106">Il cmdlet **Import-AzRedisCache** importa dati da BLOB nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="34bac-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="34bac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34bac-107">EXAMPLES</span></span>

### <span data-ttu-id="34bac-108">Esempio 1: importare dati</span><span class="sxs-lookup"><span data-stu-id="34bac-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="34bac-109">Questo comando importa i dati dal blob specificato dall'URL SAS nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="34bac-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="34bac-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34bac-110">PARAMETERS</span></span>

### <span data-ttu-id="34bac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bac-111">-DefaultProfile</span></span>
<span data-ttu-id="34bac-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34bac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34bac-113">-File</span><span class="sxs-lookup"><span data-stu-id="34bac-113">-Files</span></span>
<span data-ttu-id="34bac-114">Specifica gli URL SAS di BLOB di cui il contenuto questo cmdlet importa nella cache.</span><span class="sxs-lookup"><span data-stu-id="34bac-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="34bac-115">Puoi generare gli URL SAS usando i comandi di PowerShell seguenti: $storageAccountContext = New-AzStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForBlob = New-AzStorageBlobSASToken-container "ContainerName"-blob "blobname"-permission "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-context $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-nome "CacheName"-file ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="34bac-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="34bac-116">-Force</span><span class="sxs-lookup"><span data-stu-id="34bac-116">-Force</span></span>
<span data-ttu-id="34bac-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34bac-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34bac-118">-Format</span><span class="sxs-lookup"><span data-stu-id="34bac-118">-Format</span></span>
<span data-ttu-id="34bac-119">Specifica il formato del BLOB.</span><span class="sxs-lookup"><span data-stu-id="34bac-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="34bac-120">Attualmente RDB è l'unico formato supportato.</span><span class="sxs-lookup"><span data-stu-id="34bac-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="34bac-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="34bac-121">-Name</span></span>
<span data-ttu-id="34bac-122">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="34bac-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="34bac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34bac-123">-PassThru</span></span>
<span data-ttu-id="34bac-124">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="34bac-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="34bac-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="34bac-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34bac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bac-126">-ResourceGroupName</span></span>
<span data-ttu-id="34bac-127">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="34bac-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="34bac-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34bac-128">-Confirm</span></span>
<span data-ttu-id="34bac-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34bac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34bac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34bac-130">-WhatIf</span></span>
<span data-ttu-id="34bac-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34bac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34bac-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34bac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34bac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bac-133">CommonParameters</span></span>
<span data-ttu-id="34bac-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bac-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34bac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bac-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34bac-136">INPUTS</span></span>

### <span data-ttu-id="34bac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="34bac-137">System.String</span></span>

### <span data-ttu-id="34bac-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="34bac-138">System.String[]</span></span>

## <span data-ttu-id="34bac-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34bac-139">OUTPUTS</span></span>

### <span data-ttu-id="34bac-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34bac-140">System.Boolean</span></span>

## <span data-ttu-id="34bac-141">Note</span><span class="sxs-lookup"><span data-stu-id="34bac-141">NOTES</span></span>
* <span data-ttu-id="34bac-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="34bac-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="34bac-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34bac-143">RELATED LINKS</span></span>

[<span data-ttu-id="34bac-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="34bac-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="34bac-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="34bac-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="34bac-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="34bac-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


