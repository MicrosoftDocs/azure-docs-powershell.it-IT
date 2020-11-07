---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 42de9254bc5bdaf31aa965aa7bdd1512cad361f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684887"
---
# <span data-ttu-id="2edc5-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2edc5-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2edc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2edc5-102">SYNOPSIS</span></span>
<span data-ttu-id="2edc5-103">Abilita HTTPS di dominio personalizzato (deprecato).</span><span class="sxs-lookup"><span data-stu-id="2edc5-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="2edc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2edc5-104">SYNTAX</span></span>

### <span data-ttu-id="2edc5-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2edc5-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2edc5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2edc5-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edc5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2edc5-107">DESCRIPTION</span></span>
<span data-ttu-id="2edc5-108">Il cmdlet **Enable-AzCdnCustomDomain** Abilita il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="2edc5-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="2edc5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2edc5-109">EXAMPLES</span></span>

### <span data-ttu-id="2edc5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2edc5-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="2edc5-111">Abilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2edc5-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="2edc5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2edc5-112">PARAMETERS</span></span>

### <span data-ttu-id="2edc5-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2edc5-113">-CustomDomainName</span></span>
<span data-ttu-id="2edc5-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2edc5-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="2edc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edc5-115">-DefaultProfile</span></span>
<span data-ttu-id="2edc5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2edc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2edc5-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2edc5-117">-EndpointName</span></span>
<span data-ttu-id="2edc5-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2edc5-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2edc5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edc5-119">-InputObject</span></span>
<span data-ttu-id="2edc5-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2edc5-120">The custom domain object.</span></span>

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

### <span data-ttu-id="2edc5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2edc5-121">-PassThru</span></span>
<span data-ttu-id="2edc5-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="2edc5-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="2edc5-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2edc5-123">-ProfileName</span></span>
<span data-ttu-id="2edc5-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2edc5-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2edc5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edc5-125">-ResourceGroupName</span></span>
<span data-ttu-id="2edc5-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2edc5-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2edc5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2edc5-127">-Confirm</span></span>
<span data-ttu-id="2edc5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2edc5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edc5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edc5-129">-WhatIf</span></span>
<span data-ttu-id="2edc5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2edc5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2edc5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2edc5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edc5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edc5-132">CommonParameters</span></span>
<span data-ttu-id="2edc5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edc5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edc5-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edc5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edc5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2edc5-135">INPUTS</span></span>

### <span data-ttu-id="2edc5-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2edc5-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="2edc5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2edc5-137">OUTPUTS</span></span>

### <span data-ttu-id="2edc5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2edc5-138">System.Boolean</span></span>

## <span data-ttu-id="2edc5-139">Note</span><span class="sxs-lookup"><span data-stu-id="2edc5-139">NOTES</span></span>

## <span data-ttu-id="2edc5-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2edc5-140">RELATED LINKS</span></span>
