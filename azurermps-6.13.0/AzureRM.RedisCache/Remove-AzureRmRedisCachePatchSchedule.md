---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686899"
---
# <span data-ttu-id="cea2e-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cea2e-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="cea2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cea2e-102">SYNOPSIS</span></span>
<span data-ttu-id="cea2e-103">Rimuove la pianificazione della patch.</span><span class="sxs-lookup"><span data-stu-id="cea2e-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cea2e-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cea2e-105">DESCRIPTION</span></span>
<span data-ttu-id="cea2e-106">Il cmdlet **Remove-AzureRmRedisCachePatchSchedule** rimuove la pianificazione della patch da una cache in Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="cea2e-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="cea2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cea2e-107">EXAMPLES</span></span>

### <span data-ttu-id="cea2e-108">Esempio 1: rimuovere la pianificazione della patch</span><span class="sxs-lookup"><span data-stu-id="cea2e-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="cea2e-109">Questo comando rimuove la pianificazione della patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="cea2e-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="cea2e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cea2e-110">PARAMETERS</span></span>

### <span data-ttu-id="cea2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea2e-111">-DefaultProfile</span></span>
<span data-ttu-id="cea2e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cea2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea2e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cea2e-113">-Name</span></span>
<span data-ttu-id="cea2e-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="cea2e-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="cea2e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cea2e-115">-PassThru</span></span>
<span data-ttu-id="cea2e-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cea2e-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cea2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cea2e-118">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="cea2e-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="cea2e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cea2e-119">-Confirm</span></span>
<span data-ttu-id="cea2e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cea2e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea2e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea2e-121">-WhatIf</span></span>
<span data-ttu-id="cea2e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cea2e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea2e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cea2e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea2e-124">CommonParameters</span></span>
<span data-ttu-id="cea2e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea2e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea2e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea2e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cea2e-127">INPUTS</span></span>

### <span data-ttu-id="cea2e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cea2e-128">System.String</span></span>

## <span data-ttu-id="cea2e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cea2e-129">OUTPUTS</span></span>

### <span data-ttu-id="cea2e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cea2e-130">System.Boolean</span></span>

## <span data-ttu-id="cea2e-131">Note</span><span class="sxs-lookup"><span data-stu-id="cea2e-131">NOTES</span></span>
* <span data-ttu-id="cea2e-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="cea2e-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cea2e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cea2e-133">RELATED LINKS</span></span>

[<span data-ttu-id="cea2e-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cea2e-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="cea2e-135">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cea2e-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="cea2e-136">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="cea2e-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


