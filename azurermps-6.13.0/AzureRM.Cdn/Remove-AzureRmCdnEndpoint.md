---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517527"
---
# <span data-ttu-id="9f43e-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9f43e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f43e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f43e-103">Rimuove un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="9f43e-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f43e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f43e-104">SYNTAX</span></span>

### <span data-ttu-id="9f43e-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f43e-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f43e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f43e-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f43e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f43e-107">DESCRIPTION</span></span>
<span data-ttu-id="9f43e-108">Il cmdlet **Remove-AzureRmCdnEndpoint** rimuove un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="9f43e-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9f43e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f43e-109">EXAMPLES</span></span>

## <span data-ttu-id="9f43e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f43e-110">PARAMETERS</span></span>

### <span data-ttu-id="9f43e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-111">-CdnEndpoint</span></span>
<span data-ttu-id="9f43e-112">Specifica l'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f43e-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9f43e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f43e-113">-DefaultProfile</span></span>
<span data-ttu-id="9f43e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9f43e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f43e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9f43e-115">-EndpointName</span></span>
<span data-ttu-id="9f43e-116">Specifica il nome dell'endpoint rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f43e-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9f43e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9f43e-117">-Force</span></span>
<span data-ttu-id="9f43e-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9f43e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f43e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f43e-119">-PassThru</span></span>
<span data-ttu-id="9f43e-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9f43e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f43e-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9f43e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f43e-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9f43e-122">-ProfileName</span></span>
<span data-ttu-id="9f43e-123">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f43e-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9f43e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f43e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f43e-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f43e-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9f43e-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f43e-126">-Confirm</span></span>
<span data-ttu-id="9f43e-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f43e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f43e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f43e-128">-WhatIf</span></span>
<span data-ttu-id="9f43e-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f43e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f43e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f43e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f43e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f43e-131">CommonParameters</span></span>
<span data-ttu-id="9f43e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f43e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f43e-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f43e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f43e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f43e-134">INPUTS</span></span>

### <span data-ttu-id="9f43e-135">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="9f43e-136">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f43e-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="9f43e-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f43e-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f43e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f43e-138">OUTPUTS</span></span>

### <span data-ttu-id="9f43e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f43e-139">System.Boolean</span></span>

## <span data-ttu-id="9f43e-140">Note</span><span class="sxs-lookup"><span data-stu-id="9f43e-140">NOTES</span></span>

## <span data-ttu-id="9f43e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f43e-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f43e-142">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9f43e-143">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9f43e-144">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9f43e-145">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9f43e-146">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f43e-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


