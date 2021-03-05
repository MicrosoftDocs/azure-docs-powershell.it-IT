---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012094"
---
# <span data-ttu-id="a802f-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="a802f-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="a802f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a802f-102">SYNOPSIS</span></span>
<span data-ttu-id="a802f-103">Ottiene una o più cache.</span><span class="sxs-lookup"><span data-stu-id="a802f-103">Gets a cache(s).</span></span>

## <span data-ttu-id="a802f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a802f-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a802f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a802f-105">DESCRIPTION</span></span>
<span data-ttu-id="a802f-106">Il cmdlet **Get-AzHpcCache** ottiene una singola cache, una o più cache in un gruppo di risorse specifico o un elenco di cache a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a802f-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="a802f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a802f-107">EXAMPLES</span></span>

### <span data-ttu-id="a802f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a802f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="a802f-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a802f-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="a802f-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a802f-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="a802f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a802f-111">PARAMETERS</span></span>

### <span data-ttu-id="a802f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a802f-112">-DefaultProfile</span></span>
<span data-ttu-id="a802f-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a802f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a802f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a802f-114">-Name</span></span>
<span data-ttu-id="a802f-115">Nome di cache specifica.</span><span class="sxs-lookup"><span data-stu-id="a802f-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a802f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a802f-116">-ResourceGroupName</span></span>
<span data-ttu-id="a802f-117">Nome del gruppo di risorse in cui elencare le cache.</span><span class="sxs-lookup"><span data-stu-id="a802f-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="a802f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a802f-118">CommonParameters</span></span>
<span data-ttu-id="a802f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a802f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a802f-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a802f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a802f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="a802f-121">INPUTS</span></span>

### <span data-ttu-id="a802f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="a802f-122">System.String</span></span>

## <span data-ttu-id="a802f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a802f-123">OUTPUTS</span></span>

### <span data-ttu-id="a802f-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="a802f-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="a802f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="a802f-125">NOTES</span></span>

## <span data-ttu-id="a802f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a802f-126">RELATED LINKS</span></span>
