---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183782"
---
# <span data-ttu-id="25b81-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="25b81-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="25b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b81-102">SYNOPSIS</span></span>
<span data-ttu-id="25b81-103">Ottiene informazioni su un database in un cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="25b81-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="25b81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25b81-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="25b81-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25b81-105">DESCRIPTION</span></span>
<span data-ttu-id="25b81-106">Ottiene informazioni su un database in un cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="25b81-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="25b81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25b81-107">EXAMPLES</span></span>

### <span data-ttu-id="25b81-108">Esempio 1: Ottenere un database</span><span class="sxs-lookup"><span data-stu-id="25b81-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="25b81-109">Questo comando recupera il database della cache aziendale di Redis denominato MyCache.</span><span class="sxs-lookup"><span data-stu-id="25b81-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="25b81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b81-110">PARAMETERS</span></span>

### <span data-ttu-id="25b81-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="25b81-111">-ClusterName</span></span>
<span data-ttu-id="25b81-112">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="25b81-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="25b81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b81-113">-DefaultProfile</span></span>
<span data-ttu-id="25b81-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25b81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b81-115">-ResourceGroupName</span></span>
<span data-ttu-id="25b81-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25b81-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="25b81-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25b81-117">-SubscriptionId</span></span>
<span data-ttu-id="25b81-118">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25b81-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="25b81-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="25b81-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25b81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b81-120">CommonParameters</span></span>
<span data-ttu-id="25b81-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b81-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25b81-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b81-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="25b81-123">INPUTS</span></span>

## <span data-ttu-id="25b81-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25b81-124">OUTPUTS</span></span>

### <span data-ttu-id="25b81-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="25b81-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="25b81-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="25b81-126">NOTES</span></span>

<span data-ttu-id="25b81-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="25b81-127">ALIASES</span></span>

## <span data-ttu-id="25b81-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25b81-128">RELATED LINKS</span></span>

