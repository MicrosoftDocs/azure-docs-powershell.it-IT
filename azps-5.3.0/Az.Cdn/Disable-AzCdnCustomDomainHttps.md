---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488683"
---
# <span data-ttu-id="08f21-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="08f21-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="08f21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08f21-102">SYNOPSIS</span></span>
<span data-ttu-id="08f21-103">Disabilita il dominio personalizzato HTTPS.</span><span class="sxs-lookup"><span data-stu-id="08f21-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="08f21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08f21-104">SYNTAX</span></span>

### <span data-ttu-id="08f21-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08f21-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f21-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f21-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f21-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f21-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f21-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f21-108">DESCRIPTION</span></span>
<span data-ttu-id="08f21-109">Il cmdlet **Disable-AzCdnCustomDomainHttps Disabilita** il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="08f21-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="08f21-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08f21-110">EXAMPLES</span></span>

### <span data-ttu-id="08f21-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08f21-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="08f21-112">Disabilitare il recapito sicuro del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="08f21-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="08f21-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08f21-113">PARAMETERS</span></span>

### <span data-ttu-id="08f21-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="08f21-114">-CustomDomainName</span></span>
<span data-ttu-id="08f21-115">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="08f21-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="08f21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f21-116">-DefaultProfile</span></span>
<span data-ttu-id="08f21-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08f21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f21-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="08f21-118">-EndpointName</span></span>
<span data-ttu-id="08f21-119">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="08f21-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="08f21-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08f21-120">-InputObject</span></span>
<span data-ttu-id="08f21-121">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="08f21-121">The custom domain object.</span></span>

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

### <span data-ttu-id="08f21-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08f21-122">-PassThru</span></span>
<span data-ttu-id="08f21-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="08f21-123">Return object if specified.</span></span>

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

### <span data-ttu-id="08f21-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="08f21-124">-ProfileName</span></span>
<span data-ttu-id="08f21-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="08f21-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="08f21-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f21-126">-ResourceGroupName</span></span>
<span data-ttu-id="08f21-127">Gruppo risorse del profilo CDN di Azure</span><span class="sxs-lookup"><span data-stu-id="08f21-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="08f21-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08f21-128">-ResourceId</span></span>
<span data-ttu-id="08f21-129">ResourceId del dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="08f21-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="08f21-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08f21-130">-Confirm</span></span>
<span data-ttu-id="08f21-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f21-132">-WhatIf</span></span>
<span data-ttu-id="08f21-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08f21-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f21-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08f21-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f21-135">CommonParameters</span></span>
<span data-ttu-id="08f21-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f21-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f21-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f21-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08f21-138">INPUTS</span></span>

### <span data-ttu-id="08f21-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="08f21-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="08f21-140">System. String</span><span class="sxs-lookup"><span data-stu-id="08f21-140">System.String</span></span>

## <span data-ttu-id="08f21-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08f21-141">OUTPUTS</span></span>

### <span data-ttu-id="08f21-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08f21-142">System.Boolean</span></span>

## <span data-ttu-id="08f21-143">Note</span><span class="sxs-lookup"><span data-stu-id="08f21-143">NOTES</span></span>

## <span data-ttu-id="08f21-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08f21-144">RELATED LINKS</span></span>
