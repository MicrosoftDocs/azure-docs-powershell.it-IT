---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 35b7d3e05cced593da748f430cb121da43cd0380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519711"
---
# <span data-ttu-id="0ec6f-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ec6f-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="0ec6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ec6f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec6f-103">Rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ec6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ec6f-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ec6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ec6f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec6f-106">Il cmdlet **Remove-AzureRmRedisCache** rimuove una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="0ec6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ec6f-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec6f-108">Esempio 1: rimuovere una cache Redis e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="0ec6f-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="0ec6f-109">Questo comando rimuove una cache Redis e visualizza se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="0ec6f-110">Esempio 2: rimuovere una cache Redis e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="0ec6f-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="0ec6f-111">Questo comando rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="0ec6f-112">Poiché il parametro *PassThru* non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="0ec6f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ec6f-113">PARAMETERS</span></span>

### <span data-ttu-id="0ec6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec6f-114">-DefaultProfile</span></span>
<span data-ttu-id="0ec6f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ec6f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0ec6f-116">-Force</span></span>
<span data-ttu-id="0ec6f-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ec6f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ec6f-118">-Name</span></span>
<span data-ttu-id="0ec6f-119">Specifica il nome della cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="0ec6f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ec6f-120">-PassThru</span></span>
<span data-ttu-id="0ec6f-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ec6f-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ec6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ec6f-124">Specifica il nome del gruppo di risorse che contiene la cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="0ec6f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ec6f-125">-Confirm</span></span>
<span data-ttu-id="0ec6f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ec6f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ec6f-127">-WhatIf</span></span>
<span data-ttu-id="0ec6f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ec6f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ec6f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec6f-130">CommonParameters</span></span>
<span data-ttu-id="0ec6f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec6f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec6f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec6f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec6f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ec6f-133">INPUTS</span></span>

### <span data-ttu-id="0ec6f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0ec6f-134">System.String</span></span>

## <span data-ttu-id="0ec6f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ec6f-135">OUTPUTS</span></span>

### <span data-ttu-id="0ec6f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ec6f-136">System.Boolean</span></span>

## <span data-ttu-id="0ec6f-137">Note</span><span class="sxs-lookup"><span data-stu-id="0ec6f-137">NOTES</span></span>

## <span data-ttu-id="0ec6f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ec6f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ec6f-139">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ec6f-139">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0ec6f-140">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ec6f-140">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0ec6f-141">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0ec6f-141">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


