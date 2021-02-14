---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181879"
---
# <span data-ttu-id="bbb87-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="bbb87-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="bbb87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb87-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb87-103">Disabilita il dominio personalizzato HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bbb87-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="bbb87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbb87-104">SYNTAX</span></span>

### <span data-ttu-id="bbb87-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbb87-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbb87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbb87-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbb87-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbb87-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb87-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbb87-108">DESCRIPTION</span></span>
<span data-ttu-id="bbb87-109">Il cmdlet **Disable-AzCdnCustomDomainHttps** disabilita la distribuzione https protetta di un dominio personalizzato della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="bbb87-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="bbb87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbb87-110">EXAMPLES</span></span>

### <span data-ttu-id="bbb87-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbb87-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="bbb87-112">Disabilitare la distribuzione sicura del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bbb87-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="bbb87-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbb87-113">PARAMETERS</span></span>

### <span data-ttu-id="bbb87-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bbb87-114">-CustomDomainName</span></span>
<span data-ttu-id="bbb87-115">Nome visualizzato del dominio personalizzato della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb87-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="bbb87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb87-116">-DefaultProfile</span></span>
<span data-ttu-id="bbb87-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb87-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bbb87-118">-EndpointName</span></span>
<span data-ttu-id="bbb87-119">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb87-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bbb87-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbb87-120">-InputObject</span></span>
<span data-ttu-id="bbb87-121">L'oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bbb87-121">The custom domain object.</span></span>

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

### <span data-ttu-id="bbb87-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbb87-122">-PassThru</span></span>
<span data-ttu-id="bbb87-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="bbb87-123">Return object if specified.</span></span>

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

### <span data-ttu-id="bbb87-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bbb87-124">-ProfileName</span></span>
<span data-ttu-id="bbb87-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb87-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bbb87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb87-126">-ResourceGroupName</span></span>
<span data-ttu-id="bbb87-127">Gruppo di risorse del profilo CDN di Azure</span><span class="sxs-lookup"><span data-stu-id="bbb87-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="bbb87-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbb87-128">-ResourceId</span></span>
<span data-ttu-id="bbb87-129">ResourceId del dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="bbb87-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb87-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbb87-130">-Confirm</span></span>
<span data-ttu-id="bbb87-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb87-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb87-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb87-132">-WhatIf</span></span>
<span data-ttu-id="bbb87-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbb87-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb87-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbb87-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb87-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb87-135">CommonParameters</span></span>
<span data-ttu-id="bbb87-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb87-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb87-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbb87-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb87-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbb87-138">INPUTS</span></span>

### <span data-ttu-id="bbb87-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bbb87-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="bbb87-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bbb87-140">System.String</span></span>

## <span data-ttu-id="bbb87-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbb87-141">OUTPUTS</span></span>

### <span data-ttu-id="bbb87-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbb87-142">System.Boolean</span></span>

## <span data-ttu-id="bbb87-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbb87-143">NOTES</span></span>

## <span data-ttu-id="bbb87-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbb87-144">RELATED LINKS</span></span>
