---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865145"
---
# <span data-ttu-id="15a7e-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="15a7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="15a7e-103">Riavvia i nodi di una cache.</span><span class="sxs-lookup"><span data-stu-id="15a7e-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="15a7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15a7e-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15a7e-105">DESCRIPTION</span></span>
<span data-ttu-id="15a7e-106">Il cmdlet **Reset-AzRedisCache** riavvia i nodi di un'istanza della cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="15a7e-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="15a7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15a7e-107">EXAMPLES</span></span>

### <span data-ttu-id="15a7e-108">Esempio 1: riavviare entrambi i nodi</span><span class="sxs-lookup"><span data-stu-id="15a7e-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="15a7e-109">Questo comando Riavvia entrambi i nodi per la cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="15a7e-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="15a7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15a7e-110">PARAMETERS</span></span>

### <span data-ttu-id="15a7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a7e-111">-DefaultProfile</span></span>
<span data-ttu-id="15a7e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15a7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a7e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="15a7e-113">-Force</span></span>
<span data-ttu-id="15a7e-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="15a7e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15a7e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a7e-115">-Name</span></span>
<span data-ttu-id="15a7e-116">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="15a7e-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="15a7e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15a7e-117">-PassThru</span></span>
<span data-ttu-id="15a7e-118">Indica che questo cmdlet restituisce un valore booleano che indica se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="15a7e-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="15a7e-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="15a7e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15a7e-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="15a7e-120">-RebootType</span></span>
<span data-ttu-id="15a7e-121">Specifica il nodo o i nodi da riavviare.</span><span class="sxs-lookup"><span data-stu-id="15a7e-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="15a7e-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="15a7e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="15a7e-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="15a7e-123">PrimaryNode</span></span> 
- <span data-ttu-id="15a7e-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="15a7e-124">SecondaryNode</span></span> 
- <span data-ttu-id="15a7e-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="15a7e-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="15a7e-127">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="15a7e-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="15a7e-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="15a7e-128">-ShardId</span></span>
<span data-ttu-id="15a7e-129">Specifica l'ID del frammento che questo cmdlet riavvia per una cache Premium con il clustering abilitato.</span><span class="sxs-lookup"><span data-stu-id="15a7e-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a7e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15a7e-130">-Confirm</span></span>
<span data-ttu-id="15a7e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a7e-132">-WhatIf</span></span>
<span data-ttu-id="15a7e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a7e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a7e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a7e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a7e-135">CommonParameters</span></span>
<span data-ttu-id="15a7e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a7e-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a7e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a7e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15a7e-138">INPUTS</span></span>

### <span data-ttu-id="15a7e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="15a7e-139">System.String</span></span>

### <span data-ttu-id="15a7e-140">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15a7e-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="15a7e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15a7e-141">OUTPUTS</span></span>

### <span data-ttu-id="15a7e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15a7e-142">System.Boolean</span></span>

## <span data-ttu-id="15a7e-143">Note</span><span class="sxs-lookup"><span data-stu-id="15a7e-143">NOTES</span></span>
* <span data-ttu-id="15a7e-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="15a7e-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="15a7e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15a7e-145">RELATED LINKS</span></span>

[<span data-ttu-id="15a7e-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="15a7e-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="15a7e-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="15a7e-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="15a7e-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="15a7e-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


