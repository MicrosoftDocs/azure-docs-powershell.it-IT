---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000830"
---
# <span data-ttu-id="99ba2-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="99ba2-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="99ba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="99ba2-103">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="99ba2-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="99ba2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99ba2-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="99ba2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99ba2-105">DESCRIPTION</span></span>
<span data-ttu-id="99ba2-106">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="99ba2-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="99ba2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99ba2-107">EXAMPLES</span></span>

### <span data-ttu-id="99ba2-108">Esempio 1: Ottenere una cache aziendale di Redis in base al nome</span><span class="sxs-lookup"><span data-stu-id="99ba2-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="99ba2-109">Questo comando recupera la cache dell'organizzazione di Redis denominata MyCache.</span><span class="sxs-lookup"><span data-stu-id="99ba2-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="99ba2-110">Esempio 2: Ottenere ogni cache di Ridis Enterprise in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="99ba2-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="99ba2-111">Questo comando recupera ogni cache di Ridis Enterprise nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="99ba2-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="99ba2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99ba2-112">PARAMETERS</span></span>

### <span data-ttu-id="99ba2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99ba2-113">-ClusterName</span></span>
<span data-ttu-id="99ba2-114">Nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="99ba2-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="99ba2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ba2-115">-DefaultProfile</span></span>
<span data-ttu-id="99ba2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99ba2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ba2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ba2-117">-ResourceGroupName</span></span>
<span data-ttu-id="99ba2-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99ba2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="99ba2-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99ba2-119">-SubscriptionId</span></span>
<span data-ttu-id="99ba2-120">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99ba2-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="99ba2-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="99ba2-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99ba2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ba2-122">CommonParameters</span></span>
<span data-ttu-id="99ba2-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ba2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ba2-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99ba2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ba2-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="99ba2-125">INPUTS</span></span>

## <span data-ttu-id="99ba2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99ba2-126">OUTPUTS</span></span>

### <span data-ttu-id="99ba2-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="99ba2-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="99ba2-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="99ba2-128">NOTES</span></span>

<span data-ttu-id="99ba2-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="99ba2-129">ALIASES</span></span>

## <span data-ttu-id="99ba2-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99ba2-130">RELATED LINKS</span></span>

