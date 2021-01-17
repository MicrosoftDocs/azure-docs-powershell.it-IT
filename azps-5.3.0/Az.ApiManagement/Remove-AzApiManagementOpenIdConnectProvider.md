---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382017"
---
# <span data-ttu-id="541e2-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="541e2-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="541e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="541e2-102">SYNOPSIS</span></span>
<span data-ttu-id="541e2-103">Rimuove un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="541e2-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="541e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="541e2-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="541e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="541e2-105">DESCRIPTION</span></span>
<span data-ttu-id="541e2-106">Il cmdlet **Remove-AzApiManagementOpenIdConnectProvider** rimuove un provider OpenID Connect per la gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="541e2-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="541e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="541e2-107">EXAMPLES</span></span>

### <span data-ttu-id="541e2-108">Esempio 1: rimuovere un provider</span><span class="sxs-lookup"><span data-stu-id="541e2-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="541e2-109">Questo comando rimuove un provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="541e2-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="541e2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="541e2-110">PARAMETERS</span></span>

### <span data-ttu-id="541e2-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="541e2-111">-Context</span></span>
<span data-ttu-id="541e2-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="541e2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="541e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541e2-113">-DefaultProfile</span></span>
<span data-ttu-id="541e2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="541e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="541e2-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="541e2-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="541e2-116">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="541e2-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="541e2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="541e2-117">-PassThru</span></span>
<span data-ttu-id="541e2-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="541e2-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="541e2-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="541e2-119">-Confirm</span></span>
<span data-ttu-id="541e2-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="541e2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="541e2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="541e2-121">-WhatIf</span></span>
<span data-ttu-id="541e2-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="541e2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="541e2-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="541e2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="541e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541e2-124">CommonParameters</span></span>
<span data-ttu-id="541e2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="541e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541e2-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="541e2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541e2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="541e2-127">INPUTS</span></span>

### <span data-ttu-id="541e2-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="541e2-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="541e2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="541e2-129">System.String</span></span>

### <span data-ttu-id="541e2-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="541e2-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="541e2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="541e2-131">OUTPUTS</span></span>

### <span data-ttu-id="541e2-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="541e2-132">System.Boolean</span></span>

## <span data-ttu-id="541e2-133">Note</span><span class="sxs-lookup"><span data-stu-id="541e2-133">NOTES</span></span>

## <span data-ttu-id="541e2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="541e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="541e2-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="541e2-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="541e2-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="541e2-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="541e2-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="541e2-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


