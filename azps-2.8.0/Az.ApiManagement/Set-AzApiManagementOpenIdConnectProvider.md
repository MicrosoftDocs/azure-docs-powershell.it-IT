---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675889"
---
# <span data-ttu-id="1e9fa-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1e9fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9fa-103">Modifica un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="1e9fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e9fa-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e9fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="1e9fa-106">Il cmdlet **set-AzApiManagementOpenIdConnectProvider** modifica un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="1e9fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="1e9fa-108">Esempio 1: cambiare il segreto del client per un provider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="1e9fa-109">Questo comando modifica il provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="1e9fa-110">Il comando specifica un segreto client per il provider.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="1e9fa-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e9fa-111">PARAMETERS</span></span>

### <span data-ttu-id="1e9fa-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="1e9fa-112">-ClientId</span></span>
<span data-ttu-id="1e9fa-113">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-113">Specifies the client ID of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9fa-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1e9fa-114">-ClientSecret</span></span>
<span data-ttu-id="1e9fa-115">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-115">Specifies the client secret of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9fa-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1e9fa-116">-Context</span></span>
<span data-ttu-id="1e9fa-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1e9fa-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1e9fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9fa-118">-DefaultProfile</span></span>
<span data-ttu-id="1e9fa-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e9fa-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e9fa-120">-Description</span></span>
<span data-ttu-id="1e9fa-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9fa-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="1e9fa-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="1e9fa-123">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-123">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9fa-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e9fa-124">-Name</span></span>
<span data-ttu-id="1e9fa-125">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-125">Specifies a friendly name for the provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9fa-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="1e9fa-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="1e9fa-127">Specifica un ID per il provider modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="1e9fa-128">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="1e9fa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e9fa-129">-PassThru</span></span>
<span data-ttu-id="1e9fa-130">Indica che questo cmdlet restituisce il **PsApiManagementOpenIdConnectProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1e9fa-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e9fa-131">-Confirm</span></span>
<span data-ttu-id="1e9fa-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9fa-133">-WhatIf</span></span>
<span data-ttu-id="1e9fa-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e9fa-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9fa-136">CommonParameters</span></span>
<span data-ttu-id="1e9fa-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9fa-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e9fa-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9fa-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e9fa-139">INPUTS</span></span>

### <span data-ttu-id="1e9fa-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1e9fa-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1e9fa-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9fa-141">System.String</span></span>

### <span data-ttu-id="1e9fa-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e9fa-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1e9fa-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e9fa-143">OUTPUTS</span></span>

### <span data-ttu-id="1e9fa-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1e9fa-145">Note</span><span class="sxs-lookup"><span data-stu-id="1e9fa-145">NOTES</span></span>

## <span data-ttu-id="1e9fa-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e9fa-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e9fa-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1e9fa-148">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1e9fa-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1e9fa-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


