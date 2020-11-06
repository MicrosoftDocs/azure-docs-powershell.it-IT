---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510371"
---
# <span data-ttu-id="a4b9a-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4b9a-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="a4b9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b9a-103">Rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4b9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b9a-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b9a-106">Il cmdlet **Remove-AzureRmRedisCache** rimuove una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="a4b9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b9a-108">Esempio 1: rimuovere una cache Redis e restituire il risultato</span><span class="sxs-lookup"><span data-stu-id="a4b9a-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="a4b9a-109">Questo comando rimuove una cache Redis e visualizza se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="a4b9a-110">Esempio 2: rimuovere una cache Redis e non visualizzare il risultato</span><span class="sxs-lookup"><span data-stu-id="a4b9a-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="a4b9a-111">Questo comando rimuove una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="a4b9a-112">Poiché il parametro *PassThru* non è specificato, il risultato dell'operazione non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="a4b9a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4b9a-113">PARAMETERS</span></span>

### <span data-ttu-id="a4b9a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a4b9a-114">-Force</span></span>
<span data-ttu-id="a4b9a-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4b9a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4b9a-116">-Name</span></span>
<span data-ttu-id="a4b9a-117">Specifica il nome della cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-117">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="a4b9a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4b9a-118">-PassThru</span></span>
<span data-ttu-id="a4b9a-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4b9a-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4b9a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b9a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4b9a-122">Specifica il nome del gruppo di risorse che contiene la cache Redis da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-122">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="a4b9a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4b9a-123">-Confirm</span></span>
<span data-ttu-id="a4b9a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b9a-125">-WhatIf</span></span>
<span data-ttu-id="a4b9a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b9a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b9a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b9a-128">-DefaultProfile</span></span>
<span data-ttu-id="a4b9a-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b9a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b9a-130">CommonParameters</span></span>
<span data-ttu-id="a4b9a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b9a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b9a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b9a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4b9a-133">INPUTS</span></span>

### <span data-ttu-id="a4b9a-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4b9a-134">None</span></span>
<span data-ttu-id="a4b9a-135">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="a4b9a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b9a-136">OUTPUTS</span></span>

### <span data-ttu-id="a4b9a-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4b9a-137">Boolean</span></span>
<span data-ttu-id="a4b9a-138">Restituisce $True se non si verifica un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a4b9a-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="a4b9a-139">Note</span><span class="sxs-lookup"><span data-stu-id="a4b9a-139">NOTES</span></span>

## <span data-ttu-id="a4b9a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b9a-140">RELATED LINKS</span></span>

[<span data-ttu-id="a4b9a-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4b9a-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a4b9a-142">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4b9a-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a4b9a-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a4b9a-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


