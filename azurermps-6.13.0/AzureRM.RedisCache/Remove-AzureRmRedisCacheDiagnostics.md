---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 62519c49fe347036f5ea974dd2656aebe24b5675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519707"
---
# <span data-ttu-id="2c9a0-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2c9a0-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="2c9a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9a0-103">Disattiva la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c9a0-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9a0-106">Il cmdlet **Remove-AzureRmRedisCacheDiagnostics** Disabilita la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="2c9a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9a0-108">Esempio 1: disabilitare la diagnostica</span><span class="sxs-lookup"><span data-stu-id="2c9a0-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="2c9a0-109">Questo comando Disabilita la diagnostica nella cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="2c9a0-110">Questo disabilita la diagnostica per tutte le cache di Azure Redis nella stessa area geografica per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="2c9a0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c9a0-111">PARAMETERS</span></span>

### <span data-ttu-id="2c9a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9a0-112">-DefaultProfile</span></span>
<span data-ttu-id="2c9a0-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9a0-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c9a0-114">-Name</span></span>
<span data-ttu-id="2c9a0-115">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="2c9a0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9a0-116">-ResourceGroupName</span></span>
<span data-ttu-id="2c9a0-117">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="2c9a0-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c9a0-118">-Confirm</span></span>
<span data-ttu-id="2c9a0-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9a0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9a0-120">-WhatIf</span></span>
<span data-ttu-id="2c9a0-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9a0-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9a0-123">CommonParameters</span></span>
<span data-ttu-id="2c9a0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9a0-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9a0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9a0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c9a0-126">INPUTS</span></span>

### <span data-ttu-id="2c9a0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9a0-127">System.String</span></span>

## <span data-ttu-id="2c9a0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c9a0-128">OUTPUTS</span></span>

### <span data-ttu-id="2c9a0-129">System. void</span><span class="sxs-lookup"><span data-stu-id="2c9a0-129">System.Void</span></span>

## <span data-ttu-id="2c9a0-130">Note</span><span class="sxs-lookup"><span data-stu-id="2c9a0-130">NOTES</span></span>
* <span data-ttu-id="2c9a0-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="2c9a0-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2c9a0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c9a0-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c9a0-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2c9a0-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


