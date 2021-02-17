---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206106"
---
# <span data-ttu-id="32b6b-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="32b6b-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="32b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b6b-103">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="32b6b-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="32b6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32b6b-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="32b6b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="32b6b-106">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="32b6b-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="32b6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="32b6b-108">Esempio 1: Ottenere una cache aziendale di Redis in base al nome</span><span class="sxs-lookup"><span data-stu-id="32b6b-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="32b6b-109">Questo comando recupera la cache dell'organizzazione di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="32b6b-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="32b6b-110">Esempio 2: Ottenere ogni cache di Ridis Enterprise in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="32b6b-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="32b6b-111">Questo comando recupera tutte le cache dell'organizzazione di Ridis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="32b6b-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="32b6b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32b6b-112">PARAMETERS</span></span>

### <span data-ttu-id="32b6b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="32b6b-113">-ClusterName</span></span>
<span data-ttu-id="32b6b-114">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="32b6b-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b6b-115">-DefaultProfile</span></span>
<span data-ttu-id="32b6b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32b6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="32b6b-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32b6b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="32b6b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32b6b-119">-SubscriptionId</span></span>
<span data-ttu-id="32b6b-120">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32b6b-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="32b6b-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="32b6b-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32b6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b6b-122">CommonParameters</span></span>
<span data-ttu-id="32b6b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b6b-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32b6b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b6b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="32b6b-125">INPUTS</span></span>

## <span data-ttu-id="32b6b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32b6b-126">OUTPUTS</span></span>

### <span data-ttu-id="32b6b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="32b6b-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="32b6b-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="32b6b-128">NOTES</span></span>

<span data-ttu-id="32b6b-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="32b6b-129">ALIASES</span></span>

## <span data-ttu-id="32b6b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32b6b-130">RELATED LINKS</span></span>

