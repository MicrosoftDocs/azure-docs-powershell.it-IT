---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3d7d6600e7e26202c920499a615f4124767c830c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988510"
---
# <span data-ttu-id="7a671-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7a671-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="7a671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a671-102">SYNOPSIS</span></span>
<span data-ttu-id="7a671-103">Rimuove un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="7a671-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="7a671-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a671-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a671-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a671-105">DESCRIPTION</span></span>
<span data-ttu-id="7a671-106">Il cmdlet **Remove-AzApiManagementOpenIdConnectProvider** rimuove un provider OpenID Connect per Gestione API Azure.</span><span class="sxs-lookup"><span data-stu-id="7a671-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="7a671-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a671-107">EXAMPLES</span></span>

### <span data-ttu-id="7a671-108">Esempio 1: Rimuovere un provider</span><span class="sxs-lookup"><span data-stu-id="7a671-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="7a671-109">Questo comando rimuove un provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="7a671-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="7a671-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a671-110">PARAMETERS</span></span>

### <span data-ttu-id="7a671-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7a671-111">-Context</span></span>
<span data-ttu-id="7a671-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7a671-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a671-113">-DefaultProfile</span></span>
<span data-ttu-id="7a671-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a671-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="7a671-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="7a671-116">Specifica un ID del provider rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a671-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a671-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a671-117">-PassThru</span></span>
<span data-ttu-id="7a671-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione riesce o se $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7a671-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a671-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a671-119">-Confirm</span></span>
<span data-ttu-id="7a671-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a671-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a671-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a671-121">-WhatIf</span></span>
<span data-ttu-id="7a671-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a671-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a671-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a671-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a671-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a671-124">CommonParameters</span></span>
<span data-ttu-id="7a671-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a671-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a671-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a671-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a671-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a671-127">INPUTS</span></span>

### <span data-ttu-id="7a671-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a671-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a671-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7a671-129">System.String</span></span>

### <span data-ttu-id="7a671-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a671-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a671-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a671-131">OUTPUTS</span></span>

### <span data-ttu-id="7a671-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a671-132">System.Boolean</span></span>

## <span data-ttu-id="7a671-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a671-133">NOTES</span></span>

## <span data-ttu-id="7a671-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a671-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a671-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7a671-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="7a671-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7a671-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="7a671-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="7a671-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


