---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342955"
---
# <span data-ttu-id="1e805-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e805-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1e805-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e805-102">SYNOPSIS</span></span>
<span data-ttu-id="1e805-103">Rimuove un set di versioni dell'API specifico</span><span class="sxs-lookup"><span data-stu-id="1e805-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="1e805-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e805-104">SYNTAX</span></span>

### <span data-ttu-id="1e805-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e805-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e805-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e805-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e805-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e805-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e805-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e805-108">DESCRIPTION</span></span>

<span data-ttu-id="1e805-109">Il cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** rimuove un set di versioni dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="1e805-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="1e805-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e805-110">EXAMPLES</span></span>

### <span data-ttu-id="1e805-111">Esempio 1: rimuovere un set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="1e805-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="1e805-112">Questo comando rimuove il set di versioni dell'API con il ApiVersionSetId specificato.</span><span class="sxs-lookup"><span data-stu-id="1e805-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="1e805-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e805-113">PARAMETERS</span></span>

### <span data-ttu-id="1e805-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1e805-114">-ApiVersionSetId</span></span>
<span data-ttu-id="1e805-115">Identificatore del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="1e805-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="1e805-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e805-116">This parameter is required.</span></span>

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

### <span data-ttu-id="1e805-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1e805-117">-Context</span></span>
<span data-ttu-id="1e805-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1e805-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1e805-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e805-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e805-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e805-120">-DefaultProfile</span></span>
<span data-ttu-id="1e805-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e805-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e805-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e805-122">-InputObject</span></span>
<span data-ttu-id="1e805-123">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1e805-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="1e805-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e805-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e805-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e805-125">-PassThru</span></span>
<span data-ttu-id="1e805-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e805-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1e805-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1e805-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e805-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e805-128">-ResourceId</span></span>
<span data-ttu-id="1e805-129">ResourceId ARM di ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1e805-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="1e805-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e805-130">This parameter is required.</span></span>

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

### <span data-ttu-id="1e805-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e805-131">-Confirm</span></span>
<span data-ttu-id="1e805-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e805-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e805-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e805-133">-WhatIf</span></span>
<span data-ttu-id="1e805-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e805-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e805-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e805-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e805-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e805-136">CommonParameters</span></span>
<span data-ttu-id="1e805-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e805-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e805-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e805-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e805-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e805-139">INPUTS</span></span>

### <span data-ttu-id="1e805-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1e805-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1e805-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e805-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="1e805-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1e805-142">System.String</span></span>

## <span data-ttu-id="1e805-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e805-143">OUTPUTS</span></span>

### <span data-ttu-id="1e805-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e805-144">System.Boolean</span></span>

## <span data-ttu-id="1e805-145">Note</span><span class="sxs-lookup"><span data-stu-id="1e805-145">NOTES</span></span>

## <span data-ttu-id="1e805-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e805-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e805-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e805-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1e805-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e805-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1e805-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1e805-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)