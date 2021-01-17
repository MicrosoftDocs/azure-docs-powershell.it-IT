---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382112"
---
# <span data-ttu-id="9a604-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="9a604-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="9a604-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a604-102">SYNOPSIS</span></span>
<span data-ttu-id="9a604-103">Disconnette un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="9a604-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="9a604-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a604-104">SYNTAX</span></span>

### <span data-ttu-id="9a604-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a604-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a604-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a604-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a604-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a604-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a604-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a604-108">DESCRIPTION</span></span>
<span data-ttu-id="9a604-109">Il cmdlet **Remove-AzApiManagementGateway** DISCONNETTE un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="9a604-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="9a604-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a604-110">EXAMPLES</span></span>

### <span data-ttu-id="9a604-111">Esempio 1: rimuovere un gateway esistente</span><span class="sxs-lookup"><span data-stu-id="9a604-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="9a604-112">Questo comando rimuove un gateway esistente e non chiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="9a604-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="9a604-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a604-113">PARAMETERS</span></span>

### <span data-ttu-id="9a604-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9a604-114">-Context</span></span>
<span data-ttu-id="9a604-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9a604-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9a604-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a604-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9a604-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a604-117">-DefaultProfile</span></span>
<span data-ttu-id="9a604-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a604-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a604-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9a604-119">-GatewayId</span></span>
<span data-ttu-id="9a604-120">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="9a604-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="9a604-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a604-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9a604-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a604-122">-InputObject</span></span>
<span data-ttu-id="9a604-123">Istanza di PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="9a604-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="9a604-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a604-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9a604-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a604-125">-PassThru</span></span>
<span data-ttu-id="9a604-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="9a604-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9a604-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9a604-127">This parameter is optional.</span></span>
<span data-ttu-id="9a604-128">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="9a604-128">Default value is false.</span></span>

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

### <span data-ttu-id="9a604-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a604-129">-ResourceId</span></span>
<span data-ttu-id="9a604-130">ARM ResourceId del gateway.</span><span class="sxs-lookup"><span data-stu-id="9a604-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="9a604-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a604-131">This parameter is required.</span></span>

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

### <span data-ttu-id="9a604-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a604-132">-Confirm</span></span>
<span data-ttu-id="9a604-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a604-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a604-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a604-134">-WhatIf</span></span>
<span data-ttu-id="9a604-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a604-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a604-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a604-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a604-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a604-137">CommonParameters</span></span>
<span data-ttu-id="9a604-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a604-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a604-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a604-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a604-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a604-140">INPUTS</span></span>

### <span data-ttu-id="9a604-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a604-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a604-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9a604-142">System.String</span></span>

### <span data-ttu-id="9a604-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a604-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a604-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a604-144">OUTPUTS</span></span>

### <span data-ttu-id="9a604-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a604-145">System.Boolean</span></span>

## <span data-ttu-id="9a604-146">Note</span><span class="sxs-lookup"><span data-stu-id="9a604-146">NOTES</span></span>

## <span data-ttu-id="9a604-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a604-147">RELATED LINKS</span></span>
