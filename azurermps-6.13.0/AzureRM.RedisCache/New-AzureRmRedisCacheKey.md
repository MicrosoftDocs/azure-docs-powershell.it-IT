---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: d54bc01e7a5aa23206037d4eb1d99e5d9e5deb0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519713"
---
# <span data-ttu-id="464f4-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="464f4-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="464f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="464f4-102">SYNOPSIS</span></span>
<span data-ttu-id="464f4-103">Rigenera il tasto di scelta di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="464f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="464f4-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="464f4-105">DESCRIPTION</span></span>
<span data-ttu-id="464f4-106">Il cmdlet **New-AzureRmRedisCacheKey** rigenera il tasto di scelta di una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="464f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="464f4-107">EXAMPLES</span></span>

### <span data-ttu-id="464f4-108">Esempio 1: rigenerare una chiave primaria</span><span class="sxs-lookup"><span data-stu-id="464f4-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="464f4-109">Questo comando rigenera la chiave primaria di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="464f4-110">Esempio 2: rigenerare una chiave secondaria</span><span class="sxs-lookup"><span data-stu-id="464f4-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="464f4-111">Questo comando rigenera la chiave secondaria di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="464f4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="464f4-112">PARAMETERS</span></span>

### <span data-ttu-id="464f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464f4-113">-DefaultProfile</span></span>
<span data-ttu-id="464f4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="464f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="464f4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="464f4-115">-Force</span></span>
<span data-ttu-id="464f4-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="464f4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="464f4-117">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="464f4-117">-KeyType</span></span>
<span data-ttu-id="464f4-118">Specifica se rigenerare il codice di accesso primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="464f4-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="464f4-119">I valori validi sono: primario, secondario.</span><span class="sxs-lookup"><span data-stu-id="464f4-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464f4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="464f4-120">-Name</span></span>
<span data-ttu-id="464f4-121">Specifica il nome della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="464f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="464f4-123">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="464f4-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="464f4-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="464f4-124">-Confirm</span></span>
<span data-ttu-id="464f4-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464f4-126">-WhatIf</span></span>
<span data-ttu-id="464f4-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="464f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464f4-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="464f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464f4-129">CommonParameters</span></span>
<span data-ttu-id="464f4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464f4-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="464f4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464f4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="464f4-132">INPUTS</span></span>

### <span data-ttu-id="464f4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="464f4-133">System.String</span></span>

## <span data-ttu-id="464f4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="464f4-134">OUTPUTS</span></span>

### <span data-ttu-id="464f4-135">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="464f4-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="464f4-136">Note</span><span class="sxs-lookup"><span data-stu-id="464f4-136">NOTES</span></span>

## <span data-ttu-id="464f4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="464f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="464f4-138">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="464f4-138">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


