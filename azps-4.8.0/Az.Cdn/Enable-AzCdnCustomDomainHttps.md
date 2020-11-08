---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189174"
---
# <span data-ttu-id="d2afe-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d2afe-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d2afe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2afe-102">SYNOPSIS</span></span>
<span data-ttu-id="d2afe-103">Abilita HTTPS personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d2afe-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="d2afe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2afe-104">SYNTAX</span></span>

### <span data-ttu-id="d2afe-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2afe-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2afe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2afe-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2afe-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2afe-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2afe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2afe-108">DESCRIPTION</span></span>
<span data-ttu-id="d2afe-109">Il cmdlet **Enable-AzCdnCustomDomainHttps** Abilita il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="d2afe-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d2afe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2afe-110">EXAMPLES</span></span>

### <span data-ttu-id="d2afe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2afe-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d2afe-112">Abilitare il recapito sicuro del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d2afe-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d2afe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2afe-113">PARAMETERS</span></span>

### <span data-ttu-id="d2afe-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d2afe-114">-CustomDomainName</span></span>
<span data-ttu-id="d2afe-115">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d2afe-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d2afe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2afe-116">-DefaultProfile</span></span>
<span data-ttu-id="d2afe-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2afe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2afe-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d2afe-118">-EndpointName</span></span>
<span data-ttu-id="d2afe-119">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2afe-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d2afe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2afe-120">-InputObject</span></span>
<span data-ttu-id="d2afe-121">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d2afe-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d2afe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2afe-122">-PassThru</span></span>
<span data-ttu-id="d2afe-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="d2afe-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d2afe-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d2afe-124">-ProfileName</span></span>
<span data-ttu-id="d2afe-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2afe-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d2afe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2afe-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2afe-127">Gruppo risorse del profilo CDN di Azure</span><span class="sxs-lookup"><span data-stu-id="d2afe-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d2afe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2afe-128">-ResourceId</span></span>
<span data-ttu-id="d2afe-129">ResourceId del dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="d2afe-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d2afe-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2afe-130">-Confirm</span></span>
<span data-ttu-id="d2afe-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2afe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2afe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2afe-132">-WhatIf</span></span>
<span data-ttu-id="d2afe-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2afe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2afe-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2afe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2afe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2afe-135">CommonParameters</span></span>
<span data-ttu-id="d2afe-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2afe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2afe-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2afe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2afe-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2afe-138">INPUTS</span></span>

### <span data-ttu-id="d2afe-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d2afe-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d2afe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d2afe-140">System.String</span></span>

## <span data-ttu-id="d2afe-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2afe-141">OUTPUTS</span></span>

### <span data-ttu-id="d2afe-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2afe-142">System.Boolean</span></span>

## <span data-ttu-id="d2afe-143">Note</span><span class="sxs-lookup"><span data-stu-id="d2afe-143">NOTES</span></span>

## <span data-ttu-id="d2afe-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2afe-144">RELATED LINKS</span></span>
