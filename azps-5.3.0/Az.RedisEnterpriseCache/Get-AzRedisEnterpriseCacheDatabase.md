---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474349"
---
# <span data-ttu-id="16aa4-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="16aa4-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="16aa4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="16aa4-103">Ottiene le informazioni su un database in un cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="16aa4-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="16aa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16aa4-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16aa4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="16aa4-106">Ottiene le informazioni su un database in un cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="16aa4-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="16aa4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="16aa4-108">Esempio 1: recuperare il database</span><span class="sxs-lookup"><span data-stu-id="16aa4-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="16aa4-109">Questo comando consente di ottenere il database per la cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="16aa4-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="16aa4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16aa4-110">PARAMETERS</span></span>

### <span data-ttu-id="16aa4-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="16aa4-111">-ClusterName</span></span>
<span data-ttu-id="16aa4-112">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="16aa4-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="16aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="16aa4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16aa4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16aa4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16aa4-115">-ResourceGroupName</span></span>
<span data-ttu-id="16aa4-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16aa4-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="16aa4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16aa4-117">-SubscriptionId</span></span>
<span data-ttu-id="16aa4-118">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16aa4-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="16aa4-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="16aa4-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16aa4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16aa4-120">CommonParameters</span></span>
<span data-ttu-id="16aa4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16aa4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16aa4-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16aa4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16aa4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16aa4-123">INPUTS</span></span>

## <span data-ttu-id="16aa4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16aa4-124">OUTPUTS</span></span>

### <span data-ttu-id="16aa4-125">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="16aa4-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="16aa4-126">Note</span><span class="sxs-lookup"><span data-stu-id="16aa4-126">NOTES</span></span>

<span data-ttu-id="16aa4-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="16aa4-127">ALIASES</span></span>

## <span data-ttu-id="16aa4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16aa4-128">RELATED LINKS</span></span>

