---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012845"
---
# <span data-ttu-id="3d900-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d900-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="3d900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d900-102">SYNOPSIS</span></span>
<span data-ttu-id="3d900-103">Rimuove una configurazione del nome host dal gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="3d900-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="3d900-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d900-104">SYNTAX</span></span>

### <span data-ttu-id="3d900-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d900-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d900-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d900-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d900-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d900-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d900-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d900-108">DESCRIPTION</span></span>
<span data-ttu-id="3d900-109">Il cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** rimuove una configurazione del nome host dal gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="3d900-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="3d900-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d900-110">EXAMPLES</span></span>

### <span data-ttu-id="3d900-111">Esempio 1: Rimuovere la configurazione di un nome host del gateway esistente</span><span class="sxs-lookup"><span data-stu-id="3d900-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="3d900-112">Questo comando rimuove una configurazione del nome host del gateway esistente e non richiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3d900-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="3d900-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d900-113">PARAMETERS</span></span>

### <span data-ttu-id="3d900-114">-Context</span><span class="sxs-lookup"><span data-stu-id="3d900-114">-Context</span></span>
<span data-ttu-id="3d900-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3d900-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3d900-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d900-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d900-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d900-117">-DefaultProfile</span></span>
<span data-ttu-id="3d900-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d900-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d900-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3d900-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="3d900-120">Identificatore della configurazione del nome host del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="3d900-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="3d900-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d900-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d900-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3d900-122">-GatewayId</span></span>
<span data-ttu-id="3d900-123">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="3d900-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="3d900-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d900-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d900-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d900-125">-InputObject</span></span>
<span data-ttu-id="3d900-126">Istanza di PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d900-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="3d900-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d900-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d900-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d900-128">-PassThru</span></span>
<span data-ttu-id="3d900-129">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="3d900-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3d900-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3d900-130">This parameter is optional.</span></span>
<span data-ttu-id="3d900-131">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="3d900-131">Default value is false.</span></span>

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

### <span data-ttu-id="3d900-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d900-132">-ResourceId</span></span>
<span data-ttu-id="3d900-133">Arm ResourceId di GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d900-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="3d900-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d900-134">This parameter is required.</span></span>

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

### <span data-ttu-id="3d900-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d900-135">-Confirm</span></span>
<span data-ttu-id="3d900-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d900-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d900-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d900-137">-WhatIf</span></span>
<span data-ttu-id="3d900-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d900-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d900-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d900-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d900-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d900-140">CommonParameters</span></span>
<span data-ttu-id="3d900-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d900-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d900-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d900-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d900-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d900-143">INPUTS</span></span>

### <span data-ttu-id="3d900-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d900-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d900-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3d900-145">System.String</span></span>

### <span data-ttu-id="3d900-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d900-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d900-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d900-147">OUTPUTS</span></span>

### <span data-ttu-id="3d900-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d900-148">System.Boolean</span></span>

## <span data-ttu-id="3d900-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d900-149">NOTES</span></span>

## <span data-ttu-id="3d900-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d900-150">RELATED LINKS</span></span>
