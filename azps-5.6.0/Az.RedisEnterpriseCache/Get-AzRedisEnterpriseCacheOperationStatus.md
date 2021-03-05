---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: fd2662af291b8c5c3372f27a3de89f7e18bfd35e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000782"
---
# <span data-ttu-id="5d3ea-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5d3ea-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="5d3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3ea-103">Ottiene lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-103">Gets the status of operation.</span></span>

## <span data-ttu-id="5d3ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d3ea-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5d3ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="5d3ea-106">Ottiene lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-106">Gets the status of operation.</span></span>

## <span data-ttu-id="5d3ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="5d3ea-108">Esempio 1: Ottenere lo stato dell'operazione</span><span class="sxs-lookup"><span data-stu-id="5d3ea-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="5d3ea-109">Questo comando ottiene lo stato di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="5d3ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d3ea-110">PARAMETERS</span></span>

### <span data-ttu-id="5d3ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3ea-111">-DefaultProfile</span></span>
<span data-ttu-id="5d3ea-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d3ea-113">-Location</span><span class="sxs-lookup"><span data-stu-id="5d3ea-113">-Location</span></span>
<span data-ttu-id="5d3ea-114">Area geografica in cui si trova l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="5d3ea-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5d3ea-115">-OperationId</span></span>
<span data-ttu-id="5d3ea-116">Identificatore univoco dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="5d3ea-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d3ea-117">-SubscriptionId</span></span>
<span data-ttu-id="5d3ea-118">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d3ea-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d3ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3ea-120">CommonParameters</span></span>
<span data-ttu-id="5d3ea-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3ea-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d3ea-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3ea-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d3ea-123">INPUTS</span></span>

## <span data-ttu-id="5d3ea-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d3ea-124">OUTPUTS</span></span>

### <span data-ttu-id="5d3ea-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5d3ea-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="5d3ea-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d3ea-126">NOTES</span></span>

<span data-ttu-id="5d3ea-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5d3ea-127">ALIASES</span></span>

## <span data-ttu-id="5d3ea-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d3ea-128">RELATED LINKS</span></span>

