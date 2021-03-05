---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 2ae4c2d5de8eeba370c981ceb5a94baa1ba91cf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960126"
---
# <span data-ttu-id="67910-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="67910-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="67910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67910-102">SYNOPSIS</span></span>
<span data-ttu-id="67910-103">Rimuove una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="67910-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="67910-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67910-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67910-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67910-105">DESCRIPTION</span></span>
<span data-ttu-id="67910-106">Il cmdlet **Remove-AzRedisCache** rimuove una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="67910-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="67910-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67910-107">EXAMPLES</span></span>

### <span data-ttu-id="67910-108">Esempio 1: Rimuovere una cache di Ridis e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="67910-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="67910-109">Questo comando rimuove una cache di Ridis e indica se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="67910-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="67910-110">Esempio 2: Rimuovere una cache di Ridis e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="67910-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="67910-111">Questo comando rimuove una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="67910-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="67910-112">Poiché il *parametro PassThru* non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="67910-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="67910-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67910-113">PARAMETERS</span></span>

### <span data-ttu-id="67910-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67910-114">-DefaultProfile</span></span>
<span data-ttu-id="67910-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67910-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67910-116">-Force</span><span class="sxs-lookup"><span data-stu-id="67910-116">-Force</span></span>
<span data-ttu-id="67910-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="67910-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67910-118">-Name</span><span class="sxs-lookup"><span data-stu-id="67910-118">-Name</span></span>
<span data-ttu-id="67910-119">Specifica il nome della cache di Ridis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="67910-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="67910-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67910-120">-PassThru</span></span>
<span data-ttu-id="67910-121">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="67910-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67910-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="67910-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67910-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67910-123">-ResourceGroupName</span></span>
<span data-ttu-id="67910-124">Specifica il nome del gruppo di risorse che contiene la cache di Ridisposizione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="67910-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="67910-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67910-125">-Confirm</span></span>
<span data-ttu-id="67910-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67910-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67910-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67910-127">-WhatIf</span></span>
<span data-ttu-id="67910-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67910-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67910-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67910-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67910-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67910-130">CommonParameters</span></span>
<span data-ttu-id="67910-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67910-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67910-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67910-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67910-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="67910-133">INPUTS</span></span>

### <span data-ttu-id="67910-134">System.String</span><span class="sxs-lookup"><span data-stu-id="67910-134">System.String</span></span>

## <span data-ttu-id="67910-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67910-135">OUTPUTS</span></span>

### <span data-ttu-id="67910-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67910-136">System.Boolean</span></span>

## <span data-ttu-id="67910-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="67910-137">NOTES</span></span>

## <span data-ttu-id="67910-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67910-138">RELATED LINKS</span></span>

[<span data-ttu-id="67910-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="67910-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="67910-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="67910-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="67910-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="67910-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


