---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 5f7ad20d2a6243d52346600d4ae37e5a0505c8e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675574"
---
# <span data-ttu-id="db94d-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="db94d-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="db94d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db94d-102">SYNOPSIS</span></span>
<span data-ttu-id="db94d-103">Abilita HTTPS di dominio personalizzato (deprecato).</span><span class="sxs-lookup"><span data-stu-id="db94d-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="db94d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db94d-104">SYNTAX</span></span>

### <span data-ttu-id="db94d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db94d-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db94d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db94d-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db94d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db94d-107">DESCRIPTION</span></span>
<span data-ttu-id="db94d-108">Il cmdlet **Enable-AzCdnCustomDomain** Abilita il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="db94d-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="db94d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db94d-109">EXAMPLES</span></span>

### <span data-ttu-id="db94d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db94d-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="db94d-111">Abilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="db94d-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="db94d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db94d-112">PARAMETERS</span></span>

### <span data-ttu-id="db94d-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="db94d-113">-CustomDomainName</span></span>
<span data-ttu-id="db94d-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="db94d-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="db94d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db94d-115">-DefaultProfile</span></span>
<span data-ttu-id="db94d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db94d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db94d-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="db94d-117">-EndpointName</span></span>
<span data-ttu-id="db94d-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="db94d-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="db94d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db94d-119">-InputObject</span></span>
<span data-ttu-id="db94d-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="db94d-120">The custom domain object.</span></span>

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

### <span data-ttu-id="db94d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db94d-121">-PassThru</span></span>
<span data-ttu-id="db94d-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="db94d-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="db94d-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="db94d-123">-ProfileName</span></span>
<span data-ttu-id="db94d-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="db94d-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="db94d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db94d-125">-ResourceGroupName</span></span>
<span data-ttu-id="db94d-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="db94d-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="db94d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db94d-127">-Confirm</span></span>
<span data-ttu-id="db94d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db94d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db94d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db94d-129">-WhatIf</span></span>
<span data-ttu-id="db94d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db94d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db94d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db94d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db94d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db94d-132">CommonParameters</span></span>
<span data-ttu-id="db94d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db94d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db94d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db94d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db94d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db94d-135">INPUTS</span></span>

### <span data-ttu-id="db94d-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="db94d-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="db94d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db94d-137">OUTPUTS</span></span>

### <span data-ttu-id="db94d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db94d-138">System.Boolean</span></span>

## <span data-ttu-id="db94d-139">Note</span><span class="sxs-lookup"><span data-stu-id="db94d-139">NOTES</span></span>

## <span data-ttu-id="db94d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db94d-140">RELATED LINKS</span></span>