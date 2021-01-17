---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474373"
---
# <span data-ttu-id="c5157-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c5157-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="c5157-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5157-102">SYNOPSIS</span></span>
<span data-ttu-id="c5157-103">Rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="c5157-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="c5157-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5157-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5157-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5157-105">DESCRIPTION</span></span>
<span data-ttu-id="c5157-106">Il cmdlet **Remove-AzRedisCache** rimuove una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c5157-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="c5157-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5157-107">EXAMPLES</span></span>

### <span data-ttu-id="c5157-108">Esempio 1: rimuovere una cache Redis e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="c5157-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="c5157-109">Questo comando rimuove una cache Redis e visualizza se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="c5157-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="c5157-110">Esempio 2: rimuovere una cache Redis e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="c5157-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="c5157-111">Questo comando rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="c5157-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="c5157-112">Poiché il parametro *PassThru* non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c5157-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="c5157-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5157-113">PARAMETERS</span></span>

### <span data-ttu-id="c5157-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5157-114">-DefaultProfile</span></span>
<span data-ttu-id="c5157-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5157-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5157-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c5157-116">-Force</span></span>
<span data-ttu-id="c5157-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c5157-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5157-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5157-118">-Name</span></span>
<span data-ttu-id="c5157-119">Specifica il nome della cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c5157-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c5157-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5157-120">-PassThru</span></span>
<span data-ttu-id="c5157-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c5157-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c5157-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c5157-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5157-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5157-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5157-124">Specifica il nome del gruppo di risorse che contiene la cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c5157-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c5157-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5157-125">-Confirm</span></span>
<span data-ttu-id="c5157-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5157-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5157-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5157-127">-WhatIf</span></span>
<span data-ttu-id="c5157-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5157-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5157-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5157-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5157-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5157-130">CommonParameters</span></span>
<span data-ttu-id="c5157-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5157-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5157-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5157-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5157-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5157-133">INPUTS</span></span>

### <span data-ttu-id="c5157-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c5157-134">System.String</span></span>

## <span data-ttu-id="c5157-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5157-135">OUTPUTS</span></span>

### <span data-ttu-id="c5157-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5157-136">System.Boolean</span></span>

## <span data-ttu-id="c5157-137">Note</span><span class="sxs-lookup"><span data-stu-id="c5157-137">NOTES</span></span>

## <span data-ttu-id="c5157-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5157-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5157-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c5157-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c5157-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c5157-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c5157-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c5157-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


