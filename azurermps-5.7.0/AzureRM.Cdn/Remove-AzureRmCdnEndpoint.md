---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514540"
---
# <span data-ttu-id="d6a93-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="d6a93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6a93-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a93-103">Rimuove un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="d6a93-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6a93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6a93-104">SYNTAX</span></span>

### <span data-ttu-id="d6a93-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a93-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a93-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a93-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a93-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6a93-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a93-108">Il cmdlet **Remove-AzureRmCdnEndpoint** rimuove un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="d6a93-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d6a93-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6a93-109">EXAMPLES</span></span>

## <span data-ttu-id="d6a93-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6a93-110">PARAMETERS</span></span>

### <span data-ttu-id="d6a93-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-111">-CdnEndpoint</span></span>
<span data-ttu-id="d6a93-112">Specifica l'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6a93-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a93-113">-DefaultProfile</span></span>
<span data-ttu-id="d6a93-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6a93-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d6a93-115">-EndpointName</span></span>
<span data-ttu-id="d6a93-116">Specifica il nome dell'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6a93-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d6a93-117">-Force</span></span>
<span data-ttu-id="d6a93-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d6a93-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6a93-119">-PassThru</span></span>
<span data-ttu-id="d6a93-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d6a93-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6a93-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d6a93-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d6a93-122">-ProfileName</span></span>
<span data-ttu-id="d6a93-123">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d6a93-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a93-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6a93-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d6a93-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6a93-126">-Confirm</span></span>
<span data-ttu-id="d6a93-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6a93-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a93-128">-WhatIf</span></span>
<span data-ttu-id="d6a93-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a93-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a93-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6a93-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a93-131">CommonParameters</span></span>
<span data-ttu-id="d6a93-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a93-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a93-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6a93-134">INPUTS</span></span>

### <span data-ttu-id="d6a93-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-135">PSEndpoint</span></span>
<span data-ttu-id="d6a93-136">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d6a93-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d6a93-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6a93-137">OUTPUTS</span></span>

### <span data-ttu-id="d6a93-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6a93-138">System.Boolean</span></span>

## <span data-ttu-id="d6a93-139">Note</span><span class="sxs-lookup"><span data-stu-id="d6a93-139">NOTES</span></span>

## <span data-ttu-id="d6a93-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6a93-140">RELATED LINKS</span></span>

[<span data-ttu-id="d6a93-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="d6a93-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="d6a93-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="d6a93-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="d6a93-145">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a93-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


