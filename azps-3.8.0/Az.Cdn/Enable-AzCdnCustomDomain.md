---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 9cf4633f464316d41034a0cb2d79384e229bcf4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018768"
---
# <span data-ttu-id="c30c3-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c30c3-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c30c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c30c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c30c3-103">Abilita HTTPS di dominio personalizzato (deprecato).</span><span class="sxs-lookup"><span data-stu-id="c30c3-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="c30c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c30c3-104">SYNTAX</span></span>

### <span data-ttu-id="c30c3-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c30c3-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c30c3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c30c3-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c30c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c30c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c30c3-108">Il cmdlet **Enable-AzCdnCustomDomain** Abilita il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="c30c3-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="c30c3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c30c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c30c3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c30c3-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="c30c3-111">Abilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c30c3-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="c30c3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c30c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c30c3-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c30c3-113">-CustomDomainName</span></span>
<span data-ttu-id="c30c3-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c30c3-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="c30c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30c3-115">-DefaultProfile</span></span>
<span data-ttu-id="c30c3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c30c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c30c3-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c30c3-117">-EndpointName</span></span>
<span data-ttu-id="c30c3-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="c30c3-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c30c3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c30c3-119">-InputObject</span></span>
<span data-ttu-id="c30c3-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c30c3-120">The custom domain object.</span></span>

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

### <span data-ttu-id="c30c3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c30c3-121">-PassThru</span></span>
<span data-ttu-id="c30c3-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="c30c3-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="c30c3-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c30c3-123">-ProfileName</span></span>
<span data-ttu-id="c30c3-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="c30c3-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c30c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="c30c3-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="c30c3-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c30c3-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c30c3-127">-Confirm</span></span>
<span data-ttu-id="c30c3-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c30c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c30c3-129">-WhatIf</span></span>
<span data-ttu-id="c30c3-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c30c3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c30c3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c30c3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30c3-132">CommonParameters</span></span>
<span data-ttu-id="c30c3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30c3-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c30c3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30c3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c30c3-135">INPUTS</span></span>

### <span data-ttu-id="c30c3-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c30c3-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c30c3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c30c3-137">OUTPUTS</span></span>

### <span data-ttu-id="c30c3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c30c3-138">System.Boolean</span></span>

## <span data-ttu-id="c30c3-139">Note</span><span class="sxs-lookup"><span data-stu-id="c30c3-139">NOTES</span></span>

## <span data-ttu-id="c30c3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c30c3-140">RELATED LINKS</span></span>