---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182375"
---
# <span data-ttu-id="e59b7-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e59b7-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e59b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e59b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e59b7-103">Crea una configurazione del nome host per il Gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="e59b7-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="e59b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e59b7-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e59b7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e59b7-105">DESCRIPTION</span></span>
<span data-ttu-id="e59b7-106">Il cmdlet **New-AzApiManagementGatewayHostnameConfiguration crea** una configurazione del nome host per il gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="e59b7-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="e59b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e59b7-107">EXAMPLES</span></span>

### <span data-ttu-id="e59b7-108">Esempio 1: Creare una configurazione del nome host per il gateway esistente</span><span class="sxs-lookup"><span data-stu-id="e59b7-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="e59b7-109">Questo comando crea una configurazione del nome host "h01" per un gateway "g01".</span><span class="sxs-lookup"><span data-stu-id="e59b7-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="e59b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e59b7-110">PARAMETERS</span></span>

### <span data-ttu-id="e59b7-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="e59b7-111">-CertificateResourceId</span></span>
<span data-ttu-id="e59b7-112">Un identificatore di risorsa per l'ID certificato esistente. Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e59b7-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="e59b7-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e59b7-113">-Context</span></span>
<span data-ttu-id="e59b7-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e59b7-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e59b7-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e59b7-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e59b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59b7-116">-DefaultProfile</span></span>
<span data-ttu-id="e59b7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e59b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59b7-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e59b7-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="e59b7-119">Identificatore della connessione con il nome host del nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="e59b7-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="e59b7-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e59b7-120">This parameter is optional.</span></span>
<span data-ttu-id="e59b7-121">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="e59b7-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e59b7-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e59b7-122">-GatewayId</span></span>
<span data-ttu-id="e59b7-123">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="e59b7-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="e59b7-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e59b7-124">This parameter is required.</span></span>

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

### <span data-ttu-id="e59b7-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="e59b7-125">-Hostname</span></span>
<span data-ttu-id="e59b7-126">Nome host.</span><span class="sxs-lookup"><span data-stu-id="e59b7-126">Hostname.</span></span>
<span data-ttu-id="e59b7-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e59b7-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e59b7-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e59b7-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="e59b7-129">Flag per applicare NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="e59b7-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="e59b7-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e59b7-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e59b7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e59b7-131">-Confirm</span></span>
<span data-ttu-id="e59b7-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e59b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59b7-133">-WhatIf</span></span>
<span data-ttu-id="e59b7-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e59b7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e59b7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e59b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59b7-136">CommonParameters</span></span>
<span data-ttu-id="e59b7-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59b7-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e59b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59b7-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="e59b7-139">INPUTS</span></span>

### <span data-ttu-id="e59b7-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e59b7-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e59b7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e59b7-141">System.String</span></span>

### <span data-ttu-id="e59b7-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e59b7-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e59b7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e59b7-143">OUTPUTS</span></span>

### <span data-ttu-id="e59b7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e59b7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="e59b7-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e59b7-145">NOTES</span></span>

## <span data-ttu-id="e59b7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e59b7-146">RELATED LINKS</span></span>
