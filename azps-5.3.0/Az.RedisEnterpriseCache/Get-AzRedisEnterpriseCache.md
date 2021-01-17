---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474348"
---
# <span data-ttu-id="f4db7-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="f4db7-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="f4db7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4db7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4db7-103">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="f4db7-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f4db7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4db7-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4db7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4db7-105">DESCRIPTION</span></span>
<span data-ttu-id="f4db7-106">Ottiene informazioni su un cluster RedisEnterprise e sul database associato</span><span class="sxs-lookup"><span data-stu-id="f4db7-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f4db7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4db7-107">EXAMPLES</span></span>

### <span data-ttu-id="f4db7-108">Esempio 1: ottenere una cache di redis Enterprise per nome</span><span class="sxs-lookup"><span data-stu-id="f4db7-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="f4db7-109">Questo comando consente di ottenere la cache di redis Enterprise denominata cache.</span><span class="sxs-lookup"><span data-stu-id="f4db7-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="f4db7-110">Esempio 2: ottenere ogni cache di redis Enterprise in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f4db7-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="f4db7-111">Questo comando consente di ottenere tutte le cache di redis Enterprise nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f4db7-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="f4db7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4db7-112">PARAMETERS</span></span>

### <span data-ttu-id="f4db7-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f4db7-113">-ClusterName</span></span>
<span data-ttu-id="f4db7-114">Il nome del cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="f4db7-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="f4db7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4db7-115">-DefaultProfile</span></span>
<span data-ttu-id="f4db7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4db7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4db7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4db7-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4db7-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4db7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4db7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4db7-119">-SubscriptionId</span></span>
<span data-ttu-id="f4db7-120">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4db7-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4db7-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f4db7-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4db7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4db7-122">CommonParameters</span></span>
<span data-ttu-id="f4db7-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4db7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4db7-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4db7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4db7-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4db7-125">INPUTS</span></span>

## <span data-ttu-id="f4db7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4db7-126">OUTPUTS</span></span>

### <span data-ttu-id="f4db7-127">Microsoft. Azure. PowerShell. Cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="f4db7-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="f4db7-128">Note</span><span class="sxs-lookup"><span data-stu-id="f4db7-128">NOTES</span></span>

<span data-ttu-id="f4db7-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f4db7-129">ALIASES</span></span>

## <span data-ttu-id="f4db7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4db7-130">RELATED LINKS</span></span>

