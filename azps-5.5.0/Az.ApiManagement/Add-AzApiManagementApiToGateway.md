---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205851"
---
# <span data-ttu-id="2acdd-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="2acdd-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="2acdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2acdd-102">SYNOPSIS</span></span>
<span data-ttu-id="2acdd-103">Collega un'API a un gateway.</span><span class="sxs-lookup"><span data-stu-id="2acdd-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="2acdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2acdd-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2acdd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2acdd-105">DESCRIPTION</span></span>
<span data-ttu-id="2acdd-106">Il cmdlet **Add-AzApiManagementApiToGateway** aggiunge un'API di Gestione API Azure a un gateway.</span><span class="sxs-lookup"><span data-stu-id="2acdd-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="2acdd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2acdd-107">EXAMPLES</span></span>

### <span data-ttu-id="2acdd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2acdd-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="2acdd-109">Questo comando aggiunge l'API specificata al gateway specificato.</span><span class="sxs-lookup"><span data-stu-id="2acdd-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="2acdd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2acdd-110">PARAMETERS</span></span>

### <span data-ttu-id="2acdd-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2acdd-111">-ApiId</span></span>
<span data-ttu-id="2acdd-112">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="2acdd-112">Identifier of existing API.</span></span>
<span data-ttu-id="2acdd-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2acdd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2acdd-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2acdd-114">-Context</span></span>
<span data-ttu-id="2acdd-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2acdd-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2acdd-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2acdd-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2acdd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acdd-117">-DefaultProfile</span></span>
<span data-ttu-id="2acdd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2acdd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acdd-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2acdd-119">-GatewayId</span></span>
<span data-ttu-id="2acdd-120">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="2acdd-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="2acdd-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2acdd-121">This parameter is required.</span></span>

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

### <span data-ttu-id="2acdd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2acdd-122">-PassThru</span></span>
<span data-ttu-id="2acdd-123">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="2acdd-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2acdd-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2acdd-124">This parameter is optional.</span></span>
<span data-ttu-id="2acdd-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2acdd-125">Default value is false.</span></span>

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

### <span data-ttu-id="2acdd-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2acdd-126">-ProvisioningState</span></span>
<span data-ttu-id="2acdd-127">Stato provisioning (creato).</span><span class="sxs-lookup"><span data-stu-id="2acdd-127">Provisioning State (Created).</span></span>
<span data-ttu-id="2acdd-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2acdd-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2acdd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2acdd-129">-Confirm</span></span>
<span data-ttu-id="2acdd-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2acdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2acdd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acdd-131">-WhatIf</span></span>
<span data-ttu-id="2acdd-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acdd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2acdd-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acdd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2acdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acdd-134">CommonParameters</span></span>
<span data-ttu-id="2acdd-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acdd-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2acdd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acdd-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="2acdd-137">INPUTS</span></span>

### <span data-ttu-id="2acdd-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2acdd-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2acdd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2acdd-139">System.String</span></span>

### <span data-ttu-id="2acdd-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2acdd-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2acdd-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2acdd-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2acdd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2acdd-142">OUTPUTS</span></span>

### <span data-ttu-id="2acdd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2acdd-143">System.Boolean</span></span>

## <span data-ttu-id="2acdd-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="2acdd-144">NOTES</span></span>

## <span data-ttu-id="2acdd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2acdd-145">RELATED LINKS</span></span>

[<span data-ttu-id="2acdd-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="2acdd-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)