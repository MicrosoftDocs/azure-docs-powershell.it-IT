---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018681"
---
# <span data-ttu-id="d4ab6-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d4ab6-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d4ab6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ab6-103">Disabilita il dominio personalizzato HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="d4ab6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4ab6-104">SYNTAX</span></span>

### <span data-ttu-id="d4ab6-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4ab6-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4ab6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ab6-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4ab6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ab6-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ab6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="d4ab6-109">Il cmdlet **Disable-AzCdnCustomDomainHttps Disabilita** il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d4ab6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4ab6-110">EXAMPLES</span></span>

### <span data-ttu-id="d4ab6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4ab6-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d4ab6-112">Disabilitare il recapito sicuro del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d4ab6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4ab6-113">PARAMETERS</span></span>

### <span data-ttu-id="d4ab6-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d4ab6-114">-CustomDomainName</span></span>
<span data-ttu-id="d4ab6-115">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d4ab6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ab6-116">-DefaultProfile</span></span>
<span data-ttu-id="d4ab6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4ab6-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d4ab6-118">-EndpointName</span></span>
<span data-ttu-id="d4ab6-119">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d4ab6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4ab6-120">-InputObject</span></span>
<span data-ttu-id="d4ab6-121">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d4ab6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4ab6-122">-PassThru</span></span>
<span data-ttu-id="d4ab6-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d4ab6-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d4ab6-124">-ProfileName</span></span>
<span data-ttu-id="d4ab6-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d4ab6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ab6-126">-ResourceGroupName</span></span>
<span data-ttu-id="d4ab6-127">Gruppo risorse del profilo CDN di Azure</span><span class="sxs-lookup"><span data-stu-id="d4ab6-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d4ab6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4ab6-128">-ResourceId</span></span>
<span data-ttu-id="d4ab6-129">ResourceId del dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="d4ab6-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d4ab6-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4ab6-130">-Confirm</span></span>
<span data-ttu-id="d4ab6-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ab6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ab6-132">-WhatIf</span></span>
<span data-ttu-id="d4ab6-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ab6-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ab6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ab6-135">CommonParameters</span></span>
<span data-ttu-id="d4ab6-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ab6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ab6-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4ab6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ab6-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4ab6-138">INPUTS</span></span>

### <span data-ttu-id="d4ab6-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d4ab6-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d4ab6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ab6-140">System.String</span></span>

## <span data-ttu-id="d4ab6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4ab6-141">OUTPUTS</span></span>

### <span data-ttu-id="d4ab6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4ab6-142">System.Boolean</span></span>

## <span data-ttu-id="d4ab6-143">Note</span><span class="sxs-lookup"><span data-stu-id="d4ab6-143">NOTES</span></span>

## <span data-ttu-id="d4ab6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4ab6-144">RELATED LINKS</span></span>
