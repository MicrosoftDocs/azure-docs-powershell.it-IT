---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 4107ae55b42e35ae600766deb037c8c0590c8731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675577"
---
# <span data-ttu-id="4e65e-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4e65e-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4e65e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e65e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e65e-103">Disabilita il dominio personalizzato HTTPS (deprecato).</span><span class="sxs-lookup"><span data-stu-id="4e65e-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="4e65e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e65e-104">SYNTAX</span></span>

### <span data-ttu-id="4e65e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e65e-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e65e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e65e-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e65e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e65e-107">DESCRIPTION</span></span>
<span data-ttu-id="4e65e-108">Il cmdlet **Disable-AzCdnCustomDomain Disabilita** il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="4e65e-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="4e65e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e65e-109">EXAMPLES</span></span>

### <span data-ttu-id="4e65e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e65e-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="4e65e-111">Disabilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4e65e-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="4e65e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e65e-112">PARAMETERS</span></span>

### <span data-ttu-id="4e65e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4e65e-113">-CustomDomainName</span></span>
<span data-ttu-id="4e65e-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4e65e-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="4e65e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e65e-115">-DefaultProfile</span></span>
<span data-ttu-id="4e65e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e65e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e65e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4e65e-117">-EndpointName</span></span>
<span data-ttu-id="4e65e-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e65e-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4e65e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e65e-119">-InputObject</span></span>
<span data-ttu-id="4e65e-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4e65e-120">The custom domain object.</span></span>

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

### <span data-ttu-id="4e65e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e65e-121">-PassThru</span></span>
<span data-ttu-id="4e65e-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="4e65e-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="4e65e-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4e65e-123">-ProfileName</span></span>
<span data-ttu-id="4e65e-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e65e-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4e65e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e65e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e65e-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e65e-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4e65e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e65e-127">-Confirm</span></span>
<span data-ttu-id="4e65e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e65e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e65e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e65e-129">-WhatIf</span></span>
<span data-ttu-id="4e65e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e65e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e65e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e65e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e65e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e65e-132">CommonParameters</span></span>
<span data-ttu-id="4e65e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e65e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e65e-134">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e65e-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e65e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e65e-135">INPUTS</span></span>

### <span data-ttu-id="4e65e-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4e65e-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4e65e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e65e-137">OUTPUTS</span></span>

### <span data-ttu-id="4e65e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e65e-138">System.Boolean</span></span>

## <span data-ttu-id="4e65e-139">Note</span><span class="sxs-lookup"><span data-stu-id="4e65e-139">NOTES</span></span>

## <span data-ttu-id="4e65e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e65e-140">RELATED LINKS</span></span>