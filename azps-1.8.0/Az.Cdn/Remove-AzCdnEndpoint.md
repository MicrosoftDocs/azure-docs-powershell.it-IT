---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 4dca00cf4b1746590591301657eb3ac0cbc7c17e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684863"
---
# <span data-ttu-id="e789c-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="e789c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e789c-102">SYNOPSIS</span></span>
<span data-ttu-id="e789c-103">Rimuove un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="e789c-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="e789c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e789c-104">SYNTAX</span></span>

### <span data-ttu-id="e789c-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e789c-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e789c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e789c-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e789c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e789c-107">DESCRIPTION</span></span>
<span data-ttu-id="e789c-108">Il cmdlet **Remove-AzCdnEndpoint** rimuove un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="e789c-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e789c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e789c-109">EXAMPLES</span></span>

## <span data-ttu-id="e789c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e789c-110">PARAMETERS</span></span>

### <span data-ttu-id="e789c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-111">-CdnEndpoint</span></span>
<span data-ttu-id="e789c-112">Specifica l'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e789c-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e789c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e789c-113">-DefaultProfile</span></span>
<span data-ttu-id="e789c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e789c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e789c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e789c-115">-EndpointName</span></span>
<span data-ttu-id="e789c-116">Specifica il nome dell'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e789c-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e789c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e789c-117">-Force</span></span>
<span data-ttu-id="e789c-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e789c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e789c-119">-PassThru</span></span>
<span data-ttu-id="e789c-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e789c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e789c-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e789c-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e789c-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e789c-122">-ProfileName</span></span>
<span data-ttu-id="e789c-123">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e789c-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e789c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e789c-124">-ResourceGroupName</span></span>
<span data-ttu-id="e789c-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e789c-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e789c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e789c-126">-Confirm</span></span>
<span data-ttu-id="e789c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e789c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e789c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e789c-128">-WhatIf</span></span>
<span data-ttu-id="e789c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e789c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e789c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e789c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e789c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e789c-131">CommonParameters</span></span>
<span data-ttu-id="e789c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e789c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e789c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e789c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e789c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e789c-134">INPUTS</span></span>

### <span data-ttu-id="e789c-135">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e789c-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e789c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e789c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e789c-137">OUTPUTS</span></span>

### <span data-ttu-id="e789c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e789c-138">System.Boolean</span></span>

## <span data-ttu-id="e789c-139">Note</span><span class="sxs-lookup"><span data-stu-id="e789c-139">NOTES</span></span>

## <span data-ttu-id="e789c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e789c-140">RELATED LINKS</span></span>

[<span data-ttu-id="e789c-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="e789c-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="e789c-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="e789c-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="e789c-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e789c-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


