---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517543"
---
# <span data-ttu-id="0ec69-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0ec69-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="0ec69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ec69-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec69-103">Disabilita l'HTTPS personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0ec69-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ec69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ec69-104">SYNTAX</span></span>

### <span data-ttu-id="0ec69-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ec69-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ec69-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ec69-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ec69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ec69-107">DESCRIPTION</span></span>
<span data-ttu-id="0ec69-108">Il cmdlet **Disable-AzureRmCdnCustomDomain Disabilita** il recapito HTTPS protetto di un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="0ec69-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="0ec69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ec69-109">EXAMPLES</span></span>

### <span data-ttu-id="0ec69-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ec69-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="0ec69-111">Disabilitare il recapito HTTPS del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0ec69-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="0ec69-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ec69-112">PARAMETERS</span></span>

### <span data-ttu-id="0ec69-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0ec69-113">-CustomDomainName</span></span>
<span data-ttu-id="0ec69-114">Nome visualizzato del dominio personalizzato di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="0ec69-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="0ec69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec69-115">-DefaultProfile</span></span>
<span data-ttu-id="0ec69-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ec69-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0ec69-117">-EndpointName</span></span>
<span data-ttu-id="0ec69-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec69-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0ec69-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ec69-119">-InputObject</span></span>
<span data-ttu-id="0ec69-120">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0ec69-120">The custom domain object.</span></span>

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

### <span data-ttu-id="0ec69-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ec69-121">-PassThru</span></span>
<span data-ttu-id="0ec69-122">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="0ec69-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="0ec69-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0ec69-123">-ProfileName</span></span>
<span data-ttu-id="0ec69-124">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec69-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0ec69-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec69-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ec69-126">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec69-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0ec69-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ec69-127">-Confirm</span></span>
<span data-ttu-id="0ec69-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec69-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ec69-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ec69-129">-WhatIf</span></span>
<span data-ttu-id="0ec69-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec69-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ec69-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec69-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ec69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec69-132">CommonParameters</span></span>
<span data-ttu-id="0ec69-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec69-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec69-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec69-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ec69-135">INPUTS</span></span>

### <span data-ttu-id="0ec69-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0ec69-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="0ec69-137">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ec69-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0ec69-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ec69-138">OUTPUTS</span></span>

### <span data-ttu-id="0ec69-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ec69-139">System.Boolean</span></span>

## <span data-ttu-id="0ec69-140">Note</span><span class="sxs-lookup"><span data-stu-id="0ec69-140">NOTES</span></span>

## <span data-ttu-id="0ec69-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ec69-141">RELATED LINKS</span></span>
