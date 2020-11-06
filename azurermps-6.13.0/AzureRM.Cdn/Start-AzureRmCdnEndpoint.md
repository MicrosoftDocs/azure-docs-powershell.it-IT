---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 4a6f7b86d16e5b82cf6bf9e869ed74f688fc5950
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517512"
---
# <span data-ttu-id="cf1da-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="cf1da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf1da-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1da-103">Avvia un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="cf1da-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf1da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf1da-104">SYNTAX</span></span>

### <span data-ttu-id="cf1da-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf1da-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1da-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1da-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf1da-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf1da-107">DESCRIPTION</span></span>
<span data-ttu-id="cf1da-108">Il cmdlet **Start-AzureRmCdnEndpoint** avvia un endpoint della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="cf1da-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cf1da-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf1da-109">EXAMPLES</span></span>

## <span data-ttu-id="cf1da-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf1da-110">PARAMETERS</span></span>

### <span data-ttu-id="cf1da-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-111">-CdnEndpoint</span></span>
<span data-ttu-id="cf1da-112">Specifica l'endpoint avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1da-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cf1da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1da-113">-DefaultProfile</span></span>
<span data-ttu-id="cf1da-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf1da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf1da-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cf1da-115">-EndpointName</span></span>
<span data-ttu-id="cf1da-116">Specifica il nome dell'endpoint avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1da-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cf1da-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf1da-117">-PassThru</span></span>
<span data-ttu-id="cf1da-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cf1da-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf1da-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cf1da-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf1da-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cf1da-120">-ProfileName</span></span>
<span data-ttu-id="cf1da-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cf1da-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="cf1da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1da-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf1da-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cf1da-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="cf1da-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf1da-124">-Confirm</span></span>
<span data-ttu-id="cf1da-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1da-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1da-126">-WhatIf</span></span>
<span data-ttu-id="cf1da-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1da-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf1da-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf1da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1da-129">CommonParameters</span></span>
<span data-ttu-id="cf1da-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1da-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1da-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf1da-132">INPUTS</span></span>

### <span data-ttu-id="cf1da-133">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="cf1da-134">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf1da-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="cf1da-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cf1da-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf1da-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf1da-136">OUTPUTS</span></span>

### <span data-ttu-id="cf1da-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf1da-137">System.Boolean</span></span>

## <span data-ttu-id="cf1da-138">Note</span><span class="sxs-lookup"><span data-stu-id="cf1da-138">NOTES</span></span>

## <span data-ttu-id="cf1da-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf1da-139">RELATED LINKS</span></span>

[<span data-ttu-id="cf1da-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cf1da-141">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cf1da-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cf1da-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cf1da-144">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1da-144">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


