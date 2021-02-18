---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201303"
---
# <span data-ttu-id="675e5-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="675e5-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="675e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="675e5-102">SYNOPSIS</span></span>
<span data-ttu-id="675e5-103">Rimuove una determinata versione di API</span><span class="sxs-lookup"><span data-stu-id="675e5-103">Removes a particular API Release</span></span>

## <span data-ttu-id="675e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="675e5-104">SYNTAX</span></span>

### <span data-ttu-id="675e5-105">ByApiReleaseId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="675e5-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="675e5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="675e5-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="675e5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="675e5-107">DESCRIPTION</span></span>

<span data-ttu-id="675e5-108">Il cmdlet **Remove-AzAzureRmApiManagementApiRelease** rimuove una versione DI API esistente.</span><span class="sxs-lookup"><span data-stu-id="675e5-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="675e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="675e5-109">EXAMPLES</span></span>

### <span data-ttu-id="675e5-110">Esempio 1: Rimuovere una versione di API</span><span class="sxs-lookup"><span data-stu-id="675e5-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="675e5-111">Questo comando rimuove la versione di API con i valori ApiId e ReleaseId specificati.</span><span class="sxs-lookup"><span data-stu-id="675e5-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="675e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="675e5-112">PARAMETERS</span></span>

### <span data-ttu-id="675e5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="675e5-113">-ApiId</span></span>
<span data-ttu-id="675e5-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="675e5-114">Identifier of the API.</span></span>
<span data-ttu-id="675e5-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="675e5-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675e5-116">-Context</span><span class="sxs-lookup"><span data-stu-id="675e5-116">-Context</span></span>
<span data-ttu-id="675e5-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="675e5-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="675e5-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="675e5-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="675e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675e5-119">-DefaultProfile</span></span>
<span data-ttu-id="675e5-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="675e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="675e5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="675e5-121">-InputObject</span></span>
<span data-ttu-id="675e5-122">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="675e5-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="675e5-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="675e5-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="675e5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="675e5-124">-PassThru</span></span>
<span data-ttu-id="675e5-125">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="675e5-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="675e5-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="675e5-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="675e5-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="675e5-127">-ReleaseId</span></span>
<span data-ttu-id="675e5-128">Identificatore della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="675e5-128">Identifier of the API Release.</span></span>
<span data-ttu-id="675e5-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="675e5-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="675e5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="675e5-130">-Confirm</span></span>
<span data-ttu-id="675e5-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="675e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="675e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="675e5-132">-WhatIf</span></span>
<span data-ttu-id="675e5-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="675e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="675e5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="675e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="675e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675e5-135">CommonParameters</span></span>
<span data-ttu-id="675e5-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="675e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675e5-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="675e5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675e5-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="675e5-138">INPUTS</span></span>

### <span data-ttu-id="675e5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="675e5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="675e5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="675e5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="675e5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="675e5-141">System.String</span></span>

## <span data-ttu-id="675e5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="675e5-142">OUTPUTS</span></span>

### <span data-ttu-id="675e5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="675e5-143">System.Boolean</span></span>

## <span data-ttu-id="675e5-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="675e5-144">NOTES</span></span>

## <span data-ttu-id="675e5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="675e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="675e5-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="675e5-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="675e5-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="675e5-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="675e5-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="675e5-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)