---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190655"
---
# <span data-ttu-id="ed081-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ed081-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="ed081-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed081-102">SYNOPSIS</span></span>
<span data-ttu-id="ed081-103">Disattiva la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ed081-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="ed081-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed081-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed081-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed081-105">DESCRIPTION</span></span>
<span data-ttu-id="ed081-106">Il cmdlet **Remove-AzRedisCacheDiagnostic** Disabilita la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="ed081-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="ed081-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed081-107">EXAMPLES</span></span>

### <span data-ttu-id="ed081-108">Esempio 1: disabilitare la diagnostica</span><span class="sxs-lookup"><span data-stu-id="ed081-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="ed081-109">Questo comando Disabilita la diagnostica nella cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="ed081-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="ed081-110">Questo disabilita la diagnostica per tutte le cache di Azure Redis nella stessa area geografica per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ed081-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="ed081-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed081-111">PARAMETERS</span></span>

### <span data-ttu-id="ed081-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed081-112">-DefaultProfile</span></span>
<span data-ttu-id="ed081-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed081-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed081-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed081-114">-Name</span></span>
<span data-ttu-id="ed081-115">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="ed081-115">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed081-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed081-116">-ResourceGroupName</span></span>
<span data-ttu-id="ed081-117">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="ed081-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ed081-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed081-118">-Confirm</span></span>
<span data-ttu-id="ed081-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed081-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed081-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed081-120">-WhatIf</span></span>
<span data-ttu-id="ed081-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed081-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed081-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed081-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed081-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed081-123">CommonParameters</span></span>
<span data-ttu-id="ed081-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed081-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed081-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed081-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed081-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed081-126">INPUTS</span></span>

### <span data-ttu-id="ed081-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ed081-127">System.String</span></span>

## <span data-ttu-id="ed081-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed081-128">OUTPUTS</span></span>

### <span data-ttu-id="ed081-129">System. void</span><span class="sxs-lookup"><span data-stu-id="ed081-129">System.Void</span></span>

## <span data-ttu-id="ed081-130">Note</span><span class="sxs-lookup"><span data-stu-id="ed081-130">NOTES</span></span>
* <span data-ttu-id="ed081-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="ed081-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ed081-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed081-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed081-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ed081-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


