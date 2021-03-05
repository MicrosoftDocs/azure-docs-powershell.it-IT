---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 42f91d45bf93f453e4c6368abaabcb64f9234771
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000941"
---
# <span data-ttu-id="df5bc-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="df5bc-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="df5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="df5bc-103">Rimuove la pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="df5bc-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="df5bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df5bc-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5bc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="df5bc-106">Il cmdlet **Remove-AzRedisCachePatchSchedule** rimuove la pianificazione delle patch da una cache della cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="df5bc-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="df5bc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="df5bc-108">Esempio 1: Rimuovere la pianificazione delle patch</span><span class="sxs-lookup"><span data-stu-id="df5bc-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="df5bc-109">Questo comando rimuove la pianificazione delle patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="df5bc-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="df5bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df5bc-110">PARAMETERS</span></span>

### <span data-ttu-id="df5bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5bc-111">-DefaultProfile</span></span>
<span data-ttu-id="df5bc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df5bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df5bc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="df5bc-113">-Name</span></span>
<span data-ttu-id="df5bc-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="df5bc-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="df5bc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df5bc-115">-PassThru</span></span>
<span data-ttu-id="df5bc-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="df5bc-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="df5bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="df5bc-118">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="df5bc-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="df5bc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df5bc-119">-Confirm</span></span>
<span data-ttu-id="df5bc-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df5bc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5bc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5bc-121">-WhatIf</span></span>
<span data-ttu-id="df5bc-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df5bc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df5bc-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df5bc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5bc-124">CommonParameters</span></span>
<span data-ttu-id="df5bc-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5bc-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5bc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5bc-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="df5bc-127">INPUTS</span></span>

### <span data-ttu-id="df5bc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="df5bc-128">System.String</span></span>

## <span data-ttu-id="df5bc-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df5bc-129">OUTPUTS</span></span>

### <span data-ttu-id="df5bc-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df5bc-130">System.Boolean</span></span>

## <span data-ttu-id="df5bc-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="df5bc-131">NOTES</span></span>
* <span data-ttu-id="df5bc-132">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="df5bc-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="df5bc-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df5bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="df5bc-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="df5bc-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="df5bc-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="df5bc-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="df5bc-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="df5bc-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


