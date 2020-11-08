---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199716"
---
# <span data-ttu-id="2a00b-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2a00b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a00b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a00b-103">Rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2a00b-103">Removes a custom domain.</span></span>

## <span data-ttu-id="2a00b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a00b-104">SYNTAX</span></span>

### <span data-ttu-id="2a00b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a00b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a00b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a00b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a00b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a00b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a00b-108">Il cmdlet **Remove-AzCdnCustomDomain** rimuove il dominio personalizzato da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="2a00b-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2a00b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a00b-109">EXAMPLES</span></span>

## <span data-ttu-id="2a00b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a00b-110">PARAMETERS</span></span>

### <span data-ttu-id="2a00b-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-111">-CdnCustomDomain</span></span>
<span data-ttu-id="2a00b-112">Specifica il dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a00b-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a00b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2a00b-113">-CustomDomainName</span></span>
<span data-ttu-id="2a00b-114">Specifica il nome della risorsa del dominio personalizzato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a00b-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a00b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a00b-115">-DefaultProfile</span></span>
<span data-ttu-id="2a00b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2a00b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a00b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2a00b-117">-EndpointName</span></span>
<span data-ttu-id="2a00b-118">Specifica il nome dell'endpoint da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2a00b-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="2a00b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a00b-119">-PassThru</span></span>
<span data-ttu-id="2a00b-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2a00b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a00b-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2a00b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a00b-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2a00b-122">-ProfileName</span></span>
<span data-ttu-id="2a00b-123">Specifica il nome del profilo da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2a00b-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="2a00b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a00b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a00b-125">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2a00b-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="2a00b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a00b-126">-Confirm</span></span>
<span data-ttu-id="2a00b-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a00b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a00b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a00b-128">-WhatIf</span></span>
<span data-ttu-id="2a00b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a00b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a00b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a00b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a00b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a00b-131">CommonParameters</span></span>
<span data-ttu-id="2a00b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a00b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a00b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a00b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a00b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a00b-134">INPUTS</span></span>

### <span data-ttu-id="2a00b-135">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="2a00b-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a00b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a00b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a00b-137">OUTPUTS</span></span>

### <span data-ttu-id="2a00b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a00b-138">System.Boolean</span></span>

## <span data-ttu-id="2a00b-139">Note</span><span class="sxs-lookup"><span data-stu-id="2a00b-139">NOTES</span></span>

## <span data-ttu-id="2a00b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a00b-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a00b-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="2a00b-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="2a00b-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a00b-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


