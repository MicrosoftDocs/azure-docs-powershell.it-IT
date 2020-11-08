---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032009"
---
# <span data-ttu-id="18964-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="18964-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="18964-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18964-102">SYNOPSIS</span></span>
<span data-ttu-id="18964-103">Rimuove una configurazione hostname dal gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="18964-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="18964-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18964-104">SYNTAX</span></span>

### <span data-ttu-id="18964-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18964-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18964-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18964-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18964-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18964-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18964-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18964-108">DESCRIPTION</span></span>
<span data-ttu-id="18964-109">Il cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** rimuove una configurazione hostname dal gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="18964-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="18964-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18964-110">EXAMPLES</span></span>

### <span data-ttu-id="18964-111">Esempio 1: rimuovere una configurazione del nome host del gateway esistente</span><span class="sxs-lookup"><span data-stu-id="18964-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="18964-112">Questo comando rimuove una configurazione del nome host del gateway esistente e non chiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="18964-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="18964-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18964-113">PARAMETERS</span></span>

### <span data-ttu-id="18964-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="18964-114">-Context</span></span>
<span data-ttu-id="18964-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="18964-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="18964-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18964-116">This parameter is required.</span></span>

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

### <span data-ttu-id="18964-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18964-117">-DefaultProfile</span></span>
<span data-ttu-id="18964-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18964-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18964-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="18964-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="18964-120">Identificatore della configurazione del nome host del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="18964-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="18964-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18964-121">This parameter is required.</span></span>

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

### <span data-ttu-id="18964-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="18964-122">-GatewayId</span></span>
<span data-ttu-id="18964-123">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="18964-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="18964-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18964-124">This parameter is required.</span></span>

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

### <span data-ttu-id="18964-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18964-125">-InputObject</span></span>
<span data-ttu-id="18964-126">Istanza di PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="18964-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="18964-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18964-127">This parameter is required.</span></span>

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

### <span data-ttu-id="18964-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18964-128">-PassThru</span></span>
<span data-ttu-id="18964-129">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="18964-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="18964-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18964-130">This parameter is optional.</span></span>
<span data-ttu-id="18964-131">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="18964-131">Default value is false.</span></span>

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

### <span data-ttu-id="18964-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18964-132">-ResourceId</span></span>
<span data-ttu-id="18964-133">ResourceId ARM di GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="18964-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="18964-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="18964-134">This parameter is required.</span></span>

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

### <span data-ttu-id="18964-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18964-135">-Confirm</span></span>
<span data-ttu-id="18964-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18964-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18964-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18964-137">-WhatIf</span></span>
<span data-ttu-id="18964-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18964-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18964-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18964-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18964-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18964-140">CommonParameters</span></span>
<span data-ttu-id="18964-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18964-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18964-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18964-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18964-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18964-143">INPUTS</span></span>

### <span data-ttu-id="18964-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="18964-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="18964-145">System. String</span><span class="sxs-lookup"><span data-stu-id="18964-145">System.String</span></span>

### <span data-ttu-id="18964-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18964-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18964-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18964-147">OUTPUTS</span></span>

### <span data-ttu-id="18964-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18964-148">System.Boolean</span></span>

## <span data-ttu-id="18964-149">Note</span><span class="sxs-lookup"><span data-stu-id="18964-149">NOTES</span></span>

## <span data-ttu-id="18964-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18964-150">RELATED LINKS</span></span>
