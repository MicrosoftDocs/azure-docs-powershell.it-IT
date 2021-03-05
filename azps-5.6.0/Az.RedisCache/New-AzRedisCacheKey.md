---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: 1d9b11aa7c259a3534b76a1d1ef011671c7f1142
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014925"
---
# <span data-ttu-id="bd66d-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="bd66d-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="bd66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd66d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd66d-103">Rigenera la chiave di accesso di una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="bd66d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd66d-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd66d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd66d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd66d-106">Il cmdlet **New-AzRedisCacheKey** rigenera la chiave di accesso di una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="bd66d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd66d-107">EXAMPLES</span></span>

### <span data-ttu-id="bd66d-108">Esempio 1: Rigenerare una chiave primaria</span><span class="sxs-lookup"><span data-stu-id="bd66d-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="bd66d-109">Questo comando rigenera la chiave primaria di una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="bd66d-110">Esempio 2: Rigenerare una chiave secondaria</span><span class="sxs-lookup"><span data-stu-id="bd66d-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="bd66d-111">Questo comando rigenera la chiave secondaria di una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="bd66d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd66d-112">PARAMETERS</span></span>

### <span data-ttu-id="bd66d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd66d-113">-DefaultProfile</span></span>
<span data-ttu-id="bd66d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd66d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd66d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bd66d-115">-Force</span></span>
<span data-ttu-id="bd66d-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="bd66d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd66d-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="bd66d-117">-KeyType</span></span>
<span data-ttu-id="bd66d-118">Specifica se rigenerare la chiave di accesso primaria o secondaria.</span><span class="sxs-lookup"><span data-stu-id="bd66d-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="bd66d-119">I valori validi sono: Primario, Secondario.</span><span class="sxs-lookup"><span data-stu-id="bd66d-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="bd66d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bd66d-120">-Name</span></span>
<span data-ttu-id="bd66d-121">Specifica il nome della cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="bd66d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd66d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd66d-123">Specifica il nome del gruppo di risorse che contiene la cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="bd66d-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="bd66d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd66d-124">-Confirm</span></span>
<span data-ttu-id="bd66d-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd66d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd66d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd66d-126">-WhatIf</span></span>
<span data-ttu-id="bd66d-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd66d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd66d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd66d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd66d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd66d-129">CommonParameters</span></span>
<span data-ttu-id="bd66d-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd66d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd66d-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd66d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd66d-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd66d-132">INPUTS</span></span>

### <span data-ttu-id="bd66d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bd66d-133">System.String</span></span>

## <span data-ttu-id="bd66d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd66d-134">OUTPUTS</span></span>

### <span data-ttu-id="bd66d-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bd66d-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="bd66d-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd66d-136">NOTES</span></span>

## <span data-ttu-id="bd66d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd66d-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd66d-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="bd66d-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


