---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311610"
---
# <span data-ttu-id="76f79-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="76f79-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="76f79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76f79-102">SYNOPSIS</span></span>
<span data-ttu-id="76f79-103">Configura un gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="76f79-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="76f79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76f79-104">SYNTAX</span></span>

### <span data-ttu-id="76f79-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76f79-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f79-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76f79-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f79-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76f79-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f79-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f79-108">DESCRIPTION</span></span>
<span data-ttu-id="76f79-109">Il cmdlet **Update-AzApiManagementGateway** configura un gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="76f79-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="76f79-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76f79-110">EXAMPLES</span></span>

### <span data-ttu-id="76f79-111">Esempio 1: configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="76f79-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="76f79-112">Questo comando configura un gateway.</span><span class="sxs-lookup"><span data-stu-id="76f79-112">This command configures a gateway.</span></span>

## <span data-ttu-id="76f79-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76f79-113">PARAMETERS</span></span>

### <span data-ttu-id="76f79-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="76f79-114">-Context</span></span>
<span data-ttu-id="76f79-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="76f79-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="76f79-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f79-116">This parameter is required.</span></span>

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

### <span data-ttu-id="76f79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f79-117">-DefaultProfile</span></span>
<span data-ttu-id="76f79-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f79-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f79-119">-Description</span></span>
<span data-ttu-id="76f79-120">Descrizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="76f79-120">Gateway description.</span></span>
<span data-ttu-id="76f79-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="76f79-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="76f79-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="76f79-122">-GatewayId</span></span>
<span data-ttu-id="76f79-123">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="76f79-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="76f79-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f79-124">This parameter is required.</span></span>

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

### <span data-ttu-id="76f79-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76f79-125">-InputObject</span></span>
<span data-ttu-id="76f79-126">Istanza di PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="76f79-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="76f79-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f79-127">This parameter is required.</span></span>

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

### <span data-ttu-id="76f79-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="76f79-128">-LocationData</span></span>
<span data-ttu-id="76f79-129">Posizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="76f79-129">Gateway location.</span></span>
<span data-ttu-id="76f79-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="76f79-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="76f79-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f79-131">-PassThru</span></span>
<span data-ttu-id="76f79-132">Se specificato, quindi istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway che rappresenta il gateway modificato.</span><span class="sxs-lookup"><span data-stu-id="76f79-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="76f79-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76f79-133">-ResourceId</span></span>
<span data-ttu-id="76f79-134">ARM ResourceId del gateway.</span><span class="sxs-lookup"><span data-stu-id="76f79-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="76f79-135">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="76f79-135">This parameter is required.</span></span>

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

### <span data-ttu-id="76f79-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76f79-136">-Confirm</span></span>
<span data-ttu-id="76f79-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f79-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f79-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f79-138">-WhatIf</span></span>
<span data-ttu-id="76f79-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f79-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f79-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f79-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f79-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f79-141">CommonParameters</span></span>
<span data-ttu-id="76f79-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f79-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f79-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76f79-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f79-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76f79-144">INPUTS</span></span>

### <span data-ttu-id="76f79-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76f79-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76f79-146">System. String</span><span class="sxs-lookup"><span data-stu-id="76f79-146">System.String</span></span>

### <span data-ttu-id="76f79-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="76f79-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="76f79-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76f79-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76f79-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76f79-149">OUTPUTS</span></span>

### <span data-ttu-id="76f79-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="76f79-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="76f79-151">Note</span><span class="sxs-lookup"><span data-stu-id="76f79-151">NOTES</span></span>

## <span data-ttu-id="76f79-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76f79-152">RELATED LINKS</span></span>
