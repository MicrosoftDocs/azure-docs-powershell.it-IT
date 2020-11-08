---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201280"
---
# <span data-ttu-id="6394b-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="6394b-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="6394b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6394b-102">SYNOPSIS</span></span>
<span data-ttu-id="6394b-103">Ottiene una cache (s).</span><span class="sxs-lookup"><span data-stu-id="6394b-103">Gets a cache(s).</span></span>

## <span data-ttu-id="6394b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6394b-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6394b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6394b-105">DESCRIPTION</span></span>
<span data-ttu-id="6394b-106">Il cmdlet **Get-AzHpcCache** consente di ottenere una singola cache, una cache o un gruppo di risorse specifico o un elenco esteso di sottoscrizioni di cache.</span><span class="sxs-lookup"><span data-stu-id="6394b-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="6394b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6394b-107">EXAMPLES</span></span>

### <span data-ttu-id="6394b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6394b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="6394b-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6394b-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="6394b-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6394b-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="6394b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6394b-111">PARAMETERS</span></span>

### <span data-ttu-id="6394b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6394b-112">-DefaultProfile</span></span>
<span data-ttu-id="6394b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6394b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6394b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6394b-114">-Name</span></span>
<span data-ttu-id="6394b-115">Nome della cache specifica.</span><span class="sxs-lookup"><span data-stu-id="6394b-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="6394b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6394b-116">-ResourceGroupName</span></span>
<span data-ttu-id="6394b-117">Nome del gruppo di risorse in cui si vogliono elencare le cache.</span><span class="sxs-lookup"><span data-stu-id="6394b-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="6394b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6394b-118">CommonParameters</span></span>
<span data-ttu-id="6394b-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6394b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6394b-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6394b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6394b-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6394b-121">INPUTS</span></span>

### <span data-ttu-id="6394b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6394b-122">System.String</span></span>

## <span data-ttu-id="6394b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6394b-123">OUTPUTS</span></span>

### <span data-ttu-id="6394b-124">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="6394b-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="6394b-125">Note</span><span class="sxs-lookup"><span data-stu-id="6394b-125">NOTES</span></span>

## <span data-ttu-id="6394b-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6394b-126">RELATED LINKS</span></span>
