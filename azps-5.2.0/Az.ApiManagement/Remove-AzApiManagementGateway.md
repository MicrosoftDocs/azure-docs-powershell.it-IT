---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361378"
---
# <span data-ttu-id="f78ae-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="f78ae-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="f78ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f78ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f78ae-103">Disconnette un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="f78ae-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="f78ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f78ae-104">SYNTAX</span></span>

### <span data-ttu-id="f78ae-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f78ae-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f78ae-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f78ae-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f78ae-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f78ae-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f78ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f78ae-108">DESCRIPTION</span></span>
<span data-ttu-id="f78ae-109">Il cmdlet **Remove-AzApiManagementGateway** DISCONNETTE un'API da un gateway.</span><span class="sxs-lookup"><span data-stu-id="f78ae-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="f78ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f78ae-110">EXAMPLES</span></span>

### <span data-ttu-id="f78ae-111">Esempio 1: rimuovere un gateway esistente</span><span class="sxs-lookup"><span data-stu-id="f78ae-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="f78ae-112">Questo comando rimuove un gateway esistente e non chiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="f78ae-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="f78ae-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f78ae-113">PARAMETERS</span></span>

### <span data-ttu-id="f78ae-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f78ae-114">-Context</span></span>
<span data-ttu-id="f78ae-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f78ae-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f78ae-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f78ae-116">This parameter is required.</span></span>

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

### <span data-ttu-id="f78ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78ae-117">-DefaultProfile</span></span>
<span data-ttu-id="f78ae-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f78ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f78ae-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f78ae-119">-GatewayId</span></span>
<span data-ttu-id="f78ae-120">Identificatore del gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="f78ae-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="f78ae-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f78ae-121">This parameter is required.</span></span>

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

### <span data-ttu-id="f78ae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f78ae-122">-InputObject</span></span>
<span data-ttu-id="f78ae-123">Istanza di PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="f78ae-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="f78ae-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f78ae-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f78ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f78ae-125">-PassThru</span></span>
<span data-ttu-id="f78ae-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="f78ae-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f78ae-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f78ae-127">This parameter is optional.</span></span>
<span data-ttu-id="f78ae-128">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="f78ae-128">Default value is false.</span></span>

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

### <span data-ttu-id="f78ae-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f78ae-129">-ResourceId</span></span>
<span data-ttu-id="f78ae-130">ARM ResourceId del gateway.</span><span class="sxs-lookup"><span data-stu-id="f78ae-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="f78ae-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f78ae-131">This parameter is required.</span></span>

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

### <span data-ttu-id="f78ae-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f78ae-132">-Confirm</span></span>
<span data-ttu-id="f78ae-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78ae-134">-WhatIf</span></span>
<span data-ttu-id="f78ae-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f78ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78ae-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f78ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78ae-137">CommonParameters</span></span>
<span data-ttu-id="f78ae-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78ae-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f78ae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78ae-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f78ae-140">INPUTS</span></span>

### <span data-ttu-id="f78ae-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f78ae-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f78ae-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f78ae-142">System.String</span></span>

### <span data-ttu-id="f78ae-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f78ae-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f78ae-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f78ae-144">OUTPUTS</span></span>

### <span data-ttu-id="f78ae-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f78ae-145">System.Boolean</span></span>

## <span data-ttu-id="f78ae-146">Note</span><span class="sxs-lookup"><span data-stu-id="f78ae-146">NOTES</span></span>

## <span data-ttu-id="f78ae-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f78ae-147">RELATED LINKS</span></span>
