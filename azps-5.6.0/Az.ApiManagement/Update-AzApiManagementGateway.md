---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: 62131f634d049afe137b635d6a970d37e2173b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001933"
---
# <span data-ttu-id="8f4aa-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="8f4aa-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="8f4aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4aa-103">Configura un Gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="8f4aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f4aa-104">SYNTAX</span></span>

### <span data-ttu-id="8f4aa-105">ExpandedParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="8f4aa-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f4aa-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4aa-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4aa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f4aa-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4aa-109">Il cmdlet **Update-AzApiManagementGateway** configura un Gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="8f4aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f4aa-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4aa-111">Esempio 1: Configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8f4aa-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="8f4aa-112">Questo comando configura un gateway.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-112">This command configures a gateway.</span></span>

## <span data-ttu-id="8f4aa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4aa-113">PARAMETERS</span></span>

### <span data-ttu-id="8f4aa-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8f4aa-114">-Context</span></span>
<span data-ttu-id="8f4aa-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8f4aa-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4aa-117">-DefaultProfile</span></span>
<span data-ttu-id="8f4aa-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4aa-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f4aa-119">-Description</span></span>
<span data-ttu-id="8f4aa-120">Descrizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-120">Gateway description.</span></span>
<span data-ttu-id="8f4aa-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f4aa-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8f4aa-122">-GatewayId</span></span>
<span data-ttu-id="8f4aa-123">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="8f4aa-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4aa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f4aa-125">-InputObject</span></span>
<span data-ttu-id="8f4aa-126">Istanza di PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="8f4aa-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4aa-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="8f4aa-128">-LocationData</span></span>
<span data-ttu-id="8f4aa-129">Posizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-129">Gateway location.</span></span>
<span data-ttu-id="8f4aa-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4aa-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f4aa-131">-PassThru</span></span>
<span data-ttu-id="8f4aa-132">Se si specifica l'istanza di Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway che rappresenta il gateway modificato.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="8f4aa-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4aa-133">-ResourceId</span></span>
<span data-ttu-id="8f4aa-134">Arm ResourceId del gateway.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="8f4aa-135">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4aa-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f4aa-136">-Confirm</span></span>
<span data-ttu-id="8f4aa-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4aa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4aa-138">-WhatIf</span></span>
<span data-ttu-id="8f4aa-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4aa-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4aa-141">CommonParameters</span></span>
<span data-ttu-id="8f4aa-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4aa-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8f4aa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4aa-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f4aa-144">INPUTS</span></span>

### <span data-ttu-id="8f4aa-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8f4aa-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8f4aa-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4aa-146">System.String</span></span>

### <span data-ttu-id="8f4aa-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="8f4aa-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="8f4aa-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8f4aa-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8f4aa-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f4aa-149">OUTPUTS</span></span>

### <span data-ttu-id="8f4aa-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="8f4aa-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="8f4aa-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f4aa-151">NOTES</span></span>

## <span data-ttu-id="8f4aa-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f4aa-152">RELATED LINKS</span></span>
