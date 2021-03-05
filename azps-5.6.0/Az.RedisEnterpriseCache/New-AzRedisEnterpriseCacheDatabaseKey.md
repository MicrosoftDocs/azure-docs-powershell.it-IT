---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: 3d28515ede93abf2ebb5be8bad2e961f2e22b572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000750"
---
# <span data-ttu-id="4873b-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="4873b-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="4873b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4873b-102">SYNOPSIS</span></span>
<span data-ttu-id="4873b-103">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4873b-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="4873b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4873b-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4873b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4873b-105">DESCRIPTION</span></span>
<span data-ttu-id="4873b-106">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4873b-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="4873b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4873b-107">EXAMPLES</span></span>

### <span data-ttu-id="4873b-108">Esempio 1: Rigenerare la chiave di accesso primaria</span><span class="sxs-lookup"><span data-stu-id="4873b-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="4873b-109">Questo comando rigenera la chiave di accesso segreto primario usata per l'autenticazione delle connessioni al database della cache di Redis Enterprise denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="4873b-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="4873b-110">Esempio 2: Rigenerare la chiave di accesso secondaria</span><span class="sxs-lookup"><span data-stu-id="4873b-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="4873b-111">Questo comando rigenera la chiave di accesso segreta secondaria usata per l'autenticazione delle connessioni al database della cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="4873b-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="4873b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4873b-112">PARAMETERS</span></span>

### <span data-ttu-id="4873b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4873b-113">-AsJob</span></span>
<span data-ttu-id="4873b-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4873b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4873b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4873b-115">-ClusterName</span></span>
<span data-ttu-id="4873b-116">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4873b-116">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4873b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4873b-117">-DefaultProfile</span></span>
<span data-ttu-id="4873b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4873b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4873b-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4873b-119">-KeyType</span></span>
<span data-ttu-id="4873b-120">Chiave di accesso da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="4873b-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4873b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4873b-121">-NoWait</span></span>
<span data-ttu-id="4873b-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4873b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4873b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4873b-123">-ResourceGroupName</span></span>
<span data-ttu-id="4873b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4873b-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4873b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4873b-125">-SubscriptionId</span></span>
<span data-ttu-id="4873b-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4873b-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4873b-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4873b-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4873b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4873b-128">-Confirm</span></span>
<span data-ttu-id="4873b-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4873b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4873b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4873b-130">-WhatIf</span></span>
<span data-ttu-id="4873b-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4873b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4873b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4873b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4873b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4873b-133">CommonParameters</span></span>
<span data-ttu-id="4873b-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4873b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4873b-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4873b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4873b-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4873b-136">INPUTS</span></span>

## <span data-ttu-id="4873b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4873b-137">OUTPUTS</span></span>

### <span data-ttu-id="4873b-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4873b-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="4873b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="4873b-139">NOTES</span></span>

<span data-ttu-id="4873b-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4873b-140">ALIASES</span></span>

## <span data-ttu-id="4873b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4873b-141">RELATED LINKS</span></span>

