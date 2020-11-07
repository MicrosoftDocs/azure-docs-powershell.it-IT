---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677485"
---
# <span data-ttu-id="1e418-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e418-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="1e418-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e418-102">SYNOPSIS</span></span>
<span data-ttu-id="1e418-103">Rimuove la pianificazione della patch.</span><span class="sxs-lookup"><span data-stu-id="1e418-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="1e418-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e418-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e418-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e418-105">DESCRIPTION</span></span>
<span data-ttu-id="1e418-106">Il cmdlet **Remove-AzRedisCachePatchSchedule** rimuove la pianificazione della patch da una cache in Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="1e418-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="1e418-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e418-107">EXAMPLES</span></span>

### <span data-ttu-id="1e418-108">Esempio 1: rimuovere la pianificazione della patch</span><span class="sxs-lookup"><span data-stu-id="1e418-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="1e418-109">Questo comando rimuove la pianificazione della patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="1e418-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="1e418-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e418-110">PARAMETERS</span></span>

### <span data-ttu-id="1e418-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e418-111">-DefaultProfile</span></span>
<span data-ttu-id="1e418-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e418-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e418-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e418-113">-Name</span></span>
<span data-ttu-id="1e418-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="1e418-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1e418-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e418-115">-PassThru</span></span>
<span data-ttu-id="1e418-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1e418-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e418-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e418-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e418-118">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="1e418-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="1e418-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e418-119">-Confirm</span></span>
<span data-ttu-id="1e418-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e418-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e418-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e418-121">-WhatIf</span></span>
<span data-ttu-id="1e418-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e418-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e418-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e418-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e418-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e418-124">CommonParameters</span></span>
<span data-ttu-id="1e418-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e418-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e418-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e418-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e418-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e418-127">INPUTS</span></span>

### <span data-ttu-id="1e418-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1e418-128">System.String</span></span>

## <span data-ttu-id="1e418-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e418-129">OUTPUTS</span></span>

### <span data-ttu-id="1e418-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e418-130">System.Boolean</span></span>

## <span data-ttu-id="1e418-131">Note</span><span class="sxs-lookup"><span data-stu-id="1e418-131">NOTES</span></span>
* <span data-ttu-id="1e418-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="1e418-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1e418-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e418-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e418-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e418-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="1e418-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e418-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="1e418-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1e418-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


