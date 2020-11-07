---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852493"
---
# <span data-ttu-id="2de13-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2de13-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2de13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2de13-102">SYNOPSIS</span></span>
<span data-ttu-id="2de13-103">Rimuove un set di versioni dell'API specifico</span><span class="sxs-lookup"><span data-stu-id="2de13-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="2de13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2de13-104">SYNTAX</span></span>

### <span data-ttu-id="2de13-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2de13-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de13-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2de13-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2de13-107">DESCRIPTION</span></span>

<span data-ttu-id="2de13-108">Il cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** rimuove un set di versioni dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="2de13-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="2de13-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2de13-109">EXAMPLES</span></span>

### <span data-ttu-id="2de13-110">Esempio 1: rimuovere un set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="2de13-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="2de13-111">Questo comando rimuove il set di versioni dell'API con il ApiVersionSetId specificato.</span><span class="sxs-lookup"><span data-stu-id="2de13-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="2de13-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2de13-112">PARAMETERS</span></span>

### <span data-ttu-id="2de13-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2de13-113">-ApiVersionSetId</span></span>
<span data-ttu-id="2de13-114">Identificatore del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="2de13-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="2de13-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2de13-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2de13-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2de13-116">-Context</span></span>
<span data-ttu-id="2de13-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2de13-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2de13-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2de13-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2de13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de13-119">-DefaultProfile</span></span>
<span data-ttu-id="2de13-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2de13-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de13-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2de13-121">-InputObject</span></span>
<span data-ttu-id="2de13-122">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2de13-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="2de13-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2de13-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2de13-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2de13-124">-PassThru</span></span>
<span data-ttu-id="2de13-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="2de13-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2de13-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2de13-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="2de13-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2de13-127">-Confirm</span></span>
<span data-ttu-id="2de13-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2de13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de13-129">-WhatIf</span></span>
<span data-ttu-id="2de13-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2de13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de13-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2de13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de13-132">CommonParameters</span></span>
<span data-ttu-id="2de13-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de13-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de13-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2de13-135">INPUTS</span></span>

### <span data-ttu-id="2de13-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2de13-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2de13-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2de13-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="2de13-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2de13-138">System.String</span></span>

## <span data-ttu-id="2de13-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2de13-139">OUTPUTS</span></span>

### <span data-ttu-id="2de13-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2de13-140">System.Boolean</span></span>

## <span data-ttu-id="2de13-141">Note</span><span class="sxs-lookup"><span data-stu-id="2de13-141">NOTES</span></span>

## <span data-ttu-id="2de13-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2de13-142">RELATED LINKS</span></span>

[<span data-ttu-id="2de13-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2de13-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2de13-144">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2de13-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2de13-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2de13-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)