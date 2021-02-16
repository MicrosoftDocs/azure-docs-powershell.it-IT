---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201959"
---
# <span data-ttu-id="79d21-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="79d21-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="79d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d21-102">SYNOPSIS</span></span>
<span data-ttu-id="79d21-103">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="79d21-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="79d21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79d21-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79d21-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79d21-105">DESCRIPTION</span></span>
<span data-ttu-id="79d21-106">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="79d21-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="79d21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79d21-107">EXAMPLES</span></span>

### <span data-ttu-id="79d21-108">Esempio 1: Rigenerare la chiave di accesso primaria</span><span class="sxs-lookup"><span data-stu-id="79d21-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="79d21-109">Questo comando rigenera la chiave di accesso segreta primaria usata per l'autenticazione delle connessioni al database della cache di Redis Enterprise denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="79d21-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="79d21-110">Esempio 2: Rigenerare la chiave di accesso secondaria</span><span class="sxs-lookup"><span data-stu-id="79d21-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="79d21-111">Questo comando rigenera la chiave di accesso segreta secondaria usata per l'autenticazione delle connessioni al database della cache aziendale di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="79d21-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="79d21-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79d21-112">PARAMETERS</span></span>

### <span data-ttu-id="79d21-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79d21-113">-AsJob</span></span>
<span data-ttu-id="79d21-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="79d21-114">Run the command as a job</span></span>

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

### <span data-ttu-id="79d21-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79d21-115">-ClusterName</span></span>
<span data-ttu-id="79d21-116">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="79d21-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="79d21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d21-117">-DefaultProfile</span></span>
<span data-ttu-id="79d21-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79d21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79d21-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="79d21-119">-KeyType</span></span>
<span data-ttu-id="79d21-120">Chiave di accesso da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="79d21-120">Which access key to regenerate.</span></span>

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

### <span data-ttu-id="79d21-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79d21-121">-NoWait</span></span>
<span data-ttu-id="79d21-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="79d21-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79d21-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79d21-123">-ResourceGroupName</span></span>
<span data-ttu-id="79d21-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79d21-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="79d21-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79d21-125">-SubscriptionId</span></span>
<span data-ttu-id="79d21-126">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="79d21-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="79d21-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="79d21-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="79d21-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79d21-128">-Confirm</span></span>
<span data-ttu-id="79d21-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79d21-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79d21-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d21-130">-WhatIf</span></span>
<span data-ttu-id="79d21-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79d21-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79d21-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79d21-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79d21-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d21-133">CommonParameters</span></span>
<span data-ttu-id="79d21-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d21-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d21-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79d21-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d21-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="79d21-136">INPUTS</span></span>

## <span data-ttu-id="79d21-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79d21-137">OUTPUTS</span></span>

### <span data-ttu-id="79d21-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="79d21-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="79d21-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="79d21-139">NOTES</span></span>

<span data-ttu-id="79d21-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="79d21-140">ALIASES</span></span>

## <span data-ttu-id="79d21-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79d21-141">RELATED LINKS</span></span>

