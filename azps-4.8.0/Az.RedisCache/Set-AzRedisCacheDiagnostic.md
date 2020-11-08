---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189415"
---
# <span data-ttu-id="c16b8-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c16b8-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="c16b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c16b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c16b8-103">Abilita la diagnostica in una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c16b8-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c16b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c16b8-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c16b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c16b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c16b8-106">Il cmdlet **set-AzRedisCacheDiagnostic** Abilita la diagnostica per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c16b8-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="c16b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c16b8-107">EXAMPLES</span></span>

### <span data-ttu-id="c16b8-108">Esempio 1: abilitare la diagnostica</span><span class="sxs-lookup"><span data-stu-id="c16b8-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="c16b8-109">Questo comando consente di abilitare la diagnostica per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c16b8-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="c16b8-110">Questo comando consente di abilitare la diagnostica o aggiornare l'account di archiviazione per tutte le cache di Azure Redis nella stessa area geografica per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c16b8-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c16b8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c16b8-111">PARAMETERS</span></span>

### <span data-ttu-id="c16b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16b8-112">-DefaultProfile</span></span>
<span data-ttu-id="c16b8-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c16b8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c16b8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c16b8-114">-Name</span></span>
<span data-ttu-id="c16b8-115">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="c16b8-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c16b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c16b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="c16b8-117">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="c16b8-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c16b8-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c16b8-118">-StorageAccountId</span></span>
<span data-ttu-id="c16b8-119">Specifica l'ID risorsa dell'account di archiviazione usato per archiviare i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="c16b8-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="c16b8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c16b8-120">-Confirm</span></span>
<span data-ttu-id="c16b8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16b8-122">-WhatIf</span></span>
<span data-ttu-id="c16b8-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c16b8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c16b8-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c16b8-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16b8-125">CommonParameters</span></span>
<span data-ttu-id="c16b8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16b8-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16b8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16b8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c16b8-128">INPUTS</span></span>

### <span data-ttu-id="c16b8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c16b8-129">System.String</span></span>

## <span data-ttu-id="c16b8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c16b8-130">OUTPUTS</span></span>

### <span data-ttu-id="c16b8-131">System. void</span><span class="sxs-lookup"><span data-stu-id="c16b8-131">System.Void</span></span>

## <span data-ttu-id="c16b8-132">Note</span><span class="sxs-lookup"><span data-stu-id="c16b8-132">NOTES</span></span>
* <span data-ttu-id="c16b8-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="c16b8-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c16b8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c16b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="c16b8-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c16b8-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


