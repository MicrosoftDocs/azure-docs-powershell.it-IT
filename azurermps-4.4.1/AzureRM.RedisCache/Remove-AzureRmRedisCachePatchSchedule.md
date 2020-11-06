---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510364"
---
# <span data-ttu-id="851de-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="851de-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="851de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="851de-102">SYNOPSIS</span></span>
<span data-ttu-id="851de-103">Rimuove la pianificazione della patch.</span><span class="sxs-lookup"><span data-stu-id="851de-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="851de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="851de-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="851de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="851de-105">DESCRIPTION</span></span>
<span data-ttu-id="851de-106">Il cmdlet **Remove-AzureRmRedisCachePatchSchedule** rimuove la pianificazione della patch da una cache in Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="851de-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="851de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="851de-107">EXAMPLES</span></span>

### <span data-ttu-id="851de-108">Esempio 1: rimuovere la pianificazione della patch</span><span class="sxs-lookup"><span data-stu-id="851de-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="851de-109">Questo comando rimuove la pianificazione della patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="851de-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="851de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="851de-110">PARAMETERS</span></span>

### <span data-ttu-id="851de-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="851de-111">-Name</span></span>
<span data-ttu-id="851de-112">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="851de-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="851de-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851de-113">-ResourceGroupName</span></span>
<span data-ttu-id="851de-114">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="851de-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="851de-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="851de-115">-Confirm</span></span>
<span data-ttu-id="851de-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="851de-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="851de-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="851de-117">-WhatIf</span></span>
<span data-ttu-id="851de-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="851de-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="851de-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="851de-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="851de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851de-120">-DefaultProfile</span></span>
<span data-ttu-id="851de-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="851de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="851de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851de-122">CommonParameters</span></span>
<span data-ttu-id="851de-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851de-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851de-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="851de-125">INPUTS</span></span>

### <span data-ttu-id="851de-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="851de-126">None</span></span>
<span data-ttu-id="851de-127">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="851de-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="851de-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="851de-128">OUTPUTS</span></span>

### <span data-ttu-id="851de-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="851de-129">None</span></span>

## <span data-ttu-id="851de-130">Note</span><span class="sxs-lookup"><span data-stu-id="851de-130">NOTES</span></span>
* <span data-ttu-id="851de-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="851de-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="851de-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="851de-132">RELATED LINKS</span></span>

[<span data-ttu-id="851de-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="851de-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="851de-134">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="851de-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="851de-135">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="851de-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


