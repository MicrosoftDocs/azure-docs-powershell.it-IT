---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206115"
---
# <span data-ttu-id="bfbee-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bfbee-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="bfbee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfbee-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbee-103">Disabilita la diagnostica in una cache di Ridis di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfbee-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="bfbee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfbee-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfbee-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfbee-105">DESCRIPTION</span></span>
<span data-ttu-id="bfbee-106">Il cmdlet **Remove-AzRedisCacheDiagnostic** disabilita la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bfbee-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="bfbee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfbee-107">EXAMPLES</span></span>

### <span data-ttu-id="bfbee-108">Esempio 1: Disabilitare la diagnostica</span><span class="sxs-lookup"><span data-stu-id="bfbee-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="bfbee-109">Questo comando disabilita la diagnostica nella cache di Ridisposizione di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="bfbee-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="bfbee-110">In questo modo la diagnostica per tutte le cache di Azure Redis nella stessa area geografica viene disabilitata per la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="bfbee-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="bfbee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfbee-111">PARAMETERS</span></span>

### <span data-ttu-id="bfbee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbee-112">-DefaultProfile</span></span>
<span data-ttu-id="bfbee-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfbee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfbee-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bfbee-114">-Name</span></span>
<span data-ttu-id="bfbee-115">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="bfbee-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="bfbee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfbee-116">-ResourceGroupName</span></span>
<span data-ttu-id="bfbee-117">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="bfbee-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="bfbee-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfbee-118">-Confirm</span></span>
<span data-ttu-id="bfbee-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfbee-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbee-120">-WhatIf</span></span>
<span data-ttu-id="bfbee-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfbee-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbee-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfbee-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbee-123">CommonParameters</span></span>
<span data-ttu-id="bfbee-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfbee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbee-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfbee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbee-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfbee-126">INPUTS</span></span>

### <span data-ttu-id="bfbee-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bfbee-127">System.String</span></span>

## <span data-ttu-id="bfbee-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfbee-128">OUTPUTS</span></span>

### <span data-ttu-id="bfbee-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="bfbee-129">System.Void</span></span>

## <span data-ttu-id="bfbee-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfbee-130">NOTES</span></span>
* <span data-ttu-id="bfbee-131">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="bfbee-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bfbee-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfbee-132">RELATED LINKS</span></span>

[<span data-ttu-id="bfbee-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bfbee-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


