---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507611"
---
# <span data-ttu-id="d18f4-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d18f4-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="d18f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d18f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d18f4-103">Abilita HTTPS personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d18f4-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d18f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d18f4-104">SYNTAX</span></span>

### <span data-ttu-id="d18f4-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d18f4-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d18f4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d18f4-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18f4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d18f4-107">DESCRIPTION</span></span>
<span data-ttu-id="d18f4-108">Il cmdlet **Enable-AzureRmCdnCustomDomain** Abilita il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="d18f4-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d18f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d18f4-109">EXAMPLES</span></span>

### <span data-ttu-id="d18f4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d18f4-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="d18f4-111">Abilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d18f4-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="d18f4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d18f4-112">PARAMETERS</span></span>

### <span data-ttu-id="d18f4-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d18f4-113">-CustomDomainName</span></span>
<span data-ttu-id="d18f4-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d18f4-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d18f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18f4-115">-DefaultProfile</span></span>
<span data-ttu-id="d18f4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d18f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18f4-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d18f4-117">-EndpointName</span></span>
<span data-ttu-id="d18f4-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d18f4-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d18f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d18f4-119">-InputObject</span></span>
<span data-ttu-id="d18f4-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d18f4-120">The custom domain object.</span></span>

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

### <span data-ttu-id="d18f4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d18f4-121">-PassThru</span></span>
<span data-ttu-id="d18f4-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="d18f4-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="d18f4-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d18f4-123">-ProfileName</span></span>
<span data-ttu-id="d18f4-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d18f4-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d18f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="d18f4-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="d18f4-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d18f4-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d18f4-127">-Confirm</span></span>
<span data-ttu-id="d18f4-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18f4-129">-WhatIf</span></span>
<span data-ttu-id="d18f4-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d18f4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d18f4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d18f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18f4-132">CommonParameters</span></span>
<span data-ttu-id="d18f4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18f4-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18f4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18f4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d18f4-135">INPUTS</span></span>

### <span data-ttu-id="d18f4-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d18f4-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="d18f4-137">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d18f4-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d18f4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d18f4-138">OUTPUTS</span></span>

### <span data-ttu-id="d18f4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d18f4-139">System.Boolean</span></span>

## <span data-ttu-id="d18f4-140">Note</span><span class="sxs-lookup"><span data-stu-id="d18f4-140">NOTES</span></span>

## <span data-ttu-id="d18f4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d18f4-141">RELATED LINKS</span></span>
