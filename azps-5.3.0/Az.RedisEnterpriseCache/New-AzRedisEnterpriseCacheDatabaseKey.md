---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474346"
---
# <span data-ttu-id="d4b0c-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="d4b0c-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="d4b0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b0c-103">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="d4b0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4b0c-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4b0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d4b0c-106">Rigenera i tasti di scelta del database RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="d4b0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="d4b0c-108">Esempio 1: rigenerare il tasto di accesso principale</span><span class="sxs-lookup"><span data-stu-id="d4b0c-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="d4b0c-109">Questo comando Rigenera il codice di accesso segreto principale usato per l'autenticazione delle connessioni al database della cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="d4b0c-110">Esempio 2: rigenerare il tasto di accesso secondario</span><span class="sxs-lookup"><span data-stu-id="d4b0c-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="d4b0c-111">Questo comando Rigenera il codice di accesso segreto secondario usato per l'autenticazione delle connessioni al database della cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="d4b0c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="d4b0c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4b0c-113">-AsJob</span></span>
<span data-ttu-id="d4b0c-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d4b0c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d4b0c-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d4b0c-115">-ClusterName</span></span>
<span data-ttu-id="d4b0c-116">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="d4b0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b0c-117">-DefaultProfile</span></span>
<span data-ttu-id="d4b0c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b0c-119">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="d4b0c-119">-KeyType</span></span>
<span data-ttu-id="d4b0c-120">Il tasto di scelta per la rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-120">Which access key to regenerate.</span></span>

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

### <span data-ttu-id="d4b0c-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d4b0c-121">-NoWait</span></span>
<span data-ttu-id="d4b0c-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d4b0c-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d4b0c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b0c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4b0c-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4b0c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4b0c-125">-SubscriptionId</span></span>
<span data-ttu-id="d4b0c-126">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4b0c-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4b0c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4b0c-128">-Confirm</span></span>
<span data-ttu-id="d4b0c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b0c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b0c-130">-WhatIf</span></span>
<span data-ttu-id="d4b0c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b0c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b0c-133">CommonParameters</span></span>
<span data-ttu-id="d4b0c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b0c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4b0c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b0c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4b0c-136">INPUTS</span></span>

## <span data-ttu-id="d4b0c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4b0c-137">OUTPUTS</span></span>

### <span data-ttu-id="d4b0c-138">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d4b0c-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="d4b0c-139">Note</span><span class="sxs-lookup"><span data-stu-id="d4b0c-139">NOTES</span></span>

<span data-ttu-id="d4b0c-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4b0c-140">ALIASES</span></span>

## <span data-ttu-id="d4b0c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4b0c-141">RELATED LINKS</span></span>

