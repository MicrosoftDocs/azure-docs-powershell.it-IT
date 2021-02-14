---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183807"
---
# <span data-ttu-id="0208e-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="0208e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0208e-102">SYNOPSIS</span></span>
<span data-ttu-id="0208e-103">Importa dati dai BLOB nella cache di Redis di Azure.</span><span class="sxs-lookup"><span data-stu-id="0208e-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="0208e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0208e-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0208e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0208e-105">DESCRIPTION</span></span>
<span data-ttu-id="0208e-106">Il cmdlet **Import-AzRedisCache** importa dati dai BLOB nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="0208e-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="0208e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0208e-107">EXAMPLES</span></span>

### <span data-ttu-id="0208e-108">Esempio 1: Importare dati</span><span class="sxs-lookup"><span data-stu-id="0208e-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="0208e-109">Questo comando importa i dati dal BLOB specificato dall'URL di firma di accesso condiviso nella cache di Redis di Azure.</span><span class="sxs-lookup"><span data-stu-id="0208e-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="0208e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0208e-110">PARAMETERS</span></span>

### <span data-ttu-id="0208e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0208e-111">-DefaultProfile</span></span>
<span data-ttu-id="0208e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0208e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0208e-113">-File</span><span class="sxs-lookup"><span data-stu-id="0208e-113">-Files</span></span>
<span data-ttu-id="0208e-114">Specifica gli URL della firma di accesso condiviso dei BLOB il cui contenuto viene importato nella cache da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0208e-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="0208e-115">È possibile generare gli URL della firma di accesso condiviso usando i comandi di PowerShell seguenti: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "chiave" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="0208e-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="0208e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0208e-116">-Force</span></span>
<span data-ttu-id="0208e-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="0208e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0208e-118">-Format</span><span class="sxs-lookup"><span data-stu-id="0208e-118">-Format</span></span>
<span data-ttu-id="0208e-119">Specifica il formato del BLOB.</span><span class="sxs-lookup"><span data-stu-id="0208e-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="0208e-120">Attualmente rdb è l'unico formato supportato.</span><span class="sxs-lookup"><span data-stu-id="0208e-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="0208e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0208e-121">-Name</span></span>
<span data-ttu-id="0208e-122">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="0208e-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="0208e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0208e-123">-PassThru</span></span>
<span data-ttu-id="0208e-124">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0208e-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="0208e-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0208e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0208e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0208e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0208e-127">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="0208e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="0208e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0208e-128">-Confirm</span></span>
<span data-ttu-id="0208e-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0208e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0208e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0208e-130">-WhatIf</span></span>
<span data-ttu-id="0208e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0208e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0208e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0208e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0208e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0208e-133">CommonParameters</span></span>
<span data-ttu-id="0208e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0208e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0208e-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0208e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0208e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0208e-136">INPUTS</span></span>

### <span data-ttu-id="0208e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0208e-137">System.String</span></span>

### <span data-ttu-id="0208e-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0208e-138">System.String[]</span></span>

## <span data-ttu-id="0208e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0208e-139">OUTPUTS</span></span>

### <span data-ttu-id="0208e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0208e-140">System.Boolean</span></span>

## <span data-ttu-id="0208e-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0208e-141">NOTES</span></span>
* <span data-ttu-id="0208e-142">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="0208e-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0208e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0208e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0208e-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="0208e-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="0208e-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="0208e-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="0208e-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="0208e-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


