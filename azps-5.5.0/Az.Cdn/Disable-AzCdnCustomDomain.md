---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200831"
---
# <span data-ttu-id="26845-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="26845-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="26845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26845-102">SYNOPSIS</span></span>
<span data-ttu-id="26845-103">Disabilita il dominio personalizzato HTTPS (deprecato).</span><span class="sxs-lookup"><span data-stu-id="26845-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="26845-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26845-104">SYNTAX</span></span>

### <span data-ttu-id="26845-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26845-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26845-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26845-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26845-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26845-107">DESCRIPTION</span></span>
<span data-ttu-id="26845-108">Il cmdlet **Disable-AzCdnCustomDomain** disabilita la distribuzione https protetta di un dominio personalizzato della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="26845-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="26845-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26845-109">EXAMPLES</span></span>

### <span data-ttu-id="26845-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26845-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="26845-111">Disabilitare la distribuzione https del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="26845-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="26845-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26845-112">PARAMETERS</span></span>

### <span data-ttu-id="26845-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="26845-113">-CustomDomainName</span></span>
<span data-ttu-id="26845-114">Nome visualizzato del dominio personalizzato della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="26845-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="26845-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26845-115">-DefaultProfile</span></span>
<span data-ttu-id="26845-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26845-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26845-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="26845-117">-EndpointName</span></span>
<span data-ttu-id="26845-118">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="26845-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="26845-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26845-119">-InputObject</span></span>
<span data-ttu-id="26845-120">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="26845-120">The custom domain object.</span></span>

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

### <span data-ttu-id="26845-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26845-121">-PassThru</span></span>
<span data-ttu-id="26845-122">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="26845-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="26845-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="26845-123">-ProfileName</span></span>
<span data-ttu-id="26845-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="26845-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="26845-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26845-125">-ResourceGroupName</span></span>
<span data-ttu-id="26845-126">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="26845-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="26845-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26845-127">-Confirm</span></span>
<span data-ttu-id="26845-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26845-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26845-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26845-129">-WhatIf</span></span>
<span data-ttu-id="26845-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26845-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26845-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26845-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26845-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26845-132">CommonParameters</span></span>
<span data-ttu-id="26845-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26845-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26845-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26845-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26845-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="26845-135">INPUTS</span></span>

### <span data-ttu-id="26845-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="26845-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="26845-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26845-137">OUTPUTS</span></span>

### <span data-ttu-id="26845-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26845-138">System.Boolean</span></span>

## <span data-ttu-id="26845-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="26845-139">NOTES</span></span>

## <span data-ttu-id="26845-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26845-140">RELATED LINKS</span></span>
