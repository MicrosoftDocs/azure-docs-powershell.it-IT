---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 32677a5b8c3383b23b6ebb9832842f410a74532f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020859"
---
# <span data-ttu-id="7764c-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7764c-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="7764c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7764c-102">SYNOPSIS</span></span>
<span data-ttu-id="7764c-103">Rimozione di una particolare revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="7764c-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="7764c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7764c-104">SYNTAX</span></span>

### <span data-ttu-id="7764c-105">ByApiId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7764c-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7764c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7764c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7764c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7764c-107">DESCRIPTION</span></span>
<span data-ttu-id="7764c-108">Il cmdlet **Remove-AzApiManagementApiRevision** rimuove una particolare revisione API.</span><span class="sxs-lookup"><span data-stu-id="7764c-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="7764c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7764c-109">EXAMPLES</span></span>

### <span data-ttu-id="7764c-110">Esempio 1: rimuovere una revisione API</span><span class="sxs-lookup"><span data-stu-id="7764c-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="7764c-111">Questo comando rimuove la `2` revisione dell'API `echo-api` dal servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="7764c-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="7764c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7764c-112">PARAMETERS</span></span>

### <span data-ttu-id="7764c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7764c-113">-ApiId</span></span>
<span data-ttu-id="7764c-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="7764c-114">Identifier of the API.</span></span>
<span data-ttu-id="7764c-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7764c-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7764c-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7764c-116">-ApiRevision</span></span>
<span data-ttu-id="7764c-117">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="7764c-117">Identifier of the API Revision.</span></span> <span data-ttu-id="7764c-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7764c-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7764c-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7764c-119">-Context</span></span>
<span data-ttu-id="7764c-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7764c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7764c-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7764c-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7764c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7764c-122">-DefaultProfile</span></span>
<span data-ttu-id="7764c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7764c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7764c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7764c-124">-InputObject</span></span>
<span data-ttu-id="7764c-125">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="7764c-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="7764c-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7764c-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7764c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7764c-127">-PassThru</span></span>
<span data-ttu-id="7764c-128">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="7764c-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="7764c-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7764c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="7764c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7764c-130">-Confirm</span></span>
<span data-ttu-id="7764c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7764c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7764c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7764c-132">-WhatIf</span></span>
<span data-ttu-id="7764c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7764c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7764c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7764c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7764c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7764c-135">CommonParameters</span></span>
<span data-ttu-id="7764c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7764c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7764c-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7764c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7764c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7764c-138">INPUTS</span></span>

### <span data-ttu-id="7764c-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7764c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7764c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7764c-140">System.String</span></span>

### <span data-ttu-id="7764c-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7764c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7764c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7764c-142">OUTPUTS</span></span>

### <span data-ttu-id="7764c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7764c-143">System.Boolean</span></span>

## <span data-ttu-id="7764c-144">Note</span><span class="sxs-lookup"><span data-stu-id="7764c-144">NOTES</span></span>

## <span data-ttu-id="7764c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7764c-145">RELATED LINKS</span></span>

[<span data-ttu-id="7764c-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7764c-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="7764c-147">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7764c-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="7764c-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7764c-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)