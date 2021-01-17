---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474980"
---
# <span data-ttu-id="a5c26-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="a5c26-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="a5c26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5c26-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c26-103">Rigenera il tasto di scelta di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="a5c26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5c26-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5c26-105">DESCRIPTION</span></span>
<span data-ttu-id="a5c26-106">Il cmdlet **New-AzRedisCacheKey** rigenera il tasto di scelta di una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="a5c26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5c26-107">EXAMPLES</span></span>

### <span data-ttu-id="a5c26-108">Esempio 1: rigenerare una chiave primaria</span><span class="sxs-lookup"><span data-stu-id="a5c26-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="a5c26-109">Questo comando rigenera la chiave primaria di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="a5c26-110">Esempio 2: rigenerare una chiave secondaria</span><span class="sxs-lookup"><span data-stu-id="a5c26-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="a5c26-111">Questo comando rigenera la chiave secondaria di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="a5c26-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5c26-112">PARAMETERS</span></span>

### <span data-ttu-id="a5c26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c26-113">-DefaultProfile</span></span>
<span data-ttu-id="a5c26-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c26-115">-Force</span></span>
<span data-ttu-id="a5c26-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a5c26-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5c26-117">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="a5c26-117">-KeyType</span></span>
<span data-ttu-id="a5c26-118">Specifica se rigenerare il codice di accesso primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="a5c26-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="a5c26-119">I valori validi sono: primario, secondario.</span><span class="sxs-lookup"><span data-stu-id="a5c26-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="a5c26-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5c26-120">-Name</span></span>
<span data-ttu-id="a5c26-121">Specifica il nome della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="a5c26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c26-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5c26-123">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5c26-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="a5c26-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5c26-124">-Confirm</span></span>
<span data-ttu-id="a5c26-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5c26-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c26-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c26-126">-WhatIf</span></span>
<span data-ttu-id="a5c26-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c26-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c26-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5c26-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c26-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c26-129">CommonParameters</span></span>
<span data-ttu-id="a5c26-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c26-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c26-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c26-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c26-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5c26-132">INPUTS</span></span>

### <span data-ttu-id="a5c26-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c26-133">System.String</span></span>

## <span data-ttu-id="a5c26-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5c26-134">OUTPUTS</span></span>

### <span data-ttu-id="a5c26-135">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a5c26-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="a5c26-136">Note</span><span class="sxs-lookup"><span data-stu-id="a5c26-136">NOTES</span></span>

## <span data-ttu-id="a5c26-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5c26-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5c26-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="a5c26-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


