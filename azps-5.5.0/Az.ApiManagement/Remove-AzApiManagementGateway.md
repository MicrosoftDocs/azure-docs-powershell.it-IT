---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178047"
---
# <span data-ttu-id="b9543-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b9543-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="b9543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9543-102">SYNOPSIS</span></span>
<span data-ttu-id="b9543-103">Scollega un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="b9543-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="b9543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9543-104">SYNTAX</span></span>

### <span data-ttu-id="b9543-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9543-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9543-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9543-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9543-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9543-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9543-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9543-108">DESCRIPTION</span></span>
<span data-ttu-id="b9543-109">Il cmdlet **Remove-AzApiManagementGateway** disconnette un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="b9543-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="b9543-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9543-110">EXAMPLES</span></span>

### <span data-ttu-id="b9543-111">Esempio 1: Rimuovere un gateway esistente</span><span class="sxs-lookup"><span data-stu-id="b9543-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="b9543-112">Questo comando rimuove un gateway esistente e non richiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b9543-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="b9543-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9543-113">PARAMETERS</span></span>

### <span data-ttu-id="b9543-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b9543-114">-Context</span></span>
<span data-ttu-id="b9543-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b9543-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b9543-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9543-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b9543-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9543-117">-DefaultProfile</span></span>
<span data-ttu-id="b9543-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9543-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9543-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b9543-119">-GatewayId</span></span>
<span data-ttu-id="b9543-120">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="b9543-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="b9543-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9543-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b9543-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9543-122">-InputObject</span></span>
<span data-ttu-id="b9543-123">Istanza di PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="b9543-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="b9543-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9543-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9543-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9543-125">-PassThru</span></span>
<span data-ttu-id="b9543-126">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="b9543-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b9543-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b9543-127">This parameter is optional.</span></span>
<span data-ttu-id="b9543-128">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="b9543-128">Default value is false.</span></span>

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

### <span data-ttu-id="b9543-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9543-129">-ResourceId</span></span>
<span data-ttu-id="b9543-130">Arm ResourceId del gateway.</span><span class="sxs-lookup"><span data-stu-id="b9543-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="b9543-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9543-131">This parameter is required.</span></span>

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

### <span data-ttu-id="b9543-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9543-132">-Confirm</span></span>
<span data-ttu-id="b9543-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9543-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9543-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9543-134">-WhatIf</span></span>
<span data-ttu-id="b9543-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9543-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9543-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9543-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9543-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9543-137">CommonParameters</span></span>
<span data-ttu-id="b9543-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9543-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9543-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9543-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9543-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9543-140">INPUTS</span></span>

### <span data-ttu-id="b9543-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9543-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9543-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b9543-142">System.String</span></span>

### <span data-ttu-id="b9543-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b9543-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9543-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9543-144">OUTPUTS</span></span>

### <span data-ttu-id="b9543-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9543-145">System.Boolean</span></span>

## <span data-ttu-id="b9543-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9543-146">NOTES</span></span>

## <span data-ttu-id="b9543-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9543-147">RELATED LINKS</span></span>
